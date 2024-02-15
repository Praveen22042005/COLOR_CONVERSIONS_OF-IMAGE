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
</td>
  <td>
    
### OUTPUT:
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/b932447d-5145-40a4-a9b1-867fc1e13b91)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/472665a3-0ac6-4ca9-9063-d75f68857bc7)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/c55d6fe3-722f-444d-8c56-4fbc5cda4917)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/4fcf7e77-6753-4bda-9b59-678940bc4b5d)
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/90be3e77-b45f-4138-b9c2-a27e45a211f9)

</td>
  </tr>
</table>


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('green.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2_imshow(img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2_imshow(RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2_imshow(BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/961fdb4e-89ba-4906-bbc7-e4a17791e03b)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/c7bdf89c-bbdf-405b-b67f-c486e80b7efc)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/3ed6fb47-bea0-45e6-8656-341e8c0555ff)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('green.jpg')
img = cv2.resize(img,(300,200))
cv2_imshow(img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2_imshow(YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2_imshow(YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/8d56cc2d-b28f-4e74-b33f-947747c1f57e)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/88225a0f-e1ff-43fd-8a97-0ca131465e6a)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/83331b9b-6437-47be-8965-766e04f700f5)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('green.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2_imshow(R)
cv2_imshow(G)
cv2_imshow(B)
merged = cv2.merge((B,G,R))
cv2_imshow(merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/dedba354-6127-44ee-b634-621d228021fc)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/e26c68cd-d4a9-4386-b2f2-ccf1f626260e)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/446dedaa-1254-4e70-9b99-debe6d02e760)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/acee5f86-7aba-43d5-a926-f7b9925dacda)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("green.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2_imshow(H)
cv2_imshow(S)
cv2_imshow(V)
merged = cv2.merge((H,S,V))
cv2_imshow(merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/f5fa65d8-eaa8-405b-94ae-561a02896e30)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/04e45194-b2bc-4392-a9a4-44b1e40a520a)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/f79fdde4-7fdb-46a4-b999-d319770935eb)

![image](https://github.com/Praveen22042005/COLOR_CONVERSIONS_OF-IMAGE/assets/112475766/50ed647c-f112-42b4-8670-a4266a3ab240)





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







