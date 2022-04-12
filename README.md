# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### STEP 1: 
Read an image using imread() and Convert BGR and RGB to HSV and GRAY using: cv2.cvtColor(image,cv2.COLOR_RGB2HSV) cv2.cvtColor(image,cv2.COLOR_RGB2GRAY) cv2.cvtColor(image,cv2.COLOR_BGR2HSV) cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)

### STEP 2: 
Convert HSV to RGB and BGR using: cv2.cvtColor(image,cv2.COLOR_HSV2RGB) cv2.cvtColor(image,cv2.COLOR_HSV2BGR)

### STEP 3: 
Convert RGB and BGR to YCrCb using: cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb) cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)

### STEP 4:
Split and Merge RGB Image using: blue = image[:,:,0] green = image[:,:,1] red = image[:,:,2] cv2.merge((blue,green,red))

### STEP 5: 
Split and merge HSV Image using: hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV) h, s, v = cv2.split(hsv) cv2.merge((h,s,v))

## Program:
```python
# Developed By: Manoj Choudhary V
# Register Number:212221240025
# i) Convert BGR and RGB to HSV and GRAY
import cv2
image=cv2.imread("rgb.jpg")
cv2.imshow("ORIGINAL IMAGE",image)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB_HSV_IMAGE",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB_GRAY_IMAGE",RGB_GRAY)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR_HSV_IMAGE",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR_GRAY_IMAGE",BGR_GRAY)
cv2.waitKey(0)


# ii)Convert HSV to RGB and BGR

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV_IMAGE",hsv)
HSV_RGB=cv2.cvtColor(hsv,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV_RGB_IMAGE",HSV_RGB)
HSV_BGR=cv2.cvtColor(hsv,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR_IMAGE",HSV_BGR)
cv2.waitKey(0)


# iii)Convert RGB and BGR to YCrCb

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB_YCrCb_IMAGE",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCrCb_IMAGE",BGR_YCrCb)
cv2.waitKey(0)


# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("blue",blue)
green = image[:,:,1]
cv2.imshow("green",green)
red = image[:,:,2]
cv2.imshow("red",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("merged",merged)
cv2.waitKey(0)


# v) Split and merge HSV Image

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("ORIGINAL HSV_IMAGE",hsv)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow('merged',mergedhsv)
cv2.waitKey(0)
```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<br>

### ii) HSV to RGB and BGR
<br>
<br>

### iii) RGB and BGR to YCrCb
<br>
<br>

### iv) Split and merge RGB Image
<br>
<br>

### v) Split and merge HSV Image
<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
