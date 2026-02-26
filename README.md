
# Hand Gesture Scrolling with Python

## Overview
This project enables scrolling on your computer using hand gestures detected from your webcam. It leverages OpenCV for video capture, MediaPipe for hand landmark detection, and PyAutoGUI for simulating scroll actions.

## Features
- Open palm: Scroll up
- Fist: Scroll down
- Real-time hand detection and gesture recognition
- Works with both left and right hands
- Adjustable scroll speed and delay

## Requirements
- Python 3.10 or higher
- opencv-python
- numpy
- mediapipe==0.10.5
- pyautogui

## Setup
1. Install dependencies:
   ```sh
   python -m pip install opencv-python numpy mediapipe==0.10.5 pyautogui
   ```
2. Run the script:
   ```sh
   python a1.py
   ```

## How It Works
The script uses MediaPipe to detect 21 hand landmarks. Gestures are recognized based on the position of finger tips and thumb relative to their base joints:
- **Open palm**: All fingers extended, triggers scroll up.
- **Fist**: All fingers folded, triggers scroll down.

### Hand Landmarks
MediaPipe identifies the following key points:
- Thumb: THUMB_TIP, THUMB_IP
- Fingers: INDEX_FINGER_TIP, MIDDLE_FINGER_TIP, RING_FINGER_TIP, PINKY_TIP

The script checks the y-coordinates of finger tips and thumb position to determine the gesture.

## Usage
- Start the script and show your hand to the webcam.
- Open palm will scroll up.
- Fist will scroll down.
- Press 'q' to quit.

### Customization
- Change `SCROLL_SPEED` and `SCROLL_DELAY` in `a1.py` to adjust scroll behavior.

## Troubleshooting
- Ensure your webcam is connected and accessible.
- If scrolling does not work, check that all dependencies are installed.
- Works best in well-lit environments for accurate hand detection.
- If you have multiple Python versions, use the correct executable (usually `python` on Windows).

## Example Images
You can add screenshots of the application window and hand gestures here for reference.

## Credits
- [OpenCV](https://opencv.org/)
- [MediaPipe](https://mediapipe.dev/)
- [PyAutoGUI](https://pyautogui.readthedocs.io/)

## License
MIT License