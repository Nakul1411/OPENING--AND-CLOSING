# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation
### Step5:
Use Closing Operation

 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, "Kamesh", (5, 150), font, 3, (255), 5, cv2.LINE_AA)
cv2.imshow("Original", img)
cv2.waitKey(0)

# Create the structuring element
kernel_open = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
kernel_close = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))

# Use Opening operation
opened = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel_open)
cv2.imshow("Opening", opened)
cv2.waitKey(0)

# Use Closing Operation
closed = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel_close)
cv2.imshow("Closing", closed)
cv2.waitKey(0)
```
## Output:

### Display the input Image
<img width="502" height="232" alt="image" src="https://github.com/user-attachments/assets/6c52eee2-6147-4e23-b166-8f3c2e55279e" />


### Display the result of Opening
<img width="526" height="262" alt="image" src="https://github.com/user-attachments/assets/45e65c03-6521-40a6-9e5c-239b2d130a8f" />


### Display the result of Closing
<img width="553" height="222" alt="image" src="https://github.com/user-attachments/assets/0b526347-2c07-4466-8b03-d47ac86959ff" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
