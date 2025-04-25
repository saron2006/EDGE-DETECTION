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
### Original Image
```
#Developed by : Saron xavier a
#Register No: 212223230197
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('bird.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')




```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
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
### ORIGINAL IMAGE 
![Screenshot 2025-04-25 122635](https://github.com/user-attachments/assets/7482b74f-4144-491a-a154-4f62a2be06b8)


### SOBEL EDGE DETECTOR
![Screenshot 2025-04-25 122646](https://github.com/user-attachments/assets/5e7485eb-31bf-4d71-af34-2ecd5b341a52)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2025-04-25 122655](https://github.com/user-attachments/assets/a8d001b3-a582-4c91-b759-a3a872cc0f38)

### CANNY EDGE DETECTOR
![Screenshot 2025-04-25 122706](https://github.com/user-attachments/assets/35dfb437-cba3-439c-98d1-588290165734)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
