# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
For performing edge detection on a image.

 ## Sobel
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5) sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5) sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)

## Laplacian
lap=cv2.Laplacian(gray,cv2.CV_64F)

## Canny
canny=cv2.Canny(gray,120,150)

### Step3:

Display all the images with their respective edge detected images.
 
## Program:
```python
Developed by: Lokesh N
Register no : 212222100023
```

# Import the packages
```python
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```python
img=cv2.imread("tiger.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR
## SOBEL X AXIS :

```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```

## SOBEL Y AXIS :
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY AXIS:

```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```


## LAPLACIAN EDGE DETECTOR
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

## CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```



## Output:
### SOBEL EDGE DETECTOR
## SOBEL X AXIS :
![Screenshot from 2023-10-04 13-55-33](https://github.com/lokeshnarayanan/EDGEDETECTION/assets/119393019/bf4b39e0-906e-42f4-b855-7572fbe37ef9)

## SOBEL Y AXIS :
![Screenshot from 2023-10-04 13-55-22](https://github.com/lokeshnarayanan/EDGEDETECTION/assets/119393019/420a33d9-70ec-4dde-9882-b61048a7445c)


## SOBEL XY AXIS :
![Screenshot from 2023-10-04 13-55-13](https://github.com/lokeshnarayanan/EDGEDETECTION/assets/119393019/82cbe01d-cfa0-4a2b-95f4-8f542e351dc7)



### LAPLACIAN EDGE DETECTOR
![Screenshot from 2023-10-04 13-54-58](https://github.com/lokeshnarayanan/EDGEDETECTION/assets/119393019/08c2fc8b-5ff2-4baa-9eb4-14789acce897)



### CANNY EDGE DETECTOR
![Screenshot from 2023-10-04 13-54-46](https://github.com/lokeshnarayanan/EDGEDETECTION/assets/119393019/0f1166a6-f35a-48c4-b92b-d29a9add3474)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
