# Driver Drowsiness Detection 
AI-powered real-time face and eye monitoring system

This project implements a **real-time driver drowsiness detection system** using a combination of:

- A **custom-trained face detection model** (TensorFlow + VGG16 backbone)
- **MediaPipe FaceMesh** for precise eye landmark tracking
- **EAR (Eye Aspect Ratio)** to detect eye closure
- **Live video processing** using OpenCV

The system triggers an alert when the driver’s eyes remain closed for a certain duration, helping prevent accidents caused by fatigue or microsleep.

---

## 🌟 Features

### ✅ **Custom Face Detection Model**
- Trained using TensorFlow & Keras  
- Uses VGG16 (without top layers)  
- Predicts:
  - Whether a face is present
  - The bounding box of the detected face

### ✅ **Eye Tracking with MediaPipe**
- Extracts 468 facial landmarks
- Uses specific indices for left and right eyelids  
- Calculates **EAR (Eye Aspect Ratio)** in real time

### ✅ **Drowsiness Detection**
- EAR < threshold → eyes likely closed  
- If eyes remain closed for **3 seconds**, the system triggers an alert  
- Works in real time at ~30 FPS depending on hardware

### ✅ **Live Webcam Monitoring**
- Draws bounding box around face  
- Displays EAR value  
- Shows alert text when conditions are met
