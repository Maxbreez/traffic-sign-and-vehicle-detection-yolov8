# Traffic Sign Detection Using YOLOv8
Overview

This project implements a real-time Traffic Sign Detection System using the YOLOv8 object detection model. The system is capable of detecting traffic signs from both images and videos, making it useful for intelligent transportation systems, road infrastructure monitoring, autonomous driving research, and traffic management applications.

The project utilizes the Ultralytics YOLOv8 framework along with OpenCV for image and video processing.

Features
Detect traffic signs in static images.
Process uploaded road videos for traffic sign detection.
Draw bounding boxes around detected objects.
Automatically save processed videos with detection results.
Simple implementation using Google Colab.
Fast inference using YOLOv8 Nano model (YOLOv8n).
Technologies Used
Python
YOLOv8 (Ultralytics)
OpenCV
Matplotlib
Google Colab
Supervision Library
Project Workflow
Install required dependencies.
Load a pre-trained YOLOv8 model.
Download and test a sample traffic sign image.
Perform object detection on the image.
Upload a custom road video.
Run YOLOv8 inference on the video.
Save the processed video with detected traffic signs.
Installation

Clone the repository:

git clone https://github.com/yourusername/traffic-sign-detection-yolov8.git

cd traffic-sign-detection-yolov8

Install required packages:

pip install ultralytics opencv-python-headless supervision matplotlib
Usage
Step 1: Load YOLOv8 Model
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
Step 2: Detect Traffic Signs in an Image
results = model("stop_sign.jpg")
results[0].show()
Step 3: Upload and Process a Video
results = model.predict(
    "road_video.mp4",
    save=True,
    conf=0.4,
    verbose=False
)
Project Structure
traffic-sign-detection-yolov8/
│
├── README.md
├── traffic_sign_detection.ipynb
├── stop_sign.jpg
│
├── runs/
│   └── detect/
│       └── predict/
│           └── output_video.mp4
│
└── requirements.txt
Sample Output
Input
Road traffic video
Traffic sign image
Output
Bounding boxes around detected traffic signs
Processed video saved automatically in:
runs/detect/predict/
Performance

The YOLOv8 Nano model provides:

Metric	Description
Speed	Fast inference suitable for real-time applications
Accuracy	Good baseline detection performance
Model Size	Lightweight and efficient
Deployment	Suitable for edge devices and cloud environments
Applications
Intelligent Transportation Systems (ITS)
Autonomous Vehicles
Driver Assistance Systems
Smart City Infrastructure
Traffic Monitoring and Analysis
Road Sign Inventory Management
Future Improvements
Train on dedicated traffic sign datasets such as GTSRB and TT100K.
Implement traffic sign classification after detection.
Add real-time webcam detection.
Deploy as a web application using Flask or Streamlit.
Improve detection performance under adverse weather and lighting conditions.
Integrate GPS tagging for road asset management.
Author

Maxwell Nyarko

Computer Science Graduate | Cybersecurity Enthusiast | Network Monitoring & AI Solutions Developer
