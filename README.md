# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required packages.

### Step2
Assign the image to a variable.

### Step3
Use the image filtering techniques.

### Step4
Display the respective outputs.

### Step5
End the program.

## Program:
### Developed By   : Shobika P
### Register Number: 212221230096
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('panda img.webp')
image1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel = np.ones((11,11),np.float32)/121
image2 = cv2.filter2D(image1,-1,kernel)


plt.figure(figsize =(15,15))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image2)
plt.title('Box Filter')
plt.axis('off')


```
ii) Using Weighted Averaging Filter
```Python

kernel1 = np.array([[1,2,1],[2,4,2],[1,2,1]])/30
image2 = cv2.filter2D(image1,-1,kernel1)
plt.figure(figsize =(15,15))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image2)
plt.title('Weighted Averaging Filter')
plt.axis('off')




```
iii) Using Gaussian Filter
```Python

gaussian_blur = cv2.GaussianBlur(src = image1, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (15,15))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Filter")
plt.axis("off")




```

iv) Using Median Filter
```Python

median = cv2.medianBlur(src = image1,ksize = 11)
plt.figure(figsize = (15,15))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Filter")
plt.axis("off"


```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(image1,-1,kernel3)
plt.figure(figsize = (15,15))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("laplacian kernel")
plt.axis("off")




```
ii) Using Laplacian Operator
```Python


laplacian_operator = cv2.Laplacian(image1,cv2.CV_64F)
plt.figure(figsize = (15,15))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("laplacian operator")
plt.axis("off")


```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![img 3](https://user-images.githubusercontent.com/94508142/232323020-9505eff9-d2ee-48cf-893a-56d52365ffd8.jpeg)


ii) Using Weighted Averaging Filter
![img 6](https://user-images.githubusercontent.com/94508142/232322979-8d5c6d7d-4a07-454e-8aa0-2a1b6263497a.jpeg)

iii) Using Gaussian Filter
![img 4](https://user-images.githubusercontent.com/94508142/232322998-335b1641-2a89-4107-9fe6-af122964dc50.jpeg)

iv) Using Median Filter
![img 5](https://user-images.githubusercontent.com/94508142/232322952-21aba882-c764-4a92-9ff9-2f664c758c0e.jpeg)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![img 1](https://user-images.githubusercontent.com/94508142/232323036-904ccda8-733a-432a-9323-df3fa2000f1d.jpeg)


ii) Using Laplacian Operator
![img 7](https://user-images.githubusercontent.com/94508142/232322930-c603daa0-9949-4aa0-8e69-214e61cd2c15.jpeg)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
