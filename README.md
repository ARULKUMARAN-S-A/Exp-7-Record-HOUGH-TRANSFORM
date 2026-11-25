# Exp-7-Record-HOUGH-TRANSFORM
##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm & Explanation

##  Developed By

* **Name: ARUL KUMARAN S A**
* **Register No: 212224040030**

---


# Lane Detection Using OpenCV

## Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

---

## Step 2: Read the Image

```python
# Read the image using OpenCV

img = cv2.imread("road.jpg")
```

---

## Step 3: Convert to Grayscale

```python
# Convert to grayscale.

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```

---

## Step 4: Display Images

```python
plt.figure(figsize=(10,5))

plt.subplot(1,2,1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(gray, cmap="gray")
plt.title("Grayscale Image")
plt.axis("off")

plt.show()
```

---

## Step 5: Thresholding

```python
# Apply thresholding

threshold = cv2.threshold(gray, 150, 255, cv2.THRESH_BINARY)[1]
```

---

## Step 6: Region of Interest (ROI)

```python
# ROI masking already provided
# (Do not modify)
```

---

## Step 7: Edge Detection (Canny)

```python
# Perform Edge Detection

edges = cv2.Canny(roi, 50, 150)
```

---

## Step 8: Gaussian Blur

```python
# Apply Gaussian Blur

blur = cv2.GaussianBlur(edges, (5, 5), 0)
```

---

## Step 9: Hough Transform

```python
# Detect lines using Hough Transform

lines = cv2.HoughLinesP(
    blur,
    1,
    np.pi/180,
    50,
    minLineLength=50,
    maxLineGap=100
)
```

---

## Step 10: Lane Detection Logic

```python
# Already implemented
# (Do not modify)
```

---




---

##  Expected Output

* Original image
* Grayscale image
* Thresholded image
* ROI masked image
* Edge detected image
* Smoothed image
* Detected lines
* Final lane detection output

---

##  OUTPUT
<img width="750" height="846" alt="image" src="https://github.com/user-attachments/assets/f2d3bcb4-761f-4642-8333-d97b5a7fa572" />

<img width="406" height="830" alt="image" src="https://github.com/user-attachments/assets/90809f9a-4f7b-479b-8c98-3963ec78842d" />



<img width="456" height="317" alt="image" src="https://github.com/user-attachments/assets/c4f29a87-d5b5-422e-a288-b10143733ecd" />



---

## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---

