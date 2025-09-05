https://github.com/user-attachments/assets/d9253828-c231-4bd0-8af8-e63d4e09620b

## StrokeScan: Automated Stroke Detection from Facial Images

StrokeScan is an automated system designed to detect facial drooping—a common symptom of stroke or Bell's palsy—using computer vision and deep learning. Every 40 seconds, someone in the US suffers a stroke, making early detection critical for preventing long-term effects like paralysis and cognitive deficiencies.

### Target Audience & Impact

StrokeScan is intended for individuals at high risk of stroke, including those who are obese, smokers, alcohol or drug users, or have high cholesterol. By diagnosing stroke quickly, the system aims to help users seek medical attention before severe symptoms develop.

### How It Works

- **Background Monitoring:** The app runs in the background and captures a screen image every 15 minutes.
- **Face Detection:** Uses a YOLO model to detect faces in the captured image.
- **Face Segmentation:** Crops and saves the detected face for further analysis.
- **Stroke Prediction:** A CNN model analyzes the face for signs of drooping and calculates the probability of stroke or Bell's palsy.
- **User Alert:** If a high probability is detected, the app alerts the user to seek help.

### Model Performance

- The CNN model achieved 98% accuracy on the test set.
- ROC curve AUC score: 0.99 (excellent discrimination between stroke and non-stroke cases).

### Example Workflow

1. Capture image from webcam or screen.
2. Detect and crop face using YOLO.
3. Analyze cropped face with CNN for stroke probability.
4. Alert user if probability exceeds threshold.

### Code Overview

- `ml.ipynb`: Contains the YOLO-based face detection and segmentation pipeline.
- `main/cnn.ipynb`: Contains the CNN training and evaluation code for stroke detection.

---

