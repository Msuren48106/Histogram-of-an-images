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

image = cv2.imread('rose.jpeg')
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
<img width="321" height="264" alt="Screenshot 2026-02-12 101949" src="https://github.com/user-attachments/assets/7f6fb9c6-8718-4b85-b006-7c43c234c0fd" />
<img width="210" height="269" alt="Screenshot 2026-02-12 101954" src="https://github.com/user-attachments/assets/efc3e606-c971-415f-bef8-f5b9bf034bcc" />
<img width="416" height="302" alt="Screenshot 2026-02-12 102000" src="https://github.com/user-attachments/assets/0bd3e021-5ccb-4f90-9e37-b36e82490431" />
<img width="523" height="292" alt="Screenshot 2026-02-12 102022" src="https://github.com/user-attachments/assets/3bb096ad-f3a3-4bcc-8107-8fd6824f001b" />



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
