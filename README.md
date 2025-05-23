# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Load the input image using cv2.imread().

### Step2:
Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().

### Step3:
Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.

### Step4:
Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.

### Step5:
Use plt.subplot() to show the original, opening, and closing images side by side.

 
## Program:
## NAME: Visveswarran Harikrishnan
## REGISTER NO: 212224110063
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Visveswarran Harikrishnan",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image


![WhatsApp Image 2025-05-22 at 21 43 37_7047aaca](https://github.com/user-attachments/assets/5a5521d7-f5d1-4b35-ab3e-afa61999f045)



### Display the result of Opening


![WhatsApp Image 2025-05-22 at 21 43 37_9e44f48f](https://github.com/user-attachments/assets/b651a7cb-b34e-4052-b233-d4e243061180)



### Display the result of Closing


![WhatsApp Image 2025-05-22 at 21 43 38_a05d3920](https://github.com/user-attachments/assets/5215ad72-fa06-4065-9d8c-97998939693b)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
