# Camera Calibration with OpenCV

This project provides a comprehensive workflow for camera calibration using OpenCV and Python. It detects chessboard corners in calibration images, computes the camera matrix and distortion coefficients, and demonstrates undistortion and pose estimation. The code is designed for use in Google Colab and supports batch processing of images.

---

## 📷 Overview

Camera calibration is essential for correcting lens distortion and determining the relationship between 3D real-world coordinates and their 2D projections in images. This project automates the calibration process using chessboard patterns and OpenCV’s calibration routines.

---

## 🛠️ Features

- **Batch Processing:** Automatically loads and processes all calibration images in a directory.
- **Flexible Chessboard Support:** Handles different chessboard sizes (e.g., 8x6, 8x4).
- **Corner Detection:** Uses `cv2.findChessboardCorners` and `cv2.cornerSubPix` for accurate corner localization.
- **Camera Calibration:** Computes camera matrix, distortion coefficients, rotation, and translation vectors.
- **Undistortion:** Demonstrates image undistortion using computed parameters.
- **Pose Estimation:** Estimates the camera’s pose relative to the chessboard and visualizes 3D axes projected onto the image.
- **Visualization:** Displays original and annotated images side by side in Colab using `cv2_imshow`.
- **Image Resizing:** Ensures images are resized for consistent processing and visualization.

---

## 📂 Project Structure

- **Calibration with 8x6 Chessboard:**  
  - Loads images containing "left" in the filename.
  - Detects corners, calibrates the camera, and undistorts a sample image.
  - Projects 3D axes to visualize pose estimation.

- **Calibration with 8x4 Chessboard:**  
  - Loads images containing "kaus" in the filename.
  - Repeats the calibration and visualization steps for the new chessboard size.

---

## 🚀 Getting Started

### 1. Environment Setup

- **Google Colab:**  
  The code is designed for Colab; it installs necessary packages and supports Colab-specific image display.
- **Dependencies:**  
  - Python 3.10
  - OpenCV
  - NumPy
  - Matplotlib
  - gdown (for downloading images from Google Drive)

### 2. Prepare Calibration Images

- Use printed chessboard patterns (e.g., 8x6 or 8x4 inner corners).
- Capture multiple images from different angles and distances.
- Place images in a Google Drive folder and update the `url` in the code to point to this folder.

### 3. Running the Code

- Upload the notebook or script to Colab.
- Update image paths if needed.
- Execute all cells to perform calibration, undistortion, and pose visualization.

---

## 📝 Key Steps

1. **Download Images:**  
   Uses `gdown` to fetch images from Google Drive.

2. **Detect Chessboard Corners:**  
   - Converts images to grayscale.
   - Detects corners using OpenCV functions.
   - Refines corner locations for accuracy.

3. **Calibrate Camera:**  
   - Computes camera matrix and distortion coefficients with `cv2.calibrateCamera`.
   - Saves and displays calibration results.

4. **Undistort Images:**  
   - Removes lens distortion using the computed parameters.
   - Saves and displays undistorted images.

5. **Estimate Pose and Visualize Axes:**  
   - Uses `cv2.solvePnP` for pose estimation.
   - Projects 3D axes onto images for visual verification.

---

## 📊 Example Outputs

- **calibresult.png:** Undistorted image after calibration.
- **calibresult1.png:** Undistorted image for the 8x4 chessboard.
- **Side-by-side images:** Original and annotated images with detected corners and projected axes.

---

## ⚠️ Notes

- Ensure the chessboard pattern matches the grid size specified in the code (e.g., (8, 6) or (8, 4)).
- Good calibration requires sharp images with the chessboard visible from various perspectives.
- The code resizes images for visualization; adjust sizes as needed for your dataset.

---

## 📚 References

- [OpenCV Camera Calibration Documentation](https://docs.opencv.org/master/dc/dbb/tutorial_py_calibration.html)
- [GammaCode: Camera Calibration Using OpenCV and Python][5]
- [Example Calibration Scripts on GitHub][2][3][4]

---

## 🤝 Contributing

Contributions, suggestions, and pull requests are welcome! Please ensure your code is well-documented and tested.

---

## 📝 License

This project is for educational and research purposes.

---

**Calibrate your camera, undistort your images, and unlock accurate computer vision!**

---[2][3][4][5]

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/27626270/0846e877-1428-4acd-8a88-dd2840a92afa/paste.txt
[2] https://github.com/paulmelis/opencv-camera-calibration
[3] https://github.com/tejakummarikuntla/camera-calibration-opencv
[4] https://github.com/tejakummarikuntla/camera-calibration-opencv/blob/master/README.md
[5] https://nikatsanka.github.io/camera-calibration-using-opencv-and-python.html
[6] https://github.com/chenmengdan/Camera-Calibration
[7] https://www.cba.mit.edu/leomcelroy/3d-scanning/-/blob/cd94e8e2047aef0d8d1c0aed070be8d813821cc3/README.md
[8] https://github.com/quanhua92/human-pose-estimation-opencv/blob/master/README.md
[9] https://github.com/AhmedSamara/OpenCV-camera-calibration/blob/master/calibrate_camera.cpp
[10] https://github.com/sreenithy/Camera-Calibration/blob/master/README.md
[11] https://learnopencv.com/deep-learning-based-human-pose-estimation-using-opencv-cpp-python/
[12] https://github.com/luckykk273/Camera-Calibration/blob/main/README.md
[13] https://github.com/KangLiao929/Awesome-Deep-Camera-Calibration/blob/main/README.md
[14] https://docs.opencv.org/4.x/d1/d0d/tutorial_js_pose_estimation.html
[15] https://github.com/Petros626/Camera-Calibration-with-PiCamera2-OpenCV/blob/main/README.md
[16] https://gitlab.com/VladyslavUsenko/basalt/-/blob/master/README.md
[17] https://answers.opencv.org/question/135672/calculate-odometry-from-camera-poses/
[18] https://github.com/anirudh1804/opencv/blob/main/README.md
[19] https://github.com/jagracar/OpenCV-python-tests/blob/master/OpenCV-tutorials/cameraCalibration/cameraCalibration.py
[20] https://gitlab.com/autowarefoundation/autoware.ai/utilities/blob/1f896834ddf57a549408ee1f6e988332bc372d28/autoware_camera_lidar_calibrator/README.md
[21] https://docs.ros.org/en/rolling/p/apriltag/standard_docs/README.html

---
Answer from Perplexity: pplx.ai/share
