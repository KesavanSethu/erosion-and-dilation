## Ex9 -Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7

OpenCV
## Algorithm:
Step 1:
Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.

Step 2:
Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.

Step 3:
Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.

Step 4:
Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.

Step 5:
Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.

Step 6:
Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.

Step 7:
Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.

## Program Developed By:
# Name: KESAVAN S
# Register Number: 212224230121
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype="uint8")


text = "KESAVAN S"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

```
Output:
Display the input Image

<img width="686" height="547" alt="Screenshot 2026-05-26 160745" src="https://github.com/user-attachments/assets/5c189e74-324a-4769-9ab8-3567f741386e" />


Display the Eroded Image

<img width="677" height="542" alt="Screenshot 2026-05-26 160815" src="https://github.com/user-attachments/assets/b6c12784-7907-47c7-9e50-908af75c0d82" />


Display the Dilated Image

<img width="701" height="549" alt="Screenshot 2026-05-26 160832" src="https://github.com/user-attachments/assets/03dd2009-06ea-4407-8cd6-b5af6fc4e14c" />




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
