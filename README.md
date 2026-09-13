# 🎨 Virtual Painter

A real-time virtual painting application built with Python and OpenCV that allows you to draw in the air using a colored pen or marker in front of a webcam.

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

The application captures live webcam frames and converts them from BGR to HSV color space for color-based segmentation. Predefined HSV ranges are used to isolate the supported marker colors.

Contours are detected from the resulting masks, and the position of the detected marker is tracked in real time. The tracked coordinates are then rendered as colored points on the webcam feed to create the virtual painting effect.

```text
Webcam Frame
     ↓
BGR → HSV
     ↓
Color Segmentation
     ↓
Contour Detection
     ↓
Marker Position Tracking
     ↓
Virtual Drawing
```

## 🛠️ Tech Stack

- Python
- OpenCV
- NumPy
- Computer Vision
- HSV Color Space
- Contour Detection

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- A working webcam

### Installation

Clone the repository:

```bash
git clone https://github.com/hetpatel4902/virtual-painter.git
cd virtual-painter
```

Install the required dependencies:

```bash
pip install opencv-python numpy
```

### Run the Application

```bash
python virtualPainter.py
```

The webcam window will open and the application will begin detecting the configured marker colors.

Hold a colored pen or marker in front of the webcam and move it through the camera frame to draw virtually.

Press `q` to exit the application.

## 🎨 Supported Colors

The application is configured to detect three marker colors:

- Pink
- Yellow
- Blue

The HSV thresholds and corresponding drawing colors can be modified in `virtualPainter.py`.

## ⚙️ Customization

Marker detection can be customized by modifying the HSV ranges in `virtualPainter.py`.

Additional colors can be supported by defining new HSV ranges and their corresponding drawing colors.

## 📁 Project Structure

```text
virtual-painter/
│
├── virtualPainter.py
└── README.md
```

## 📌 Project Background

Virtual Painter was developed as an early exploration of computer vision and real-time image processing using OpenCV.

The project demonstrates how webcam input, color segmentation, contour detection, and coordinate tracking can be combined to create an interactive computer-vision application.

## 🔮 Possible Improvements

- Add dynamic color calibration
- Add an eraser mode
- Add brush-size controls
- Add support for saving drawings
- Improve tracking stability under different lighting conditions
- Add a dedicated virtual canvas instead of drawing directly on the camera frame
