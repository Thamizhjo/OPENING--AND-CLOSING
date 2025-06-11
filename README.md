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
Developed by: THAMIZH KUMARAN S
RegisterNumber: 212223240166
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
cv2.putText(img, 'THAMIZH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
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

![Screenshot 2025-05-26 002711](https://github.com/user-attachments/assets/d16dd1cb-5886-4a23-aa25-f79aa7577a12)






### Display the result of Opening


![Screenshot 2025-05-26 002716](https://github.com/user-attachments/assets/a1d7f486-36f2-440b-9afd-901d9a8096f3)



### Display the result of Closing


![Screenshot 2025-05-26 002720](https://github.com/user-attachments/assets/2b058e51-b44f-4097-b931-a775644d9741)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
