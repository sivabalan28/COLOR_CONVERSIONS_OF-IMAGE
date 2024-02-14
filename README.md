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
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```py
    import cv2
    image=cv2.imread('imgr.jpg',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('SIVABALAN',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-14 233707](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/067733bf-638b-419b-85bd-6a26f56b7ed5)

  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```py
    import cv2
    image=cv2.imread('imgr.jpg',0)
    cv2.imwrite('a.jpg',image)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-14 233740](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/f6b9d03f-eb89-4e12-af1f-b66882d192a8)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```P
    import cv2
    image=cv2.imread('imgr.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-14 234251](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/3325407e-1d96-4ccd-94e1-7a1ac6c63d0e)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```py
    import random
    import cv2
    image=cv2.imread('imgr.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (400,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:
![Screenshot 2024-02-15 000338](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/5d386e22-1a32-42e1-ae47-568cbce78315)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
   import cv2
   image=cv2.imread('imgr.jpg',1)
   image=cv2.resize(image,(300,300))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('image1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![Screenshot 2024-02-14 234427](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/9c27fd25-17b2-4cb1-98e6-2e86316f4e27)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('imgr.jpg',1)
img = cv2.resize(img,(200,200))
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
![Screenshot 2024-02-14 234738](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/783fdc32-e3b0-4e08-bacd-124a9b126a17)


### vii) HSV to RGB and BGR
```py
import cv2
img = cv2.imread('imgr.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-02-14 234859](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/cd4e7127-e06b-4961-b7f8-a5904cbca088)


### viii) RGB and BGR to YCrCb
```py
import cv2
img = cv2.imread('imgr.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-02-14 235023](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/34b4a3c3-983a-47ca-bedf-c9d6028448b4)

### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('imgr.jpg',1)
img = cv2.resize(img,(200,200))

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

### OUTPUT:
![Screenshot 2024-02-14 235157](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/0741fd20-5d46-4e99-aa19-4e3120044b27)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("imgr.jpg",1)
img = cv2.resize(img,(200,200))
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
![Screenshot 2024-02-14 235330](https://github.com/sivabalan28/COLOR_CONVERSIONS_OF-IMAGE/assets/113497347/02e27b58-16f2-4b77-81cd-d2cc79a0f108)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







