# CANNY-EDGE-DETECTION
# CANNY-EDGE-DETECTION

## Aim:

To perform Canny edge detection algorithm and obtain the edges with different parameter settings.

## Software Required:

Anaconda - Python 3.7

## Algorithm:
### Step1:
To perform edge detection using Canny edge detectors.

### Step2:
For performing edge detection on a image.

Canny :
canny_edges=cv2.Canny(gray,50,150)

For different parameters :

i) Low thresholds (detects more edges, including noise) :
canny_edges1 = cv2.Canny(blurred, 30, 80)

ii) Balanced thresholds (good trade-off) :
canny_edges2 = cv2.Canny(blurred, 50, 100)

iii)High thresholds (detects only strong edges) :
canny_edges3 = cv2.Canny(blurred, 100, 200)

### Step3:
Display all the images with their respective edge detected images.

## Program :
#### Name : Bhuvaneshwaran H
#### Reg No: 212223240018
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('wb.jpg') 
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
blurred = cv2.GaussianBlur(gray, (5, 5), 1.4)
canny_edges = cv2.Canny(gray, 50, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.title('Original Image')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 2)
plt.title('Canny Edge Detection')
plt.imshow(canny_edges, cmap='gray')
plt.axis('off')
plt.show()
# Apply Canny with different threshold settings
# Low thresholds (detects more edges, including noise)
canny_edges1 = cv2.Canny(blurred, 30, 80)
plt.figure(figsize=(8, 8))
plt.subplot(2, 2, 2)
plt.title('Canny (Low Thresholds: 30-80)')
plt.imshow(canny_edges1, cmap='gray')
plt.axis('off')

plt.show()
# Balanced thresholds (good trade-off)
canny_edges2= cv2.Canny(blurred, 50, 100)
plt.figure(figsize=(8, 8))
plt.subplot(2, 2, 3)
plt.title('Canny (Balanced Thresholds: 50-100)')
plt.imshow(canny_edges2, cmap='gray')
plt.axis('off')

plt.show()
# High thresholds (detects only strong edges)
canny_edges3 = cv2.Canny(blurred, 100, 200)
plt.figure(figsize=(8,8))
plt.subplot(2, 2, 4)
plt.title('Canny (High Thresholds: 100-200)')
plt.imshow(canny_edges3, cmap='gray')
plt.axis('off')

plt.tight_layout()
plt.show()
```
## Output:

#### Original Image:

![download](https://github.com/user-attachments/assets/65612df9-ed16-41c5-9b07-ef5843a58b6d)

#### Canny Edge Detection:

![download](https://github.com/user-attachments/assets/5a6a54cd-cdbf-4c69-ba2f-c68f1dc42bd5)

#### Canny (Low Thresholds: 30-80):

![download](https://github.com/user-attachments/assets/9bae14a2-8078-4320-9bdb-981a7f6904ff)

#### Canny (Balanced Thresholds: 50-100):

![download](https://github.com/user-attachments/assets/39ec2f53-c4ea-424a-bdf5-af6b31667e3b)

#### Canny (High Thresholds: 100-200):

![download](https://github.com/user-attachments/assets/42a54d7c-53e7-4b28-893a-db2fa90adc54)

## Result:

Thus , the edges are detected by Canny edge detection and also implemented with different parameter settings.












