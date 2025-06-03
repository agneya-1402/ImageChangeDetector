# ImageChangeDetector

## 🛰 Project Overview
This project aims to detect and highlight **major changes** between two ortho-rectified aerial images of the same location captured at different times. The goal is to:

- Precisely **align** the images,
- Correct for **environmental differences** like lighting and haze,
- **Detect and visualize** changes, and
- **Segment and classify** the detected changes.


## 📁 Files

- `change_detection_assignment.ipynb` – Main Colab Notebook with complete implementation.
- `A.png`, `B.png` – Input ortho-rectified images.
- `requirements.txt` – List of required Python libraries.
- `README.md` – Documentation (this file).


## 🧠 Approach

### 1. Image Alignment
- **ORB feature matching** was used to detect keypoints and descriptors.
- **Homography transformation** was applied to warp and align image B to image A for pixel-level comparison.

### 2. Environmental Correction
- Applied **histogram matching** to normalize lighting and contrast differences between the two images.

### 3. Change Detection
- Performed **image differencing** after alignment and normalization.
- Applied **Gaussian blur** and **thresholding** to isolate significant structural changes.
- Used **contour detection** to draw bounding boxes around changed regions.

### 4. Segmentation and Classification
- While simple visual segmentation was applied, advanced classification could be extended using semantic segmentation or ML-based classifiers (not included here due to scope).


## 📦 Requirements

```
opencv-python
scikit-image
matplotlib
numpy
```

## 📊 Results
Detected major changes such as vehicle movement, temporary structures, or crowd presence.
All detected changes are highlighted using red rectangles on the output image.

## 🔍 Future Scope
Integrate deep learning models (e.g., U-Net, Mask R-CNN) for semantic segmentation and change classification.
Improve robustness to seasonal changes using multispectral analysis.
Automate report generation and area-specific change quantification.

## 👤 Author
Agneya Pathare
Robotics | Computer Vision | AI

## 📄 License
This project is for evaluation and educational purposes under the assignment provided by Indrones Solutions Pvt. Ltd. Not intended for commercial use.
