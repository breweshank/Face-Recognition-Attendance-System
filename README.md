# Face Recognition Attendance System

## Overview
This project is a face recognition-based attendance system that uses a webcam to detect faces and mark attendance in a CSV file. It uses the `face_recognition` and `OpenCV` libraries to process images and recognize faces.

## Features
- Loads images from a specified folder and encodes faces.
- Captures video from a webcam and detects faces in real time.
- Matches detected faces with known faces and marks attendance.
- Stores attendance data in a CSV file with timestamps.

## Requirements
Ensure you have the following dependencies installed before running the script:

### Python Libraries
- `opencv-python`
- `numpy`
- `face-recognition`
- `pandas`

To install the required libraries, run:
```sh
pip install opencv-python numpy face-recognition pandas
```

## Folder Structure
```
Face_Recognition_Attendance/
│-- attendance/              # Stores Attendance.csv
│-- images/                  # Folder containing known images
│-- face_recognition.py      # Main script
```

## Usage

### Step 1: Prepare Image Data
- Place images of known individuals in the specified folder (default: `C:\Users\ESHANK\Downloads\College\Image`).
- Image file names should correspond to the person's name (e.g., `John_Doe.jpg`).

### Step 2: Run the Script
Execute the following command:
```sh
python face_recognition.py
```

### Step 3: Webcam Face Detection
- The webcam will open and start detecting faces.
- If a face matches a known image, the person's name is displayed on the screen and attendance is recorded.
- Press `q` to exit.

## Attendance Output
The attendance record is stored in `attendance/Attendance.csv`, containing:
```
Name, Time
John Doe, 14:30:12
Jane Smith, 14:32:45
```

## Troubleshooting
- **No face found in images?** Ensure images have clear, front-facing faces.
- **Webcam not working?** Check the webcam index (`cv2.VideoCapture(0)`) and ensure it is connected.
- **Face not recognized?** Try adding more training images with varied lighting and angles.

## License
This project is licensed under the MIT License and contact for modification and distribution.

