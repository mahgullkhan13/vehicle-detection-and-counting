# Image and Signal Processing Projects

Python and Jupyter notebook coursework projects developed for the University of London BSc Computer Science Image and Signal Processing module.

## Projects

### 1. Vehicle detection, tracking and counting
- `vehicle-detection/vehicle_detection_tracking.ipynb`: motion detection using frame differencing, MOG2 background subtraction, ROI filtering, contours and centroid tracking.
- `vehicle-detection/vehicle_counting.ipynb`: tracks vehicles and counts first-time entries into a polygonal downtown zone.
- **Inputs needed:** `Traffic_Laramie_1.mp4`, `Traffic_Laramie_2.mp4` (not distributed).
- **Reported coursework results:** 1 and 3 counted vehicles, respectively; these are counts, not accuracy metrics.

### 2. Lossless audio compression with Rice coding
- `audio-rice-coding/rice_audio_compression.ipynb`: WAV handling, predictive residuals, zigzag mapping, Rice encoding and decoding.
- **Inputs needed:** `Sound1.wav`, `Sound2.wav` (not distributed).
- Coursework experiments compare K=2 and K=4; compression can be negative for unsuitable signals.

### 3. Automated video format validation and conversion
- `video-format-conversion/video_format_validator.ipynb`: ffprobe metadata inspection, specification validation, ffmpeg conversion and output revalidation.
- **Input needed:** `exercise3_files_isp.zip` (not distributed).
- Requires system `ffmpeg` and `ffprobe` executables.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt jupyter
jupyter notebook
```

Place authorized input media in the notebook working directory or update paths in the notebook. Some notebooks were developed in Colab and may require minor changes outside Colab.

## Limitations

These are educational prototypes, not production-ready systems. The original datasets are not included; the notebooks have not been retested end-to-end in a clean environment. Counting accuracy has not been independently benchmarked.
