# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM:
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("ro.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
#### SOBEL Y AXIS
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
#### SOBEL XY AXIS
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS
![image](https://github.com/shalini-venkatesan/EDGE-DETECTION/assets/118720291/e852e3cb-b4c5-4ab1-a98c-de26fad4c267)


#### SOBEL Y AXIS
![image](https://github.com/shalini-venkatesan/EDGE-DETECTION/assets/118720291/7723e958-d768-4573-babf-2707ab066bb5)


#### SOBEL XY AXIS

![image](https://github.com/shalini-venkatesan/EDGE-DETECTION/assets/118720291/d19a56e7-a049-436e-96c8-30c962dd4242)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/shalini-venkatesan/EDGE-DETECTION/assets/118720291/ab7e2dd9-e48c-47f9-8d56-c03bc9bc6d2f)


### CANNY EDGE DETECTOR

![image](https://github.com/shalini-venkatesan/EDGE-DETECTION/assets/118720291/329bdc00-dd99-4ca4-99e4-bff6154db3e0)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
