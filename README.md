# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the Image

### Step5:
Dilate the Image

``` 
## Program:
NAME: BALACHANDRAN
REGISTER NO: 212222100008
```
## Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


## Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'BALA',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


## Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


## Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



## Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![Screenshot 2024-05-08 004446](https://github.com/Balachandran143/erosion--dilation/assets/118886489/1021fba9-5938-4bb1-ab53-136b152e748b)

### Display the Eroded Image

![Screenshot 2024-05-08 004457](https://github.com/Balachandran143/erosion--dilation/assets/118886489/fc193a23-db6e-4bd6-b5c4-8a82d732d963)

### Display the Dilated Image
![Screenshot 2024-05-08 004505](https://github.com/Balachandran143/erosion--dilation/assets/118886489/b3162f02-4c1b-45e9-bed0-515b3c1578ac)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
