# QR code Detector

[![Platform](https://img.shields.io/badge/Platform-Windows-yellow.svg?longCache=true&style=flat-square)](https://www.microsoft.com/de-de/windows/windows-11-45434254328)
[![openCV 4.5.5](https://img.shields.io/badge/openCV-4.5.5-red.svg?longCache=true&style=flat-square)](https://docs.opencv.org/4.5.5/d4/db1/tutorial_documentation.html)
[![NumPy 1.22.3](https://img.shields.io/badge/NumPy-1.22.3-green.svg?longCache=true&style=flat-square)](https://numpy.org/doc/stable/)
[![Matplotlib 3.5.1](https://img.shields.io/badge/Matplotlib-3.5.1-blue.svg?longCache=true&style=flat-square)](https://matplotlib.org/stable/)

QR code is a machine-scannable image that can instantly be read using a Smartphone camera now-a-days.
Here we are using `openCV` to detect the QR code.

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
Another two functions are used
`QRCodeDetector()` and `detectAndDecode()` which are in library to detect and decode.

Finally, to display the QR code and not to crash the code.
```python
cv.imshow(your qr code image here)
cv.waitKey(0)
cv.destroyAllWindows()
```
