# EXP5-Implementation-of-filter

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Using Averaging Filter

### Step2
Using Weighted Averaging Filter

### Step3
Using Gaussian Filter

### Step4
Using Median Filter

### Step5
Using Laplacian Kernal

### Step6
Using Laplacian Operator

## Program: 

### Name: KAMALESHWAR KV
### Reg.No: 212223240063

### 1. Smoothing Filters
i) Using Averaging Filter

```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Ganesh_D.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```

<img width="614" height="350" alt="image" src="https://github.com/user-attachments/assets/838a6d77-1834-4f3a-b6c2-21ce0391f904" />


ii) Using Weighted Averaging Filter

```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

<img width="451" height="262" alt="image" src="https://github.com/user-attachments/assets/59764130-06c7-4303-ab74-e83c6ef2bb62" />


iii) Using Gaussian Filter

```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

<img width="529" height="315" alt="image" src="https://github.com/user-attachments/assets/85a0bcb6-8340-4366-b752-a00854bc75b0" />


iv)Using Median Filter

```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

<img width="738" height="416" alt="image" src="https://github.com/user-attachments/assets/5e5921e6-5267-41ad-85a1-980db5b85058" />


### 2. Sharpening Filters

i) Using Laplacian Linear Kernal

```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

<img width="531" height="310" alt="image" src="https://github.com/user-attachments/assets/5fabee01-6b2a-4683-ae3f-8c18c827d27c" />


ii) Using Laplacian Operator

```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

<img width="526" height="304" alt="image" src="https://github.com/user-attachments/assets/b557fb54-8a95-48b7-93dc-79817f530b5a" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
