# Traffic Sign Detection Using YOLOv8

## Overview

This project implements a Traffic Sign Detection System using the YOLOv8 object detection model. The system detects traffic signs from images and videos, making it suitable for intelligent transportation systems, autonomous driving research, road infrastructure monitoring, and traffic management applications.

The project leverages the Ultralytics YOLOv8 framework, OpenCV, and Python to provide accurate and efficient object detection capabilities.

---

## Features

- Detect traffic signs in static images.
- Process uploaded road videos for traffic sign detection.
- Draw bounding boxes around detected objects.
- Automatically save processed videos with detection results.
- Simple implementation using Google Colab.
- Fast inference using the lightweight YOLOv8 Nano model.
- Easy to customize and extend for additional traffic sign classes.

---

## Technologies Used

- Python
- YOLOv8 (Ultralytics)
- OpenCV
- Matplotlib
- Supervision Library
- Google Colab

---

## Project Workflow

1. Install the required dependencies.
2. Load a pre-trained YOLOv8 model.
3. Download and test a sample traffic sign image.
4. Perform object detection on the image.
5. Upload a custom road video.
6. Run YOLOv8 inference on the video.
7. Save the processed video with detection results.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/traffic-sign-and-vehicle-detection-yolov8.git

cd traffic-sign-and-vehicle-detection-yolov8
```

Install the required packages:

```bash
pip install ultralytics opencv-python-headless supervision matplotlib
```

Or install from the requirements file:

```bash
pip install -r requirements.txt
```

---

## Usage

### Load the YOLOv8 Model

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
```

### Detect Traffic Signs in an Image

```python
results = model("stop_sign.jpg")
results[0].show()
```

### Upload and Process a Video

```python
results = model.predict(
    "trafficVideo.mp4",
    save=True,
    conf=0.4,
    verbose=False
)
```

---

## Project Structure

```text
traffic-sign-and-vehicle-detection-yolov8/
│
├── README.md
├── requirements.txt
├── traffic_sign_detection.ipynb
│
├── sample_images/
│   └── stop_sign.jpg
│
├── sample_videos/
│   └── trafficVideo.mp4
│
├── outputs/
│   └── detected_video.mp4
│
└── LICENSE
```

---

## Sample Output

### Input

- Traffic sign images
- Road traffic videos

### Output

- Detected traffic signs with bounding boxes
- Annotated images
- Processed videos saved automatically

Output files are typically stored in:

```text
runs/detect/predict/
```

---

## Performance

The YOLOv8 Nano model offers:

| Metric | Description |
|----------|------------|
| Speed | Fast inference suitable for real-time applications |
| Accuracy | Strong baseline object detection performance |
| Model Size | Lightweight and resource-efficient |
| Deployment | Suitable for edge devices and cloud environments |

---

## Applications

- Intelligent Transportation Systems (ITS)
- Autonomous Vehicles
- Driver Assistance Systems (ADAS)
- Smart City Infrastructure
- Traffic Monitoring and Analysis
- Road Sign Inventory Management
- Transportation Research

---

## Future Improvements

- Train on dedicated traffic sign datasets such as GTSRB and TT100K.
- Improve detection accuracy with custom-trained models.
- Add traffic sign classification capabilities.
- Implement real-time webcam detection.
- Deploy as a web application using Flask or Streamlit.
- Integrate GPS tagging for road asset management.
- Support edge-device deployment for field applications.

---

## Author

**Maxwell Kwaku Nyarko**
