# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1: Read the Image

Load the input color image from a specified path.

### Step2: Convert to Grayscale

Transform the color image into a grayscale format for easier processing.

### Step3: Edge Detection

Apply an edge detection technique to identify the prominent edges in the grayscale image.

### Step4: Create Structuring Element

Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.

### Step5: Morphological Operations

Perform morphological operations:
Opening: Remove small objects from the edges to clean up the image.
Closing: Fill small holes in the detected edges to enhance the structure.

 
## Program:

#### Developed By: THAANESH.V
#### Register Number: 212223230228
``` 
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the structuring element

image = cv2.imread("001.jpg")  
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

```

### Use Opening operation

```
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```

### Use Closing Operation

```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```

## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/a2d1c32d-a2d2-44b4-ab01-f31fe26c198d)


### Display the result of Opening

![image](https://github.com/user-attachments/assets/6fb33831-ad6d-4ae5-a189-4ef4b5fb18f4)


### Display the result of Closing

![image](https://github.com/user-attachments/assets/db9e9bf8-a80f-4740-a5d4-22e51ce8065f)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
