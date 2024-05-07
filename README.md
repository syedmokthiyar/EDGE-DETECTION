#  EX:06 EDGE-DETECTION
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
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("fahad.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
## ORIGINAL IMAGE:
![Screenshot 2024-05-06 221959](https://github.com/syedmokthiyar/EDGE-DETECTION/assets/118787294/caa9de1b-ccae-4dbf-b19f-543105052785)


### SOBEL EDGE DETECTOR

![Screenshot 2024-05-06 221816](https://github.com/syedmokthiyar/EDGE-DETECTION/assets/118787294/9ec1bba1-97c3-4386-ab81-38c74b3c204f)
![Screenshot 2024-05-06 221845](https://github.com/syedmokthiyar/EDGE-DETECTION/assets/118787294/a1a7f32a-b533-45a3-97ea-2c165a56cec9)
![Screenshot 2024-05-06 221904](https://github.com/syedmokthiyar/EDGE-DETECTION/assets/118787294/b7bd82aa-ed69-4698-b5e9-d6fe8c850686)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-05-06 221712](https://github.com/syedmokthiyar/EDGE-DETECTION/assets/118787294/f422c95d-3034-4038-a99e-27afa240bd13)


### CANNY EDGE DETECTOR
![Screenshot 2024-05-06 221623](https://github.com/syedmokthiyar/EDGE-DETECTION/assets/118787294/e1d7a613-7ccb-4e73-bd0c-ff042223725a)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
