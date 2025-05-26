# PCA-Mini-Project---Face-Detection-or-Convert-an-image-into-gray-scale-image-using-CUD
Mini Project - Face Detection or Convert an image into gray scale image using CUDA GPU programming
## AIM:
The aim of this project is to demonstrate how to convert an image to grayscale using CPU-based programming with OpenCV.

## Procedure:
1.Load the input image using OpenCV’s imread function.
2.Check if the image was loaded successfully.
3.Convert the input image from RGB to grayscale using OpenCV’s cvtColor function.
4.Display the grayscale image using Google Colab’s cv2_imshow function.
5.Save the grayscale image using OpenCV’s imwrite function.
6.Clean up resources (handled automatically by Python’s garbage collection).

## Program :
```colab
import cv2
from google.colab.patches import cv2_imshow
import sys
import os

# Verify image exists
if not os.path.exists('jinsakai.jpg'):
    print("Error: jinsakai.jpg not found in the current directory.")
    print("Current directory contents:", os.listdir())
    sys.exit()

# Load the image
image = cv2.imread('jinsakai.jpg')

# Check if image loading was successful
if image is None:
    print("Error: Unable to load jinsakai.jpg. Check file format and path.")
    sys.exit()

# Convert the image to grayscale
grayscale_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Display the grayscale image
cv2_imshow(grayscale_image)

# Save the grayscale image
try:
    cv2.imwrite('grayscale_jinsakai.jpg', grayscale_image)
    print("Grayscale image saved as grayscale_jinsakai.jpg")
except Exception as e:
    print("Error saving image:", str(e))
```

## Input and Output Image :
![jinsakai](https://github.com/user-attachments/assets/4932b704-9c74-496d-a7fe-ac58f85f053b)


## Result :
The program converts input.jpg to grayscale using OpenCV’s cvtColor function.The original and grayscale images are displayed, and the grayscale image is saved as grayscale_output.jpg.
