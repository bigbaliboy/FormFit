# FormFit

FormFit is a prototype application designed to detect and count pushups, squats, and lunges while providing feedback on exercise form. It utilizes machine learning models for pose estimation and classification. This was developed for the Benefit Advanced AI Hackathon 2024 organized by the University of Bahrain.

## Data
- Data was collected using MediaPipe's pose estimation solution, collecting the normalized coordinates for 33 points.
- 75 videos of 30 frames each was done for each of the four classes; pushups, squats, lunges and noactions ( a 'null' class to reduce the number of false positives)


## Usage

1. Run the provided notebook to capture webcam footage and perform pose estimation.

2. The application will detect pushups, squats, and lunges in real-time and display the detected exercise along with a confidence score.

3. The system will count the number of repetitions for each exercise and provide feedback on exercise form in the form of on-screen text.

## Features

- Pose estimation using the MediaPipe library.
- Real-time detection and classification of pushups, squats, and lunges.
- Repetition counting for each exercise.
- Form feedback to help users maintain proper exercise technique.

## Data Collection

- Key-point values are extracted from the detected poses.
- The dataset is organized into folders based on the detected exercise type.
- Each exercise sequence consists of 30 frames of video.

## Model Training

- A Long Short-Term Memory (LSTM) neural network is trained to classify exercise types based on pose keypoints.
- The model architecture consists of multiple LSTM layers followed by dense layers with ReLU activation.
- Training is performed using Adam optimizer and categorical cross-entropy loss.

## Evaluation

- Evaluation metrics such as accuracy, precision, recall, and F1 score are computed using a confusion matrix.
- The model's performance is visualized using a confusion matrix heatmap.

## Real-time Testing

- The application provides real-time feedback on exercise form during webcam capture.
- Repetition counts for each exercise type are displayed on-screen.

## Form Evaluation

- The system calculates joint angles to detect mistakes in exercise form.
- Feedback messages are displayed to help users correct their form during exercise.

## References

- [MediaPipe](https://developers.google.com/mediapipe/solutions/vision/pose_landmarker)
- [Tutorial 1](https://www.youtube.com/watch?v=06TE_U21FK4)
- [Tutorial 2](https://youtu.be/doDUihpj6ro?si=Wog24tKlGkI4PVMf)
- [OpenCV](https://opencv.org/)


