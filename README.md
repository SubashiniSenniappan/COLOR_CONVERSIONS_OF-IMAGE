# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By:SUBASHINI S
### Register Number: 212222240106




i) Read and display the image

```
import cv2
image=cv2.imread('subashini nptel image.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('Subashini S',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i)Read and Display an Image


![Screenshot 2024-09-07 221542](https://github.com/user-attachments/assets/667d3ae3-5a44-456d-82ff-3ee0f0cbe8ce)

<br>
<br>

### ii)Write the image

```
 cv2.imwrite('b.jpg',image)
```
## OUTPUT:
![Screenshot 2024-09-07 224247](https://github.com/user-attachments/assets/ae60011e-f611-4cf1-a68f-e6a86c1f0450)

<br>
<br>

### iii)Shape of the Image

```
print(image.shape)
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/c5fea788-3e48-415c-b2c1-9a1e5f123108)

<br>
<br>

### iv)Access rows and columns

```
import random
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('suba-1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:

![Screenshot 2024-09-07 221607](https://github.com/user-attachments/assets/c7178e32-e443-4842-8648-b19dc76705f9)

<br>
<br>

### v)Cut and paste portion of image

```
image=cv2.imread('subashini nptel image.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('suba-2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
  
![Screenshot 2024-09-07 221626](https://github.com/user-attachments/assets/16b24aad-0ce6-4de6-97f2-cae3eb79a458)

<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```
img = cv2.imread('subashini nptel image.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.
COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## OUTPUT:


![Screenshot 2024-09-07 221741](https://github.com/user-attachments/assets/378eddb0-bd43-4c3f-99e6-d82eb956053b)

![Screenshot 2024-09-07 221812](https://github.com/user-attachments/assets/d0433d95-ba10-4e72-969e-1ca6103aa80f)

![Screenshot 2024-09-07 221830](https://github.com/user-attachments/assets/4a5216bb-0a2e-4efe-ae95-f223e45fbdb0)

![Screenshot 2024-09-07 221839](https://github.com/user-attachments/assets/565218c9-1e43-458b-ac05-be84095329f8)

![Screenshot 2024-09-07 225448](https://github.com/user-attachments/assets/0438e98f-8dab-44a1-bc7e-cb445ca8476c)

<br>
<br>

### vii) HSV to RGB and BGR

```
img = cv2.imread('subashini nptel image.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:


![Screenshot 2024-09-07 222036](https://github.com/user-attachments/assets/968276a2-44d0-4d66-b575-d68cb0f5974c)

![Screenshot 2024-09-07 222023](https://github.com/user-attachments/assets/99b1679b-14fa-4847-9c58-6ac805724f1f)

![Screenshot 2024-09-07 222010](https://github.com/user-attachments/assets/50bb40fd-db9f-4d4e-9e7b-df7e0cd45685)

<br>
<br>

### viii) RGB and BGR to YCrCb:

```
img = cv2.imread('subashini nptel image.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:



![Screenshot 2024-09-07 222236](https://github.com/user-attachments/assets/f787abed-44c0-4a13-9c29-4b9eb90c0127)

![Screenshot 2024-09-07 222255](https://github.com/user-attachments/assets/e769259c-b523-41db-b874-8ba530e1565a)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







