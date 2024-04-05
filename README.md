![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/e9f582a1-a172-4651-ae43-f518d5a1f988)# COLOR_CONVERSIONS_OF-IMAGE
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
### Developed By: S.Shanmathi
### Register Number: 212222100049


## Output:

### i) Read and display the image
        import cv2
        img=cv2.imread('pass.jpg',1)
        cv2.imshow('shan',img)
        cv2.waitKey(0)
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/d0216d8a-3c45-4c54-bf4b-6c54da247585)

### ii)Write the image
    import cv2
    img=cv2.imread('pass.jpg',0)
    cv2.imwrite('demos.jpg',img)
<br>

![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/1b74f853-a027-49b1-b150-f59328fb29ce)

<br>

### iii)Shape of the Image
    image=cv2.imread('pass.jpg',1)
    print(image.shape)
<br>

![Screenshot 2024-04-05 092259](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/8b579460-8f10-431f-b754-cb79165ef749)

<br>

### iv)Access rows and columns
    import random
    import cv2
    image=cv2.imread('pass.jpg',1)
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
        
![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/6180e834-d59e-4b50-a048-087875e44535)
        
<br>

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

![Screenshot 2024-04-05 093746](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/ef284bbc-13d1-4268-8a77-46d698d876dc)

<br>

### vi) BGR and RGB to HSV and GRAY
        img = cv2.imread('pass.jpg',1)
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
        
 ![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/4a9c2fd1-1e70-4b75-ba5a-58d1311de46c)
 ![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/5cce6484-8e4a-4684-86f2-095b17ea27ef)
        
        <br>

### vii) HSV to RGB and BGR
        img = cv2.imread('pass.jpg')
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
        
 ![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/b9f9b355-5e79-4738-a562-401434a263ad)
        
<br>

### viii) RGB and BGR to YCrCb
        import cv2
        img = cv2.imread('pass.jpg')
        img = cv2.resize(img,(200,200))
        cv2.imshow('Original RGB Image',img)
        
        YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
        cv2.imshow('RGB-2-YCrCb',YCrCb1)
        
        YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
        cv2.imshow('BGR-2-YCrCb',YCrCb2)
        
        cv2.waitKey(0)
        cv2.destroyAllWindows()
<br>
        
![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/fe01e8fa-9ec8-4c06-9684-3bfa862714e8)
        
<br>

### ix) Split and merge RGB Image
        <br>
        import cv2
        img = cv2.imread('pass.jpg',1)
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
![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/7b98ca2d-8af6-42d0-b06a-5107b004b14f)
        
<br>
        ### x) Split and merge HSV Image
        <br>
        import cv2
        img = cv2.imread("pass.jpg",1)
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
![image](https://github.com/ShanmathiShanmugam/COLOR_CONVERSIONS_OF-IMAGE/assets/121243595/7acee653-4922-4286-af44-730f6e43e638)
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







