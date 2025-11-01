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
- [Project Structure](#project-structure)
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
