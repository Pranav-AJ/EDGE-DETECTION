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

## Output:

```
import cv2
# Read the image
image = cv2.imread('flower.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Gaussian blur
img_blurred = cv2.GaussianBlur(gray_image, (3, 3), 0)

# Sobel edge detection
sobelx = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 0, ksize=5)
sobely = cv2.Sobel(img_blurred, cv2.CV_64F, 0, 1, ksize=5)
sobelxy = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 1, ksize=5)

# Laplacian edge detection
laplacian = cv2.Laplacian(img_blurred, cv2.CV_64F)

# Canny edge detection
canny_edges = cv2.Canny(img_blurred, 120, 150)

# Display images
cv2.imshow('Original', gray_image)
cv2.imshow('Sobel X', sobelx)
cv2.imshow('Sobel Y', sobely)
cv2.imshow('Sobel XY', sobelxy)
cv2.imshow('Laplacian', laplacian)
cv2.imshow('Canny Edges', canny_edges)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/e5ef6271-9eed-4919-a9c0-c0a72a5ba7dd)

![image](https://github.com/user-attachments/assets/6bcaa597-f79d-4481-9378-b24469b3b610)

![image](https://github.com/user-attachments/assets/2a1f8ac7-bb39-45e4-9833-50d5ebb26fbb)

![image](https://github.com/user-attachments/assets/e01f3b3a-3a95-48df-85dc-fda697c4faee)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/5d4a8541-dbb3-4165-929f-90f9cd1481e1)


### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/ebc3cbae-c0d9-483a-af53-6bee473ba67b)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
