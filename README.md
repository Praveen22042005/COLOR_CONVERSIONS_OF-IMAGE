# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: Praveen BV
### Register Number: 212222100036


## Output:

<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('green.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Praveen BV',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>
    
### OUTPUT:

![green](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/ab94fba7-ee06-4b17-a9c9-608037050f38)
  </td>
  </tr>
 
   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('green.jpg',0)
    cv2.imwrite('d.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![out](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/429b314c-793e-4689-9a22-7b5b86f5cec6)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('green.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![out 1](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/3502d9cf-0e59-4839-a360-fbfd913bb458)

  </td>
  </tr>
  <tr>
    <td>

### iv)Access rows and columns
```Python
   !pip install google-colab
from google.colab.patches import cv2_imshow
import random
import cv2
image=cv2.imread('green.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
  for j in range(image.shape[1]):
    image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)] 
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

 ![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/57b80586-c2c5-4d30-bddc-32f9afb7b001)


  </td>
  </tr>
  <tr>
    <td width=50%>

### v)Cut and paste portion of image

 ```Python
    !pip install google-colab
from google.colab.patches import cv2_imshow
import cv2
import numpy as np
image=cv2.imread('green.jpg',1)
image = cv2.resize(image, (400, 400))
print(image.shape)
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/4ab42df1-7869-4057-813e-2f36573a40ef)


  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('green.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/b932447d-5145-40a4-a9b1-867fc1e13b91)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/472665a3-0ac6-4ca9-9063-d75f68857bc7)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/c55d6fe3-722f-444d-8c56-4fbc5cda4917)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/4fcf7e77-6753-4bda-9b59-678940bc4b5d)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/90be3e77-b45f-4138-b9c2-a27e45a211f9)



### vii) HSV to RGB and BGR
<br>
<br>

### viii) RGB and BGR to YCrCb
<br>
<br>

### ix) Split and merge RGB Image
<br>
<br>

### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







