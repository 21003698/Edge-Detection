# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the required packages.
<br>


### Step2:
Load the image to operate on.
<br>

### Step3:
Convert the image to grayscale image.
<br>

### Step4:
Use Sobel operator along x,y and xy directions.
<br>

### Step5:
Operate the image using Laplacian operator.
<br>

### Step6:
Operate the image using Canny Edge operator.
<br>

### Step7:
Show all the operated images output.
<br>

### step8:
End the program.
<br>


 
## Program:

``` Python
#Program to find the solution for the given linear equations.

#Developed by: v.charan sai

#RegisterNumber: 21003158

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("image1.png")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

## SOBEL EDGE DETETCTOR:
### SOBEL X:

sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL Y:

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL XY:

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()


## LAPLACIAN EDGE DETECTOR:

laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()


## CANNY EDGE DETECTOR:

canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()




```
## Output:
### SOBEL EDGE DETECTOR
### SOBEL X:
![output](https://github.com/21003698/Edge-Detection/blob/main/v1.jpg)

### SOBEL Y:
![output](https://github.com/21003698/Edge-Detection/blob/main/v2.jpg)
### SOBEL XY:
![output](https://github.com/21003698/Edge-Detection/blob/main/v3.jpg)
### LAPLACIAN EDGE DETECTOR
![output](https://github.com/21003698/Edge-Detection/blob/main/v4.jpg)



### CANNY EDGE DETECTOR

![output](https://github.com/21003698/Edge-Detection/blob/main/v5.jpg)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
