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

![Screenshot 2024-09-07 222036](https://github.com/user-attachments/assets/9ef8fe3b-6d65-4d90-b3e5-250fc326ab3b)


![Screenshot 2024-09-07 222023](https://github.com/user-attachments/assets/83995c36-1e6b-43b9-8822-af50b86c7e25)


![Screenshot 2024-09-07 222010](https://github.com/user-attachments/assets/748a8902-5f91-4ece-bd58-dc8882c36e7c)


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

![Screenshot 2024-09-07 222225](https://github.com/user-attachments/assets/221add10-d40b-4aa7-9396-85ff2df1f111)


![Screenshot 2024-09-07 222236](https://github.com/user-attachments/assets/b98c27fa-9b77-4f70-bc45-9db8f6594eed)


![Screenshot 2024-09-07 222255](https://github.com/user-attachments/assets/c543d382-cfb3-49e8-9016-996253b5911e)


<br>
<br>

### ix) Split and merge RGB Image

```
img = cv2.imread('subashini nptel image.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:

![Screenshot 2024-09-07 222435](https://github.com/user-attachments/assets/19b2cc4f-476e-4474-a3a3-15bfe0a0c8fd)

![Screenshot 2024-09-07 222447](https://github.com/user-attachments/assets/6cbe2f40-7aed-41fe-8df8-1e99858bf9ed)


![Screenshot 2024-09-07 222553](https://github.com/user-attachments/assets/df48a44d-6f2d-4b82-b43c-81c87ba7cc4d)

![Screenshot 2024-09-07 222516](https://github.com/user-attachments/assets/9fbedbf6-54a7-48af-b123-94722c898e1e)

<br>
<br>

### x) Split and merge HSV Image
```
img = cv2.imread("subashini nptel image.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:


![Screenshot 2024-09-07 222716](https://github.com/user-attachments/assets/01544e7e-dcf0-425a-aabb-a3245ad10b91)

![Screenshot 2024-09-07 222706](https://github.com/user-attachments/assets/7f6e8cd3-f599-4fb2-b317-89925209ddd5)

![Screenshot 2024-09-07 222659](https://github.com/user-attachments/assets/b5e5e67c-eddb-43b8-97eb-89fb682902ed)


![Screenshot 2024-09-07 222650](https://github.com/user-attachments/assets/e4144f0e-e569-4e22-80b6-16df3115c34d)

<br>
<br>

# Result:

Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







