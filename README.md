# COMP0137-Machine-Vision-CW2
---

- Final Grade: 92/100
- Comments:
  - A) Great! B) Great! C) Great!
  - D) You do mention that the estimation is not perfect however you need to elaborate on the "error" you mention. E) Good! F) Good!
  - G) You do not comment on how the MAP lags behind during increased movements
  - H) You do show the frames, however you also show the ones fro.the previous exercise causing issues with running all the code.

---

# Homography and Condensation Tracking Project

Welcome to the **Homography and Condensation Tracking Project** repository. This project explores advanced techniques in **computer vision**, specifically **homography estimation** and **condensation tracking (particle filtering)**, using Python and OpenCV.

---

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Experiments and Results](#experiments-and-results)

---

## Overview

This project covers the following topics:

- **Homography Estimation:** Computing the perspective transformation between two images.
- **Feature Matching & RANSAC:** Extracting key points and computing robust correspondences.
- **Condensation Algorithm (Particle Filtering):** A probabilistic approach to object tracking.
- **Kalman Filtering:** Tracking objects through sequences of images with state estimation.

The repository consists of Jupyter notebooks that demonstrate theoretical concepts, practical implementations, and experimental results.

---

## Project Structure

The repository consists of several practical exercises and labs:

### Homography Estimation and Feature Matching
- **`HW2_TrackingAndHomographies.ipynb`**  
  *This notebook covers homography estimation using SIFT feature matching and RANSAC filtering. It demonstrates how to compute transformations between two image planes and apply perspective warping.*

- **`practical1A.ipynb` & `practical1B.ipynb`**  
  *Introduces feature detection using SIFT and SURF, and computes homographies between two images. These notebooks also cover matching key points across frames.*

### Particle Filtering and Condensation Algorithm
- **`HW2_Practical7c.ipynb`**  
  *This notebook implements the condensation algorithm (particle filtering) for object tracking. It explores probabilistic tracking in dynamic environments.*

- **`labA.ipynb` & `labB.ipynb`**  
  *Discusses theoretical foundations and implementations of particle filtering for robust tracking under occlusions and noise.*

### Kalman Filtering for Object Tracking
- **`practical2A.ipynb` & `practical2B.ipynb`**  
  *Explores the Kalman filter for object tracking, highlighting the prediction and correction phases.*

---

## Getting Started

### 1. Install Dependencies:
   - Required Python libraries: `numpy`, `scipy`, `matplotlib`, `opencv-python`, `pillow`, `jupyter`, etc.

### 2. Run the Notebook/Scripts:
   - Open Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Follow the notebook sections (e.g., Homography, Tracking, Kalman Filter) to see how data is loaded, processed, and analyzed.

---

## Usage

1. **Running the Notebooks:**  
   Open any `.ipynb` file using Jupyter Notebook or Jupyter Lab.
   
2. **Homography Estimation:**
   - Load two images with a shared overlapping region.
   - Detect features using **SIFT/SURF**.
   - Match key points using **FLANN-based matcher**.
   - Estimate the **homography matrix** using **RANSAC**.
   - Warp images to align perspectives.

3. **Condensation Tracking (Particle Filtering):**
   - Initialize a set of **particles** to represent different possible object positions.
   - Update particle positions based on a motion model.
   - Measure similarity between particles and observed features.
   - Resample particles based on likelihood.

4. **Kalman Filtering:**
   - Use a **linear dynamic model** to predict an object's next position.
   - Correct the predicted state with observations.
   - Track objects through occlusions.

---

## Experiments and Results

### **Homography Estimation**
- **Goal:** Align images using homography.
- **Findings:**
  - SIFT and SURF features provided robust key point detection.
  - RANSAC filtering improved homography estimation by removing outliers.
  - Warping was effective for image alignment.

### **Condensation Algorithm (Particle Filtering)**
- **Goal:** Track objects in noisy environments.
- **Findings:**
  - The particle filter handled non-linear motion well.
  - It performed better than Kalman filtering in cases of occlusion.
  - More particles improved tracking accuracy but increased computation time.

### **Kalman Filtering**
- **Goal:** Smooth object tracking with predictive filtering.
- **Findings:**
  - Performed well for linear motion with Gaussian noise.
  - Struggled with sudden motion changes compared to the particle filter.
  - Less computationally expensive than condensation tracking.

---

**Project Maintainer:**  
Chung-Yu Wei


