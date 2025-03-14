# Computer Vision Projects: Face & Hand Tracking & OpenCV Drawing & Video cam & Template Matching with OpenCV

This repository contains multiple computer vision projects using OpenCV and cvzone. The two main projects included are:

1. **Face, Eye, and Smile Detection**
2. **Hand Tracking and Finger Distance Measurement**

## Features:
### Face, Eye, and Smile Detection
- Detects faces in video using Haar Cascade Classifiers
- Identifies eyes and smiles within detected faces
- Displays real-time video with rectangles marking detected features

### Hand Tracking and Finger Distance Measurement
- Detects hands in video using `cvzone.HandTrackingModule`
- Supports up to 2 hands simultaneously
- Measures the distance between the thumb (tip of finger 4) and the index finger (tip of finger 8)
- Displays real-time video with tracking and distance measurement overlay

## Prerequisites:
To run these programs, you need the following libraries:
- OpenCV
- NumPy
- cvzone (for hand tracking)

To install the required libraries, use the following command:
```bash
pip install opencv-python numpy cvzone
```

## How to Use:
### Running Face Detection:
1. Ensure that `haarcascade_frontalface_default.xml`, `haarcascade_eye.xml`, and `haarcascade_smile.xml` are in the same directory.
2. Run the script:
   ```bash
   python face_detection.py
   ```
3. The webcam feed will display detected faces, eyes, and smiles.
4. Press `Esc` to exit.

### Running Hand Tracking:
1. Ensure your webcam is connected.
2. Run the script:
   ```bash
   python hand_tracking.py
   ```
3. The webcam feed will display detected hands and measured finger distance.
4. Press `Esc` to exit.

## Project Structure:
```
.
├── face_detection.py
├── hand_tracking.py
├── haarcascade_frontalface_default.xml
├── haarcascade_eye.xml
├── haarcascade_smile.xml
```
- `face_detection.py`: Face, eye, and smile detection script.
- `hand_tracking.py`: Hand tracking and finger distance measurement script.
- `haarcascade_frontalface_default.xml`, `haarcascade_eye.xml`, `haarcascade_smile.xml`: Pre-trained models for face, eye, and smile detection.

## Code Explanation:
- **CascadeClassifier**: Detects faces, eyes, and smiles.
- **HandDetector**: Detects hands and landmarks using `cvzone.HandTrackingModule`.
- **findHands()**: Identifies hands in the video frame.
- **findDistance()**: Measures the distance between two given hand landmarks.
- **imshow()**: Displays the image or video in a separate window.

## References:
- [cvzone Documentation](https://github.com/cvzone/cvzone)
- [OpenCV Documentation](https://docs.opencv.org/4.x/)


# OpenCV Drawing Example

## Description
This project demonstrates how to use OpenCV to draw basic shapes and text on an image. The program reads an image, converts it to grayscale or keeps it in color, and then overlays various shapes such as lines, rectangles, circles, and polygons.

## Features
- Read an image (grayscale or color)
- Draw a line, rectangle, and circle
- Draw a polygon using predefined points
- Overlay text on the image
- Display the modified image using OpenCV

## Requirements
- Python 3.x
- OpenCV (`cv2`)
- NumPy

## Installation
```bash
pip install opencv-python numpy
```

## Usage
1. Place your image inside a folder (e.g., `Images/cityscape.jpg`).
2. Run the script:
   ```bash
   python script.py
   ```
3. Press `Esc` to close the displayed window.

## Code Overview
```python
import numpy as np
import cv2 as cv

# Read the image (color mode)
img = cv.imread("Images/cityscape.jpg", cv.IMREAD_COLOR)

# Draw shapes
cv.line(img, (5,5), (200,150), (0,0,255), 10)  # Red Line
cv.rectangle(img, (5,5), (200,150), (0,0,255), 8)  # Red Rectangle
cv.circle(img, (200,150), 50, (0,0,255), 20)  # Red Circle

# Draw a polygon
points = np.array([[30,5], [300,200],[100,70],[40,100]], np.int32)
cv.polylines(img, [points], True, (0,0,255), 5)  # Red Polygon

# Add text
font = cv.FONT_HERSHEY_SIMPLEX
cv.putText(img, 'Salam be hame', (20,50), font, 1, (0,0,255), 2, cv.LINE_AA)  # Red Text

# Show the image
cv.imshow('image', img)
cv.waitKey(0)
cv.destroyAllWindows()
```

## Notes
- Ensure the image path is correct.
- Change `IMREAD_COLOR` to `IMREAD_GRAYSCALE` if grayscale is needed.
- Modify shape colors if using grayscale (use a single intensity value like `255`).



## 📬 Contact
For any questions or collaborations, feel free to reach out:  

📧 Email: khalilinassim85@gmail.com 
🔗 GitHub: [YourGitHubProfile](https://github.com/Nasim-Khalili)  

---

**🚀 If you found this project useful, don't forget to star ⭐ the repository!**  
