## NAME : M.suren.
## Date : 03/02/2026

# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By:  M.suren.
# Register Number: 212223230222

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('rose.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])



plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()

```
## Output:
<img width="292" height="263" alt="Screenshot 2026-02-05 114520" src="https://github.com/user-attachments/assets/71cc8798-5d45-4772-8c46-b6688e7f2918" />

<img width="191" height="254" alt="Screenshot 2026-02-05 114527" src="https://github.com/user-attachments/assets/e80ee0dc-ac22-4634-a1c6-e6211bbf7804" />

<img width="475" height="278" alt="Screenshot 2026-02-05 114548" src="https://github.com/user-attachments/assets/66ef692b-efec-4685-9980-9c1c11009647" />

<img width="430" height="284" alt="Screenshot 2026-02-05 114538" src="https://github.com/user-attachments/assets/25efb732-9749-4225-9fce-9f8e26d83d36" />


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
