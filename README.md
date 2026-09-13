# Virtual Painter 🎨

A real-time virtual painting application built with Python and OpenCV that lets you draw in the air using a colored pen or marker in front of a webcam.

The application detects the marker based on its color, tracks its position in real time, and renders the detected movement as a virtual drawing on the video feed.

## ✨ Features

- Real-time webcam-based tracking
- Color-based object detection using HSV color space
- Detection of multiple marker colors
- Contour-based object localization
- Real-time virtual drawing
- Adjustable camera resolution
- Simple keyboard control to exit the application

## 🧠 How It Works

The application processes each frame captured from the webcam through the following pipeline:

Webcam Frame
     ↓
BGR → HSV Conversion
     ↓
Color Range Filtering
     ↓
Binary Mask
     ↓
Contour Detection
     ↓
Marker Position Detection
     ↓
Coordinate Tracking
     ↓
Virtual Drawing
