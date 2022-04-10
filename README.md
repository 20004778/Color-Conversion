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
Split and merge the image using cv2.split and cv2.merge commands

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By: SURYA R
# Register Number: 212220230052
# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('cap vs tony.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('cap vs tony.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('cap vs tony.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('cap vs tony.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('cap vs tony.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (206)](https://user-images.githubusercontent.com/75236145/162630159-5ce2d9a0-fdbf-442d-9d94-e5794bc7bf41.png)
![Screenshot (207)](https://user-images.githubusercontent.com/75236145/162630199-c0ca91db-d441-4612-97e9-c6ab8e42b797.png)

### ii) HSV to RGB and BGR
![Screenshot (208)](https://user-images.githubusercontent.com/75236145/162630188-67255561-e5e3-46ba-ad64-93260b2f169f.png)
![Screenshot (209)](https://user-images.githubusercontent.com/75236145/162630192-b0e7ed93-9b0d-4d2d-a676-745811cd0c3b.png)

### iii) RGB and BGR to YCrCb
![Screenshot (210)](https://user-images.githubusercontent.com/75236145/162630207-4b564f06-6dfd-43e8-9554-ffedc3f95b34.png)
![Screenshot (211)](https://user-images.githubusercontent.com/75236145/162630209-ba43ad12-5567-4af3-a3fa-0f52241521de.png)

### iv) Split and merge RGB Image
![Screenshot (212)](https://user-images.githubusercontent.com/75236145/162630214-d15a1775-f97b-4234-890c-a7e5ab974b26.png)
![Screenshot (213)](https://user-images.githubusercontent.com/75236145/162630237-6d35f400-28fa-4602-903b-c488702903a2.png)
![Screenshot (214)](https://user-images.githubusercontent.com/75236145/162630243-75fe2f5b-7be2-4424-bf4d-7aa8a0e685c4.png)

### v) Split and merge HSV Image
![Screenshot (215)](https://user-images.githubusercontent.com/75236145/162630253-0b772fe8-ca78-42a5-97c1-e726b3e6fa33.png)
![Screenshot (217)](https://user-images.githubusercontent.com/75236145/162630256-c8cce0fd-c5ee-4555-8f61-3e675fbd0375.png)
![Screenshot (218)](https://user-images.githubusercontent.com/75236145/162630262-bd905d28-6cd9-440c-84c9-ac39f01a5328.png)
![Screenshot (216)](https://user-images.githubusercontent.com/75236145/162630254-0c4ad61c-7577-4415-83b9-87e87fa1f44d.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
