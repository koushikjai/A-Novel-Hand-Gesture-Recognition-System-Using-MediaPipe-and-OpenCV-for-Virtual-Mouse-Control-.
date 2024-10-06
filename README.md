
---
# Hand Gesture-Based Mouse Control Using OpenCV and MediaPipe

This project demonstrates a hand gesture-based mouse control system that uses a webcam feed to track hand movements. The index finger's position is used to control the mouse cursor on the screen, and the thumb-index distance is used to simulate mouse clicks. The system utilizes **OpenCV**, **MediaPipe**, and **PyAutoGUI** for real-time tracking and interaction.

## Features
- **Hand Tracking**: Tracks the user's hand using Mediapipe's Hand Landmark detection.
- **Mouse Movement**: Moves the mouse pointer based on the index finger's position.
- **Click Detection**: Simulates a mouse click when the index finger and thumb tips are brought close together.
- **Smooth Cursor Movement**: Exponential Moving Average (EMA) is applied to the cursor's position to smooth mouse movements for a better user experience.

## Requirements

To run this project, you need the following libraries installed in your Python environment:

- **OpenCV**: For real-time video capture and image processing
- **Mediapipe**: For hand landmark detection
- **PyAutoGUI**: For controlling the mouse cursor
- **Numpy**: For mathematical operations

You can install the dependencies using the following command:

```bash
pip install opencv-python mediapipe pyautogui numpy
```

## How to Run

1. Clone the repository to your local machine:

```bash
git clone https://github.com/your-username/gesture-based-mouse-control.git
```

2. Navigate to the project directory:

```bash
cd gesture-based-mouse-control
```

3. Run the Python script:

```bash
python gesture_mouse_control.py
```

4. The webcam will open, and your hand movements will start controlling the mouse cursor. Bringing the index finger and thumb close together will simulate a mouse click.

## Code Overview

- **Mediapipe Hand Tracking**: This is used to detect and track the hand landmarks in real time.
- **Index Finger Tip Detection**: The index finger's tip (landmark ID 8) is used to control the mouse cursor's position.
- **Click Detection**: The distance between the index finger and thumb tip is calculated, and if it falls below a certain threshold (30 pixels), a mouse click is triggered using PyAutoGUI.
- **Exponential Moving Average (EMA)**: This is applied to smooth the mouse's movement to prevent jittery behavior.

## Customization

- **Smoothing**: You can adjust the `smooth_factor` in the script to control the level of smoothing applied to the mouse movement.
- **Click Threshold**: You can modify the distance threshold (`30 pixels`) in the script to fine-tune the sensitivity of click detection.

## Demo

A short demo video/gif showcasing the system's functionality can be added here.

## Future Enhancements

- **Multi-Gesture Support**: Adding more gestures to support right-click, drag-and-drop, etc.
- **Hand Gesture-based Keyboard**: Implementing virtual keyboard functionality using hand gestures.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This README provides a clear overview of your project, installation instructions, and how it works. You can modify the details to suit your preferences before uploading it to your GitHub repo.
