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

## Programs
## Developed by : Sri Varshan P
## Reg.No. 212222240104

### Original Image

![SampleColor](https://github.com/PSriVarshan/EDGE-DETECTION/assets/114944059/9e6c4210-9abc-430a-8d14-5acedf1670f3)


### Convert image to grayscale and remove noise

```py
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("SampleColor.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```py
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
**SOBEL Y AXIS :**
```py
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
**SOBEL XY AXIS :**
```py
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
### LAPLACIAN EDGE DETECTOR
```py
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
### CANNY EDGE DETECTOR
```py
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
#### Sobel X Axis Edge Detection

![image](https://github.com/PSriVarshan/EDGE-DETECTION/assets/114944059/42fac950-9bbe-487b-93ce-bc5db5ff9b98)

#### Sobel Y Sxis Edge Detection 

![image](https://github.com/PSriVarshan/EDGE-DETECTION/assets/114944059/312d60a5-5580-451b-a706-c20254a743d1)


#### Sobel XY Sxis Edge Detection 

![image](https://github.com/PSriVarshan/EDGE-DETECTION/assets/114944059/27563b1a-abb1-4d00-b584-c44fd9d06d70)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/PSriVarshan/EDGE-DETECTION/assets/114944059/e5fb0986-e77f-444f-8b19-9dfe07758acf)


### CANNY EDGE DETECTOR

![image](https://github.com/PSriVarshan/EDGE-DETECTION/assets/114944059/2c415f61-6cf3-4bd7-a1d1-06991b0954de)

## Result:
### Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
