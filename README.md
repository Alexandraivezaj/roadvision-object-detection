# RoadVision – Real-Time Object Detection System

RoadVision is a computer vision application designed to detect and track roadway objects from live camera feeds and prerecorded video using YOLOv11.

The system combines real-time object detection, video processing, model training utilities, and a Python-based graphical user interface. It was developed as a collaborative Computer Science capstone project.

## Demo

RoadVision can process real-world driving footage and identify roadway objects in real time.

[▶ View RoadVision Demo](videos/test_driving_1_trimmed.mp4)

## Features

- Real-time roadway object detection
- Detection from live camera feeds
- Prerecorded video processing
- YOLOv11-based object detection
- Adjustable detection confidence threshold
- Configurable inference image size
- Graphical control panel for running inference
- Video recording of annotated detection output
- Dataset verification utilities
- Model training pipeline
- Camera detection utility

## Technologies

- Python
- YOLOv11
- OpenCV
- PyTorch
- Ultralytics YOLO
- Computer Vision
- ONNX

## Project Structure

```text
roadvision-object-detection/
│
├── UI/
│   └── control_panel.py
│
├── configs/
│
├── data/
│
├── live_feed_test/
│   ├── live_feed.py
│   └── live_predict.py
│
├── models/
│
├── src/
│   └── predict_video.py
│
├── tools/
│   ├── find_camera_id.py
│   ├── train_bdd.py
│   └── verify_dataset.py
│
├── videos/
│   └── test_driving_1_trimmed.mp4
│
├── config.json
├── requirements.txt
└── README.md
```

## Getting Started

### 1. Install Dependencies

Make sure Python is installed, then run:

```bash
pip install -r requirements.txt
```

### 2. Launch RoadVision

From the project root:

```bash
python UI/control_panel.py
```

### 3. Load a Model

From the RoadVision control panel:

1. Locate the **Model** section.
2. Click **Load .pt/.onnx**.
3. Select a compatible trained model.

Model weights are not included in this repository.

### 4. Select an Input Source

For a live camera, enter the appropriate camera index (commonly `0` or `1`).

To identify available cameras, run:

```bash
python tools/find_camera_id.py
```

For prerecorded footage, select a supported video file such as `.mp4`, `.mov`, `.avi`, or `.mkv`.

### 5. Run Object Detection

Click **START Video** to begin inference.

The interface allows the user to adjust settings such as:

- Detection confidence
- Inference image size
- Camera/video input
- Video recording

Recorded detection footage can be saved to the `videos/` directory.

## Team Project

RoadVision was developed collaboratively as a Computer Science capstone project.

### Contributors

- Alexandra Ivezaj — `Alexandraivezaj`
- Mark Georgi — `georgimark`
- Patrick Robin — `PatRobin02`
- William Kumpula — `wmkumpula`

The project provided hands-on experience with computer vision, object detection, model inference, Python development, and collaborative software development.

### 7. Stop Application
Click **STOP Video** to end the feed.

