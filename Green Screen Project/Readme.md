
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

Next, have to load the image, here with `openCV` when we load the image it will load it as a `BGR` image so have to convert it into `RGB` image for further image processing, so we use a funtion called `cvtColor`. 
```python
image = cv.imshow('image path in system')
# converting to RGB
image_rgb = cv.cvtColor(image, cv.COLOR_BGR2RGB)
```
![74c4f21f-296a-4ab2-81e1-64cd18e47bcd](https://user-images.githubusercontent.com/71933145/164051020-d32c7b33-75dc-4bf0-9a37-d7ce28c1b51a.png)
   `BGR to RGB`
![b6465f83-e08e-45db-b407-04539126e3bc](https://user-images.githubusercontent.com/71933145/164051095-ee61e70c-9088-4670-91d7-be24dc1c8828.png)


For better colour seperation we use hsv gradient to sopt the green colour. Again the `image_rgb` has to be converted to `HSV` image.
```python
# converting to HSV
image_hsv = cv.cvtColor(image_rgb, cv.COLOR_BGR2RGB)
```
![b6465f83-e08e-45db-b407-04539126e3bc](https://user-images.githubusercontent.com/71933145/164051095-ee61e70c-9088-4670-91d7-be24dc1c8828.png)
 `RGB to HSV`
![b1cb2155-ceff-4875-8ea1-92e58bc41aef](https://user-images.githubusercontent.com/71933145/164051234-aff8ced2-273a-464b-a50b-3c77e4df0d53.png)

Once `HSV` image is ready we can create a mask and remove the green screen. and replace it with the background.
![00b0d390-5866-4626-bb56-5935d16da6a8](https://user-images.githubusercontent.com/71933145/164052473-5802279c-dd98-4aac-8c2a-d37e2aac0a39.png) Masking 
![9dade35c-2d20-4c02-96bd-4fae242f967d](https://user-images.githubusercontent.com/71933145/164052615-cd8a6882-9395-4871-ba2a-7cab2f8f970c.png) Replacing
