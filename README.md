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

## Program:
```
NAME:KATHI HASINI
REG NO:212224240074
```
### ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('exp-6.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
### ORIGINAL IMAGE:
<img width="728" height="537" alt="image" src="https://github.com/user-attachments/assets/c61d2e15-7751-44dd-87aa-ffe76601efff" />

### SOBEL EDGE DETECTION:
<img width="754" height="540" alt="image" src="https://github.com/user-attachments/assets/7e4a192c-b1e7-43f5-945b-f794afc3a277" />

### LAPLACIAN EDGE DETECTOR:

<img width="795" height="546" alt="image" src="https://github.com/user-attachments/assets/d28dbdea-43ad-4ce5-9c7c-7ed0183ce96c" />

### CANNY EDGE DETECTOR:
<img width="786" height="549" alt="image" src="https://github.com/user-attachments/assets/94351feb-88e9-42fb-98d8-b9eeaa150469" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
