# OSS_TEST

**Crosswalk and Object Detection System**

A computer vision project that detects crosswalks, humans, and cars in images using YOLO and OpenCV, marking detected objects with bounding boxes.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Demo](#demo)
- [Technical Specifications](#technical-specifications)
- [References](#references)
- [License](#license)

## Features

- **Crosswalk Detection**: Identifies crosswalks in images using color masking and contour detection
- **Object Detection**: Detects humans and cars using YOLO v3
- **Bounding Box Visualization**: Draws red boxes around detected objects
- **Flexible Input**: Supports various image path configurations

## Prerequisites

Before running this project, ensure you have the following installed:

- **Python** 3.12.0 or higher - [Download Python](https://www.python.org/downloads/)
- **pip** (Python package manager)

### Required Python Packages

- `opencv-python` (4.8.1.78)
- `numpy` (1.26.2)

### Required YOLO Files

Download the following files and place them in your project directory:

1. **YOLOv3 Configuration**: [yolov3.cfg](https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg)
2. **COCO Names**: [coco.names](https://github.com/pjreddie/darknet/blob/master/data/coco.names)
3. **YOLOv3 Weights**: Download from the official YOLO website

## Installation

1. **Install Python dependencies**:
   ```bash
   pip install opencv-python==4.8.1.78 numpy==1.26.2
   ```

2. **Download YOLO files**:
   - Download `yolov3.cfg`, `coco.names`, and `yolov3.weights`
   - Place them in your project directory

3. **Prepare your images**:
   - Recommended image size: 1080 x 720 pixels
   - Supported format: JPG

## Usage

There are two ways to run the detection:

### Option 1: Image and source code in the same folder

```python
python detect_crosswalk_human_car('walk_people.jpg')
```

### Option 2: Separate image folder

```python
python detect_crosswalk_human_car('./image/walk_people.jpg')
```

## How It Works

The detection process follows these steps:

1. **Install Dependencies**: Set up Python, OpenCV, and NumPy
2. **Load Configuration**: Read YOLO configuration and COCO names files
3. **Read Image**: Load the input image
4. **Create Color Mask**: Generate a red color mask for crosswalk detection
5. **Find Contours**: Detect crosswalk contours using the color mask
6. **Draw Crosswalk Boxes**: If crosswalks are found, draw bounding boxes around them
7. **Detect Objects**: Use YOLO to detect humans and cars
8. **Merge Boxes**: Combine bounding boxes for detected objects
9. **Display Results**: Show the final image with all detected objects highlighted

## Demo

### Sample Output

![Crosswalk and Object Detection Demo](https://github.com/puzzlelzzup/OSS_TEST/assets/95035903/399e4aba-3968-49e9-8410-7833215e589d)

*The image shows detected crosswalks, humans, and cars with bounding boxes.*

## Technical Specifications

| Component | Version/Details |
|-----------|----------------|
| Python | 3.12.0 |
| OpenCV | 4.8.1.78 |
| NumPy | 1.26.2 |
| YOLO Version | v3 |
| Image Size | 1080 x 720 pixels |
| Detection Classes | Crosswalk, Human, Car |

## References

- [NumPy flatten documentation](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.flatten.html)
- [YOLOv3 Paper and Implementation](https://pjreddie.com/darknet/yolo/)
- [OpenCV Documentation](https://docs.opencv.org/)

### Image Attribution

Demo image by [Kireyonok_Yuliya](https://kr.freepik.com/free-photo/stylish-young-couple-posing-outdoors-a-young-man-with-a-bristle-in-a-cap-with-a-girl-with-long-hair-happy-young-people-are-walking-around-the-city-portrait-close-up_1210198.htm#page=3&query=%EA%B1%B0%EB%A6%AC%EB%A5%BC%20%EA%B1%B7%EB%8A%94%20%EC%82%AC%EB%9E%8C%EB%93%A4&position=25&from_view=keyword&track=ais&uuid=d327b96e-8d01-4496-9e12-678e18186db2) from Freepik

## License

Please ensure you comply with the licenses of all third-party components used in this project (YOLO, OpenCV, etc.).
