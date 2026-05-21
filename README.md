# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.
## NAME : DINESH R
## REG NO :212224240037
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program


# Load the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

```

# Read the Image and convert to grayscale
```
image = cv2.imread("C:\\Users\\admin\\Downloads\\My image.png")  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  

```



# Convert from BGR to RGB for display
```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
```
# Use Global thresholding to segment the image
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

```

# Use Adaptive thresholding to segment the image

```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)


```


# Use Otsu's method to segment the image 
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```



# Display the results

# Global Thresholding
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```
plt.tight_layout()
plt.show()

```


## Output

### Original Image

<img width="1024" height="381" alt="image" src="https://github.com/user-attachments/assets/07dca73c-e666-4e84-8bf1-339989464e2a" />


### Global Thresholding

<img width="795" height="374" alt="image" src="https://github.com/user-attachments/assets/9ccc0294-3f4a-4ddf-86d8-d93bcdfbdce7" />

### Adaptive Thresholding
<img width="382" height="356" alt="image" src="https://github.com/user-attachments/assets/676895cc-b126-45e8-af83-796777348a75" />


### Optimum Global Thesholding using Otsu's Method

<img width="278" height="294" alt="image" src="https://github.com/user-attachments/assets/4a8f2484-746a-44ed-943e-65944a7566d1" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
