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
Erode the image

### Step5:
Dilate the Image

 
## Program:

``` 
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'MANOJ',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/190d3d83-dcdb-4355-aef2-76db19f20a80)


### Display the Eroded Image

![image](https://github.com/user-attachments/assets/34dbb6fa-a883-4cee-97b1-2b002cd7f0cc)


### Display the Dilated Image

![image](https://github.com/user-attachments/assets/c70dfa6b-d714-47e7-a14b-b0d6d99bb54a)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
