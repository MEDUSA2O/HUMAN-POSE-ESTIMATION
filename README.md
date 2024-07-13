# HUMAN-POSE-ESTIMATION
# Bicep Curl Counter Using Mediapipe and OpenCV

## Objective
- Develop a computer vision-based application to count bicep curls in real-time using a webcam.
- Use Mediapipe for pose estimation to detect key body landmarks.
- Implement a counter that increments with each completed bicep curl.

## Technologies Used
- **Python**: Programming language for scripting.
- **OpenCV**: Library for real-time computer vision.
- **Mediapipe**: Framework for building multimodal ML pipelines to detect human poses.
- **NumPy**: Library for numerical operations.

## Dependencies
- `opencv-python`
- `mediapipe`
- `numpy`

## Setup
Install necessary libraries using pip:
pip install opencv-python mediapipe numpy
## Key Components
- **Webcam Integration**: Capture video feed from the webcam.
- **Pose Detection**: Use Mediapipe to detect key landmarks on the body.
- **Angle Calculation**: Calculate the angle between shoulder, elbow, and wrist to determine the curl position.
- **Curl Counter Logic**: Implement logic to count a curl when the arm moves from a straight position to a bent position and back.

## Main Functions
- **calculate_angle(a, b, c)**:
  - Takes three points (shoulder, elbow, wrist) as input.
  - Calculates the angle between these points.
  - Returns the calculated angle.
- **main()**:
  - Initializes Mediapipe pose detection.
  - Captures video frames from the webcam.
  - Processes each frame to detect pose landmarks.
  - Calculates the angle of the elbow.
  - Implements the curl counting logic.
  - Displays the live video feed with landmarks and curl count.

## Workflow
- **Initialization**:
  - Import necessary libraries.
  - Define the `calculate_angle` function.
- **Pose Detection**:
  - Use Mediapipe to detect body landmarks in real-time.
  - Recolor frames for processing and display.
- **Angle Calculation**:
  - Calculate the angle between the shoulder, elbow, and wrist to monitor the bicep curl.
- **Curl Counter**:
  - Define the stages of a bicep curl ("up" and "down").
  - Increment the counter each time a full curl is completed.
- **Display**:
  - Draw landmarks and angles on the video feed.
  - Display the curl count and stage on the video feed.
- **Cleanup**:
  - Release the webcam and close OpenCV windows.

## Usage
1. Run the script in a Python environment with access to a webcam.
2. The application will start capturing video from the webcam.
3. Perform bicep curls in front of the webcam.
4. The application will display the live feed with pose landmarks, angles, and curl count.

## Potential Improvements
- Add support for counting curls on both arms.
- Improve the UI to display more detailed workout statistics.
- Integrate with fitness tracking apps or platforms.
- Enhance the accuracy of pose detection and angle calculation.

## Example Output
- Live video feed showing the user performing bicep curls.
- Pose landmarks drawn on the user's body.
- Real-time display of the angle between shoulder, elbow, and wrist.
- Curl counter incrementing with each completed curl.
