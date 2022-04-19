
# Green Screen Replacement

[![Platform](https://img.shields.io/badge/Platform-Windows-yellow.svg?longCache=true&style=flat-square)](https://www.microsoft.com/de-de/windows/windows-11-45434254328)
[![openCV 4.5.5](https://img.shields.io/badge/openCV-4.5.5-red.svg?longCache=true&style=flat-square)](https://docs.opencv.org/4.5.5/d4/db1/tutorial_documentation.html)
[![NumPy 1.22.3](https://img.shields.io/badge/NumPy-1.22.3-green.svg?longCache=true&style=flat-square)](https://numpy.org/doc/stable/)
[![Matplotlib 3.5.1](https://img.shields.io/badge/Matplotlib-3.5.1-blue.svg?longCache=true&style=flat-square)](https://matplotlib.org/stable/)

Green screens are widely used in Media domain, where we can create a new place from the place we are located, good example for this is Weather Forecasting.
The tool used in this scenario is **openCV**, so, here I'm going to apply openCV on a simple image where the green screen will be replaced with another background.

### 📦 *Installation*

Install the required libraries into the the environment. Using the line below we can install the libraries.
You check the versions from the `requirements.txt`


```bash
pip install -r requirements.txt
```
### 🚀 *How to use*

Initially we to import the libraries
```python
import cv2 as cv
import numpy as np
import matplotlib.pyplot as plt
```
### Notes

Next, have to load the image, here with `openCV` when we load the image it will load it as a `BGR` image so have to convert it into `RGB` image for further image processing, so we use a funtion called `cvtColor`. Here it goes..
```python
image = cv.imshow('image path in system')
# converting to RGB
image_rgb = cv.cvtColor(image, cv.COLOR_BGR2RGB)
```
![0b13d2ad-fa54-432f-a34c-fda328e8ef2b](https://user-images.githubusercontent.com/71933145/164049518-a46bfe22-9e10-4cd0-ad00-a9809592a6b4.png)


For better colour seperation we use hsv gradient to sopt the green colour. Again the `image_rgb` has to be converted to `HSV` image.
```python
# converting to HSV
image_hsv = cv.cvtColor(image_rgb, cv.COLOR_BGR2RGB)
```
