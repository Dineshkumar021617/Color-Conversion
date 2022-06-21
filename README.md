# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
### Step4:
Split and merge the image using cv2.split and cv2.merge commands.
### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By: Dineshkumar S
# Register Number: 212220230012
# i) Convert BGR and RGB to HSV and GRAY
import cv2
pic=cv2.imread('hot air baloon.jpg')
hsv=cv2.cvtColor(pic,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR_HSV',hsv)
hsv2=cv2.cvtColor(pic,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB_HSV',hsv2)
hsv3=cv2.cvtColor(pic,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR_GRAY',hsv3)
hsv4=cv2.cvtColor(pic,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB_GRAY',hsv4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR
hsv=cv2.cvtColor(pic,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV_IMAGE",hsv)
HSV_RGB=cv2.cvtColor(hsv,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV_RGB_IMAGE",HSV_RGB)
HSV_BGR=cv2.cvtColor(hsv,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR_IMAGE",HSV_BGR)
cv2.waitKey(0)

# iii)Convert RGB and BGR to YCrCb
ycrcb=cv2.cvtColor(color,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB_YCrCB',ycrcb)
ycrcb1=cv2.cvtColor(color,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR_YCrCB',ycrcb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image
blue=color[:,:,0]
green=color[:,:,1]
red=color[:,:,2]
cv2.merge((blue,green,red))
cv2.imshow("blue",blue)
cv2.imshow("green",green)
cv2.imshow("red",red)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image
hsv5=cv2.cvtColor(color,cv2.COLOR_BGR2HSV)
cv2.imshow("ORIGINAL HSV",hsv5)
h , s, v = cv2.split(hsv5)
cv2.imshow('h_plane',h)
cv2.imshow('s_plane',s)
cv2.imshow('v_plane',v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow('merged',mergedhsv)
cv2.waitKey(0)

```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (21)](https://user-images.githubusercontent.com/75234807/164191830-533ff8ad-2c2a-4408-8309-549f44f11533.png)

### ii) HSV to RGB and BGR
![Screenshot (22)](https://user-images.githubusercontent.com/75234807/165232773-e5eecf9e-187f-4065-a466-30840a800bfe.png)

### iii) RGB and BGR to YCrCb
![Screenshot (23)](https://user-images.githubusercontent.com/75234807/164192121-76226930-885f-4296-80fc-a71580f823ff.png)

### iv) Split and merge RGB Image
![Screenshot (24)](https://user-images.githubusercontent.com/75234807/164192162-33832ef0-ee99-46f3-898d-89f0975147a1.png)

### v) Split and merge HSV Image
![Screenshot (25)](https://user-images.githubusercontent.com/75234807/164192211-4f7b3a5d-b7f1-4fd9-8763-d9ede946a6cd.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
