# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages

### Step 2:
Create the Text using cv2.putText

### Step 3:
Create the structuring element

### Step 4:
Use Opening operation

### Step 5:
Use Closing Operation

### Step 6:
end the program

## Program:

``` 
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,'LAKSHMI PRIYA',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)
```
## Output:

### Display the input Image
![11 1](https://user-images.githubusercontent.com/93427923/171792903-be3b0d0b-21f4-48dc-9b6b-4564126ea0f8.png)

### Display the result of Opening
![11 2](https://user-images.githubusercontent.com/93427923/171792920-7fe755ae-fe7a-4aa6-8158-26e43820da7e.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/93427923/171792940-aff3ec1b-e5a0-41ef-a90a-3d483da89e39.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
