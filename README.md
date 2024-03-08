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
    import cv2
    img=cv2.imread('pic.jpg',1)
    img=cv2.resize(img,(300,300))
    cv2.imshow('shan',img)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
<br>

![Screenshot 2024-02-28 230134](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/87273d17-934d-40be-baa9-ad2a94bc26e1)


![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/1cb82eaf-bc91-46e1-8946-875e629dcb85)

### ii)Write the image
    import cv2
    img=cv2.imread('pic.jpg',0)
    cv2.imwrite('demos.jpg',img)
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/1b74f853-a027-49b1-b150-f59328fb29ce)

<br>

### iii)Shape of the Image
    import cv2
    image=cv2.imread('pic.jpg',1)
    print(image.shape)
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/df551d8f-5684-42bd-9231-d1edabee81a8)

<br>

### iv)Access rows and columns
    import random
    import cv2
    image=cv2.imread('pic.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/1777a217-e5ee-4525-9025-352de38bb3b0)

<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/a5b0aca1-4a21-4fbd-85ce-fb8f3ed0fe5f)


### v)Cut and paste portion of image
import cv2
image=cv2.imread('pic.jpg',1)
image=cv2.resize(image,(300,300))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('image1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/2375c15e-588b-462b-bb71-e1715c3ebe7e)

<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/ce4ed0c8-b48a-489c-b096-91ec50cc020c)


### vi) BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('pic.jpg',1)
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
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/ebe8040b-3508-4780-bf76-435259a0a8eb)

<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/eca05949-ee65-4c39-a994-50f98765b3fb)


### vii) HSV to RGB and BGR
import cv2
img = cv2.imread('pic.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/d9655ba9-2f09-426a-b2b0-1c36992ec5ea)

<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/dfe21177-1327-45e8-a645-d30facc52af2)

### viii) RGB and BGR to YCrCb
import cv2
img = cv2.imread('pic.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
<br>


<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/a4f0f7de-5ea2-4741-8f23-7f2a8cc0b0f1)

### ix) Split and merge RGB Image
<br>
import cv2
img = cv2.imread('pic.jpg',1)
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
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/69a9f715-3f49-4477-8bfc-09d308a0ed77)

### x) Split and merge HSV Image
<br>
import cv2
img = cv2.imread("pic.jpg",1)
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
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/b9951810-1160-4cd2-b252-be17542f7251)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







