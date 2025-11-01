# 🖐️ Hand Gestures Media Control

A real-time hand gesture recognition system that enables touchless media control using computer vision. Control your media playback, volume, and other functions with simple hand gestures captured through your webcam.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Supported Gestures](#supported-gestures)
- [How It Works](#how-it-works)
- [Requirements](#requirements)
- [Future Enhancements](#future-enhancements)

## 🎯 Overview

This project leverages **MediaPipe** for hand tracking and gesture detection to provide an intuitive, touchless interface for controlling media playback. The system recognizes various hand gestures in real-time and translates them into keyboard commands for media control.

## ✨ Features

- **Real-time Hand Tracking**: Uses MediaPipe's hand landmark detection for accurate tracking
- **Gesture Recognition**: Detects multiple hand gestures with high accuracy
- **Media Control**: Control play/pause, volume, and other media functions
- **Visual Feedback**: Displays hand landmarks and connections on the video feed
- **Low Latency**: Minimal delay between gesture and action
- **Easy to Use**: Simple webcam-based interface requiring no additional hardware

## 🛠️ Technology Stack

- **Python 3.x**
- **OpenCV**: For video capture and image processing
- **MediaPipe**: For hand landmark detection and tracking
- **NumPy**: For mathematical calculations and distance measurements
- **PyAutoGUI**: For simulating keyboard inputs

## 📦 Installation

### Prerequisites
- Python 3.7 or higher
- Webcam

### Steps

1. **Clone the repository**
git clone https://github.com/Jaideep193/-Hand_Gestures_.git
cd -Hand_Gestures_



2. **Install required dependencies**
pip install opencv-python mediapipe numpy pyautogui



Or use the requirements file (if available):
pip install -r requirements.txt



3. **Run the application**
python main.py



## 🚀 Usage

1. Run the `main.py` script
2. Allow camera access when prompted
3. Position your hand in front of the webcam
4. Perform gestures to control media playback
5. Press **'q'** to quit the application

## 🤚 Supported Gestures

| Gesture | Action | Description |
|---------|--------|-------------|
| 👍 **Thumbs Up** | Play | Thumb pointing upward triggers play/pause (Space key) |
| 👎 **Thumbs Down** | Stop | Thumb pointing downward stops playback |
| ☝️ **Forefinger Up** | Volume Up | Index finger raised increases volume |
| 👇 **Finger Down** | Volume Down | Index finger lowered decreases volume |
| ✋ **Full Palm** | Play/Pause | Open palm toggles play/pause (Space key) |
| ✌️ **Two Fingers Up** | - | Index and middle fingers raised (detected but no action assigned) |

## 🔍 How It Works

### 1. **Hand Detection**
- MediaPipe's hand landmark model detects 21 key points on the hand
- The system tracks finger tips, joints, and wrist position in real-time

### 2. **Gesture Recognition**
The `detect_gesture()` function analyzes hand landmarks to identify gestures:
- **Distance calculations**: Measures distances between finger tips and palm landmarks
- **Position analysis**: Compares y-coordinates to determine finger positions
- **Gesture classification**: Uses threshold-based logic to classify gestures

### 3. **Action Execution**
- Recognized gestures trigger PyAutoGUI keyboard commands
- Commands control media players and system volume
- Visual feedback shows detected landmarks on the video feed

### Algorithm Flow
Webcam Input → Hand Detection → Landmark Extraction → Distance Calculation → Gesture Classification → Action Execution


## 📋 Requirements

Create a `requirements.txt` file with:
opencv-python>=4.5.0
mediapipe>=0.8.0
numpy>=1.19.0
pyautogui>=0.9.50




## 🎮 Key Functions

### `detect_gesture(hand_landmarks)`
Analyzes hand landmarks to classify gestures based on:
- Finger tip positions relative to each other
- Distance between thumb and other fingers
- Overall hand orientation and palm width
- Vertical positions (y-coordinates) of finger tips

### Main Loop
- Captures video frames from webcam
- Processes frames with MediaPipe
- Draws hand landmarks for visual feedback
- Detects gestures and executes corresponding actions

## 🔧 Configuration

You can customize the gesture detection by modifying:
- **Distance thresholds**: Adjust sensitivity in the `detect_gesture()` function
- **Gesture mappings**: Change keyboard commands in the main loop
- **Camera source**: Modify `cv2.VideoCapture(0)` to use different camera

## 🚧 Future Enhancements

- [ ] Add more gesture types (swipe, pinch, rotate)
- [ ] Custom gesture training and recognition
- [ ] Multi-hand gesture support
- [ ] Gesture history and analytics
- [ ] GUI for gesture customization
- [ ] Support for multiple applications (browser, music player, video player)
- [ ] Gesture sensitivity adjustment
- [ ] Recording and playback of gesture sequences

## 🐛 Troubleshooting

**Camera not detected?**
- Check camera permissions
- Try changing camera index: `cv2.VideoCapture(1)` or `cv2.VideoCapture(2)`

**Gestures not recognized?**
- Ensure good lighting conditions
- Keep hand within camera frame
- Adjust distance from camera (recommended: 1-2 feet)

**High CPU usage?**
- Reduce camera resolution
- Lower frame processing rate


## 👨‍💻 Author

**Jaideep**
- GitHub: [@Jaideep193](https://github.com/Jaideep193)

---

⭐ **Star this repository if you find it helpful!**
