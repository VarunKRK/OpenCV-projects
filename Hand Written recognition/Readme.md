# Hand Written recognition

[![Platform](https://img.shields.io/badge/Platform-Windows-yellow.svg?longCache=true&style=flat-square)](https://www.microsoft.com/de-de/windows/windows-11-45434254328)
[![openCV 4.5.5](https://img.shields.io/badge/openCV-4.5.5-red.svg?longCache=true&style=flat-square)](https://docs.opencv.org/4.5.5/d4/db1/tutorial_documentation.html)
[![NumPy 1.22.3](https://img.shields.io/badge/NumPy-1.22.3-green.svg?longCache=true&style=flat-square)](https://numpy.org/doc/stable/)
[![Matplotlib 3.5.1](https://img.shields.io/badge/Matplotlib-3.5.1-blue.svg?longCache=true&style=flat-square)](https://matplotlib.org/stable/)
[![Scikit-learn 1.0.2](https://img.shields.io/badge/Scikit-1.0.2-yellow.svg?longCache=true&style=flat-square)](https://scikit-learn.org/stable/index.html)

Hand Written recognition of digits on real data by training the model with MNIST dataset. The model takes the real images an convert them to machine learnable format and gives the output. The error rate is 5%.

![40600296-2180-468d-b68c-073c2ca83062](https://user-images.githubusercontent.com/71933145/164161315-80d93b03-51ca-4673-bd1b-e989a225be75.png) predicts '1'

### 📦 *Installation*

Install the required libraries into the the environment. Using the line below we can install the libraries.
You check the versions from the `requirements.txt`


```bash
pip install -r requirements.txt
```
### 🚀 *How to use*

Initially we have to import the libraries, here i use LightGBM model for prediction.
```python
import cv2 as cv
import numpy as np
import matplotlib.pyplot as plt
from lightgbm import LGBMClassifier
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
```
- Have to create a dataset from the `MNIST` using file operations by using `import os`.
- create target classes.
- reshape the data.(28 x 28 = 784)
- Split the data for training and scale the train data.
- Performing PCA for dimensionality reduction(they are 784 features after reshaping)
- Train the model(I used LightGBM Classifier from former results)
- Test the model
- Get the real data using `openCV`, perform image transformation and resize to 28x28. 
- Predict the real data now with the trained model
