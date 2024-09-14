# Experiment-01: COLOR_CONVERSIONS_OF-IMAGE
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


## Program:
### Developed By: Ashwin Akash M
### Register Number: 212223230024


## Output:
### i)Read and Display an Image
#### Load the image from your local directory and display it
```
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('Dip.jpg')
plt.imshow(image)
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/86db199e-6e2b-4ad4-82a8-6e3de223c37f)

### ii)Draw Shapes and Add Text
#### Draw a line from top-left to bottom-right of the image
```
res=cv2.line(image,(0,0),(500,500),(100,50,105),10)
plt.imshow(res)
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/2b636d10-6a3f-47a5-ae7b-b251b5fa00e1)
#### Draw a circle at the center of the image
```
image=cv2.imread('Dip.jpg')
res=cv2.circle(image,(250,250),150,(255,0,0),10)
plt.imshow(res)
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/4d9593d3-8761-4ac6-ae03-9df6be524e82)
#### Draw a rectangle aronud a specific region of interest in the image
```
img=cv2.imread('Dip.jpg')
start=(100,100)
stop=(400,400)
color=(200,255,245)
thickness=10
res=cv2.rectangle(img,start,stop,color,thickness)
plt.imshow(res)
plt.show()
```
![image](https://github.com/user-attachments/assets/b544def0-3408-4e26-909b-bd42a55e5e71)
#### Add the text "OpenCV Drawing" at the top-left corner of the image
```
imt = cv2.imread("creative.jpeg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
font_scale = 1
color = (55, 155, 255) 
thickness = 4
rest = cv2.putText(imt, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
plt.imshow(rest)
plt.show()
```
![image](https://github.com/user-attachments/assets/101e4640-81c7-45bc-8536-6e4bd6d2ebc3)

### iii)Image Color Conversion
#### Convert the image from RGB to HSV and display it
```
image = cv2.imread("creative.jpeg")
img_hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
plt.imshow(img_hsv)
plt.show()
```
![image](https://github.com/user-attachments/assets/24540070-0a00-4ecc-8318-537550dc6a91)
#### Convert the image from RGB to GRAY and display it
```
image = cv2.imread("creative.jpeg")
img_gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(img_gray)
plt.show()
```
![image](https://github.com/user-attachments/assets/8c77c907-d311-4024-a2af-f4e5c2791a71)
#### Convert the image from HSV to RGB and display it
```
img_gray = cv2.cvtColor(image, cv2.COLOR_HSV2RGB)
plt.imshow(img_gray)
plt.show()
```
![image](https://github.com/user-attachments/assets/60b6443f-2234-4332-95ca-2273380c9e9a)


### iv)Access and Manipulate Image Pixels
#### Access And Print The Value Of The Pixel At Coordinate (100,100)
```
image=cv2.imread('creative1.jpeg')
pixel=image[100,100]
pixel
```
![image](https://github.com/user-attachments/assets/b65ee6ea-cad1-4a60-af50-9d05eac7ad90)
#### Modify The Color Of The Pixel At (200,200) to White
```
image=cv2.imread('Dip.jpg')
for i in range(100,200):
    for j in range(100,200):
        image[i,j]=225
for i in range(100,250):
    for j in range(100,250):
        image[i,j]=225
plt.imshow(image,cmap="gray")
plt.show()
```
![image](https://github.com/user-attachments/assets/45ffc6d5-9e20-4f34-9ec7-da5f90c713e3)

### v)Image Resizing
#### Resize The Orginial Image To Half Of Its Size And Display It
```
image=cv2.imread('Dip.jpg')
image.shape
```
![image](https://github.com/user-attachments/assets/e6d0acb9-5dc7-495d-8be5-002b619d5f5d)
```
image_resize=cv2.resize(image,(250,250))
image_resize.shape
```
![image](https://github.com/user-attachments/assets/b574599c-1792-4a6e-b6a6-bbb5012a5f1c)

### vi)Image Cropping
#### Crop A Region Of Interest (ROI) From The Image And Display It
```
image=cv2.imread('Dip.jpg')
Re=image[0:250,0:250]
cv2.imwrite('Re.jpg',Re)
```
![image](https://github.com/user-attachments/assets/6c9b9e33-f9a5-4b38-9ff6-26921f880402)
```
plt.imshow(Re)
plt.show()
```
![image](https://github.com/user-attachments/assets/fd588f16-d850-4c91-8b5c-e7bf90860826)

### vii)Image Flipping
#### Flip The Orginal Image Horizontally And Display It
```
img1=cv2.imread('Dip.jpg')
img2=cv2.imread('Dip1.jpg')
himage=cv2.hconcat([img1,img2])
plt.imshow(himage)
plt.show()
```
![image](https://github.com/user-attachments/assets/9591dcba-d784-42a4-8a32-13d58bfe8527)
#### Flip The Orginal Image Vertically And Display It
```
img1=cv2.imread('Dip.jpg')
img2=cv2.imread('Dip1.jpg')
vimage=cv2.vconcat([img1,img2])
plt.imshow(vimage)
plt.show()
```
![image](https://github.com/user-attachments/assets/693b68d4-c798-4603-96ad-233a2401a3aa)

### viii)Write and Save the Modified Image

#### Save The Final Modified Image To Your Local Directory
```
image=cv2.imread('Re.jpg')
plt.imshow(image)
```
![image](https://github.com/user-attachments/assets/519a6f41-ecf1-4b63-9478-e962bd51ff97)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







