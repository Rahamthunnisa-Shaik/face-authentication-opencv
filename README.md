# Face-Based Authentication System (OpenCV)

A simple biometric authentication prototype built using Python and OpenCV.
This project demonstrates how facial data can be used to verify identity by comparing a live camera feed with a stored reference image.

## Overview

This system captures a user's face through a webcam, stores it as a reference, and performs real-time comparison to determine whether access should be granted or denied.

It is designed as a **learning project** to explore core concepts in biometric authentication and computer vision.

## Features

* Real-time face detection using Haar Cascade
* Automatic face registration (first detected face)
* Live face comparison using pixel difference
* Access control:

  * Access Granted (matching face)
  * Access Denied (non-matching face)
  * Lightweight and runs without heavy ML dependencies

## Tech Stack

* Python
* OpenCV
* NumPy

## ⚙️ How It Works

1. The webcam captures video input.
2. Faces are detected using OpenCV’s Haar Cascade classifier.
3. The first detected face is stored as a reference (registration phase).
4. Each new frame is compared with the stored face:

   * Faces are resized and converted to grayscale
   * Pixel-wise difference is computed
   * A threshold determines match vs non-match
5. Based on the comparison:

   * Low difference → Access Granted
   * High difference → Access Denied

## Installation & Usage

### 1. Clone the repository

```bash
git clone https://github.com/your-username/face-authentication-opencv.git
cd face-authentication-opencv
```

### 2. Install dependencies

```bash
pip install opencv-python numpy
```

### 3. Run the project

```bash
python main.py
```

### 4. Usage

* Sit in front of the camera
* The system will automatically register your face
* Stay in frame for authentication results

## Limitations

This is a basic prototype and has several limitations:

* Sensitive to lighting conditions
* Can be affected by pose variations
* No anti-spoofing (photos/videos may bypass system)
* Uses simple pixel comparison instead of advanced models
* Supports only a single registered user

## 🔮 Future Improvements

* Integrate deep learning-based face recognition
* Add multi-user support with identity labels
* Implement anti-spoofing mechanisms
* Improve accuracy under varying lighting conditions
* Build a GUI for better user interaction

## Learning Outcomes

* Understanding of biometric authentication concepts
* Hands-on experience with OpenCV
* Real-time image processing and face detection
* Trade-offs between simplicity and security
 
## Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

## License

This project is open-source and available under the MIT License.

## 👩‍💻 Author

Ayesha Parveen
Feel free to connect or reach out!

---
