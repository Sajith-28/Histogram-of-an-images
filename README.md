# Histogram-of-an-images
# NAME : # SAJITH AHAMED F
# REG NO :212223240144
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
# Developed By:  SAJITH AHAMED F
# Register Number: 212223240144

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('iron.jpg')

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
<img width="535" height="184" alt="image" src="https://github.com/user-attachments/assets/a33e71d2-ee5a-4dbb-87b1-2e9ffcc7d2f9" />
<img width="366" height="247" alt="image" src="https://github.com/user-attachments/assets/f425bffb-dffa-4dfc-9370-149d97945ac8" />
<img width="255" height="77" alt="image" src="https://github.com/user-attachments/assets/ec6ac8cf-4184-4219-930a-8ae0f8fde2f7" />
<img width="325" height="251" alt="image" src="https://github.com/user-attachments/assets/e0676934-c1be-465c-a8f3-d2c9eaa1790b" />


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
