# Vehicle Detection and Traffic Counting System

A Python-based computer vision project developed as part of the Intelligent Signal Processing module for the University of London BSc Computer Science programme.

The project uses OpenCV and image processing techniques to detect, track, and count moving vehicles in recorded traffic footage, providing automated traffic flow analysis.

## Project Overview

The system processes traffic videos to identify moving vehicles, track their movement across frames, and count vehicles entering a predefined region of interest (ROI).

It combines motion detection, background subtraction, contour analysis, and centroid-based object tracking to monitor traffic activity.

## Key Features

- **Vehicle Detection:** Identifies moving vehicles using frame differencing and MOG2 background subtraction.
- **Object Tracking:** Tracks detected vehicles across consecutive frames using centroid-based tracking.
- **Region of Interest (ROI):** Filters detections to focus on designated areas of the road.
- **Vehicle Counting:** Counts unique vehicles entering a predefined polygonal downtown zone.
- **Traffic Flow Analysis:** Calculates vehicle counts and traffic flow rates.
- **Video Processing:** Uses OpenCV to process recorded traffic footage frame by frame.

## Technologies Used

- Python
- OpenCV
- NumPy
- Jupyter Notebook
- Computer Vision
- Image Processing

## Project Structure

```text
vehicle-detection-and-counting/
│
├── vehicle_detection_tracking.ipynb
├── vehicle_counting.ipynb
├── requirements.txt
└── README.md
```

### Notebook Descriptions

**1. vehicle_detection_tracking.ipynb**

Implements vehicle detection and tracking using frame differencing, MOG2 background subtraction, contour detection, ROI filtering, and centroid-based tracking.

**2. vehicle_counting.ipynb**

Implements vehicle tracking and counting, identifying unique vehicles entering a predefined polygonal zone and calculating traffic flow statistics.

## How It Works

1. **Video Input:** Loads recorded traffic footage.
2. **Frame Processing:** Processes individual video frames using OpenCV.
3. **Motion Detection:** Identifies moving objects through frame differencing and background subtraction.
4. **Object Detection:** Uses contours and filtering to identify potential vehicles.
5. **Vehicle Tracking:** Associates detected objects across frames using centroid tracking.
6. **Vehicle Counting:** Counts vehicles entering the designated region.
7. **Traffic Analysis:** Calculates vehicle counts and traffic flow rates.

## Results

The system was evaluated using two recorded traffic videos.

| Video | Vehicles Counted | Traffic Flow |
|---|---|---|
| Traffic_Laramie_1.mp4 | 1 | 0.50 vehicles/min |
| Traffic_Laramie_2.mp4 | 3 | 1.50 vehicles/min |

These results represent the vehicle counts reported during coursework testing, not independently benchmarked detection accuracy.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/mahgullkhan13/vehicle-detection-and-counting.git
cd vehicle-detection-and-counting
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
pip install jupyter
```

### 3. Prepare Video Files

The project uses the following traffic videos:

- `Traffic_Laramie_1.mp4`
- `Traffic_Laramie_2.mp4`

The original video files are not included in this repository.

Place authorised copies of the videos in the notebook's working directory, or update the video paths in the notebooks.

### 4. Run the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open either `vehicle_detection_tracking.ipynb` or `vehicle_counting.ipynb` and execute the cells in order.

Some notebook paths may require adjustment when running outside the original development environment.

## Limitations

- The system is designed for recorded traffic footage rather than real-time deployment.
- Detection performance may be affected by lighting, occlusion, and camera positioning.
- Vehicle counting accuracy has not been independently benchmarked.
- Original video datasets are not included.
- The notebooks have not been independently retested end-to-end in a clean environment.

## Future Improvements

- Integrate deep learning-based vehicle detection using YOLO.
- Improve object tracking using more advanced tracking algorithms.
- Add real-time traffic monitoring capabilities.
- Develop a dashboard for visualising traffic statistics.
- Evaluate detection and counting accuracy against manually annotated video data.

## Academic Context

Developed as part of the **BSc Computer Science – University of London**, Intelligent Signal Processing coursework.

The project demonstrates practical applications of computer vision, motion detection, object tracking, and automated traffic analysis.
