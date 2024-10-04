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

### Program

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('flower.jpeg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)

# Display results using Matplotlib
plt.figure(figsize=(12, 12))

# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

# Sobel Edge Detection
plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

# Laplacian Edge Detection
plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

# Canny Edge Detection
plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

# Show all results
plt.tight_layout()
plt.show()

```

## Output:

![image](https://github.com/user-attachments/assets/a93c5044-0936-4a59-89e8-a8bbe30bc249)

![image](https://github.com/user-attachments/assets/56d9630a-5ebe-4b1f-8b66-084e023d208e)

![image](https://github.com/user-attachments/assets/0a9838f4-6fad-4961-aa2e-05c8be5352f6)

![image](https://github.com/user-attachments/assets/af971099-904c-4de0-b7e7-4babae0f83bb)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
