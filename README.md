# cable-profile-detection
# Non-contact Measurement of Cable Profile Using Deep Learning-Based Image Segmentation

**Course:** Introduction to Robotics, Sem 2, AY 25-26  
**Student:** Sanjeet Athawale  
**Roll No:** B22EE014  
**Department:** Electrical Engineering, IIT Jodhpur  

---

## Project Overview

Cable-driven robots use flexible cables that sag under gravity, causing positioning errors.
This project uses deep learning-based image segmentation to measure cable profiles
non-contactly from video frames, without any physical contact with the cable.

---

## Dataset

- Source: [CableDrivenRobotCableModel](https://github.com/RABKKK/CableDrivenRobotCableModel)
- Total videos: 26 `.avi` files across 5 camera positions (P1–P5)
- Data includes cable-driven robot footage with cables visible in cluttered backgrounds

---

## Work Done (Mid-term)

- Cloned and explored the dataset repository
- Extracted frames from video files using OpenCV
- Performed baseline edge detection using Canny algorithm
- Confirmed that traditional edge detection cannot isolate cables from background clutter
- This motivates the use of deep learning segmentation (next phase)

---

## Files

| File | Description |
|------|-------------|
| `cable_segmentation_midterm.ipynb` | Main Colab notebook with all code and outputs |

---

## Results (Baseline)

Canny edge detection was applied to extracted video frames.
While cable edges are detected, background clutter is also picked up,
confirming the limitation of classical methods and the need for deep learning.

---

## Planned Next Steps

- Train a U-Net / YOLO segmentation model on extracted frames
- Generate or annotate ground truth masks for cable regions
- Evaluate using IoU and pixel accuracy metrics
- Extract cable centerline profile from segmentation output

---

## References

1. R. A. Boby et al., "Measurement of end-effector pose errors and the cable profile of cable-driven robot using monocular camera," *Journal of Intelligent & Robotic Systems*, 2021.
2. R. Madaan et al., "Wire detection using synthetic data and dilated convolutional networks," *IEEE/RSJ IROS*, 2017.
3. R. Madaan et al., "Multi-view reconstruction of wires using a catenary model," *IEEE ICRA*, 2019.
