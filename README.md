## THRESHOLDING

## AIM:

To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## SOFTWARE REQUIRED:

* Anaconda - Python 3.7
* OpenCV

## ALGORITHM:

## Step1:

Load the necessary packages

## Step2:

Read the Image and convert to grayscale

## Step3:

Use Global thresholding to segment the image.

## Step4:

Use Adaptive thresholding to segment the image.

## Step5:

Use Otsu's method to segment the image and display the results.

## Program:

## Developed by: Syed Shamsheer Ali
## Register Number: 212225220114

## Original Image:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

```
image = cv2.imread(r"C:\Users\syedf\OneDrive\Documents\DIPT\Syed1.png")

if image is not None:
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.title("Original Image")
    plt.show()
```

## Global Thresholding with a Threshold value of 127:

```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
```

## Adaptive Thresholding Using Gaussian Method:

```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```

## Otsu's method for Optimal Thresholding:

```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```

## Original Image:

```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
```

## Global Thresholding:

```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```

## Adaptive Thresholding:

```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```

## Otsu's Method:

```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```

## Show the plot:

```
plt.tight_layout()
plt.show()
```

## Output:

## Original Image:

<img width="180" height="245" alt="image" src="https://github.com/user-attachments/assets/d45a4892-2bbe-439b-a204-786dcce31dcf" />

## Global Thresholding Image:

<img width="221" height="261" alt="image" src="https://github.com/user-attachments/assets/929f5f8c-ab83-453f-8cb4-6a1727e31ac5" />


## Adaptive Thresholding:

<img width="250" height="266" alt="image" src="https://github.com/user-attachments/assets/3e0c6045-08e8-41e0-96e4-97f659f668b1" />

## Otsu's Method:

<img width="182" height="248" alt="image" src="https://github.com/user-attachments/assets/9f027127-cc36-4979-9c9d-27baf5307013" />

## Result:

Thus, image segmentation is successfully performed using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques in OpenCV.
