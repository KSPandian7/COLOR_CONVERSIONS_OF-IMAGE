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

### PROGRAM:
```py
DEVELOPED BY: KULASEKARAPANDIAN K
REGISTER NO: 212222240052
```


## OUTPUT :

### i) Read and display the image
```py
import cv2
image = cv2.imread('sampledip.jpg',1)
image=cv2.resize(image,(400,350))
cv2.imshow('KSP',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![OUTPUT](/output1.png)
<br>
<br>

### ii)Write the image
```py
import cv2
image=cv2.imread('TEMPLEksp.jpg',0)
cv2.imwrite('dipt.jpg',image)
```
### OUTPUT:
![OUTPUT](/OOP2.png)

<br>
<br>

### iii)Shape of the Image
```py
import cv2
image=cv2.imread('TEMPLEksp.jpg',1)
print(image.shape)
```
### OUTPUT:
![OUTPUT](/output3.png)

<br>
<br>

### iv)Access rows and columns
```py
import random
import cv2
image=cv2.imread('TEMPLEksp.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (90,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('IMAGE',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![OUTPUT](/oop4.png)

<br>
<br>

### v)Cut and paste portion of image

```py
import cv2
image = cv2.imread('TEMPLEksp.jpg', 1)
image = cv2.resize(image, (400, 350))
tag = image[90:200, 50:160]
image[50:160, 90:200] = tag
cv2.imshow('CUT & PASTE', image)

cv2.waitKey(0)
cv2.destroyAllWindows()

```

### OUTPUT:
![OUTPUT](/cut.png)
<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```py
img = cv2.imread('TEMPLEksp.jpg',1)
img = cv2.resize(image,(400,400))

cv2.imshow('RESULTS',img)


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
![OUTPUT](/cc.png)
<br>
<br>

### vii) HSV to RGB and BGR

```py

import cv2
img = cv2.imread('TEMPLEksp.jpg')
img = cv2.resize(img,(400,400))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Og HSV Img',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()

```

### OUTPUT:
![OUTPUT](/hsv2.png)


<br>
<br>

### viii) RGB and BGR to YCrCb

```py
import cv2
img = cv2.imread('TEMPLEksp.jpg')
img = cv2.resize(img,(400,300))
cv2.imshow('Og RGB Img',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![OUTPUT](/ycrcb.png)

<br>
<br>

### ix) Split and merge RGB Image
```py
import cv2
img = cv2.imread('TEMPLEksp.jpg', 1)
img = cv2.resize(img, (300, 300))

R = img[:, :, 2]
G = img[:, :, 1]
B = img[:, :, 0]

cv2.imshow('R-Channel', R)
cv2.imshow('G-Channel', G)
cv2.imshow('B-Channel', B)

merged = cv2.merge((B, G, R))
cv2.imshow('Merged RGB image', merged)

cv2.waitKey(0)
cv2.destroyAllWindows()

```

### OUTPUT:
![OUTPUT](/merge.png)
<br>
<br>

### x) Split and merge HSV Image
```py
import cv2
img = cv2.imread("TEMPLEksp.jpg",1)
img = cv2.resize(img,(300,300))
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

### OUTPUT:
![OUTPUT](/mergehsv.png)


<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







