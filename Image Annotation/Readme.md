# Image annotation

[![Platform](https://img.shields.io/badge/Platform-Windows-yellow.svg?longCache=true&style=flat-square)](https://www.microsoft.com/de-de/windows/windows-11-45434254328)
[![openCV 4.5.5](https://img.shields.io/badge/openCV-4.5.5-red.svg?longCache=true&style=flat-square)](https://docs.opencv.org/4.5.5/d4/db1/tutorial_documentation.html)
[![NumPy 1.22.3](https://img.shields.io/badge/NumPy-1.22.3-green.svg?longCache=true&style=flat-square)](https://numpy.org/doc/stable/)
[![Matplotlib 3.5.1](https://img.shields.io/badge/Matplotlib-3.5.1-blue.svg?longCache=true&style=flat-square)](https://matplotlib.org/stable/)

Image annotation plays a significant role in computer vision, the technology that allows computers to gain high-level understanding from digital images or videos and to see and interpret visual information just like humans.

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
