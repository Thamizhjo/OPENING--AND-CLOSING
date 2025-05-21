# EXP 10
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation. 
## Program:
```
DEVELOPED BY: Karsavarthan R R
REGISTER NO: 212223230100
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'KARSA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image



![Screenshot 2025-05-21 211944](https://github.com/user-attachments/assets/45f65ef6-c8f8-45d6-ba79-1ae5567d216b)



### Display the result of Opening


![Screenshot 2025-05-21 211950](https://github.com/user-attachments/assets/2b4e02d7-72df-47f6-a009-8ff276ff2133)



### Display the result of Closing

![Screenshot 2025-05-21 211955](https://github.com/user-attachments/assets/919c5c74-779d-4bb5-a7e6-809ac7e4f2e4)




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
