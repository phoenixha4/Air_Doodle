# Air_Doodle
(This is one of my older projects, created as part of my journey to learn and explore the fascinating world of computer vision.)

We all have imagined being able to draw in the air just by moving your finger, right? This project introduces an Air Canvas, that lets you create drawings by simply moving your hand and tracking the landmarks on your knuckles. By leveraging the capabilities of OpenCV and MediaPipe, this tool transforms hand gestures into digital art.

### How It Works:
- **Video Capture**: The script uses OpenCV to capture live video from your webcam.
- **Frame Processing**: Each video frame is processed with MediaPipe to detect and track hand landmarks.
- **Landmark Drawing**: The detected hand landmarks are visualized on the video frames, effectively creating a virtual canvas for drawing in the air.

### Algorithm Overview:
1. **Frame Capture and Conversion**: The script reads video frames and converts them to the HSV color space, which simplifies color detection.
2. **Canvas Setup**: A canvas frame is prepared, and ink selection buttons are added to it.
3. **Hand Detection**: MediaPipe is configured to detect and track only one hand.
4. **Landmark Detection**: The RGB frame is passed to the MediaPipe hand detector to identify hand landmarks.
5. **Coordinate Tracking**: The coordinates of the forefinger are detected and stored in an array for consecutive frames, enabling the drawing of continuous lines.
6. **Drawing**: The points stored in the array are drawn on both the video frames and the canvas, creating the final drawing.

This project combines computer vision and hand gesture recognition to offer a unique and interactive drawing experience.