# 😊 Real-Time Emotion Detection

A real-time facial emotion detection system built with OpenCV and Keras. It uses your webcam to detect faces and classify emotions live using a pre-trained deep learning model — no third-party services like DeepFace required.

---
<img width="1899" height="964" alt="image" src="https://github.com/user-attachments/assets/e0227f69-141e-43dd-8ae5-fdb177c0a7e7" />



## 🎯 Features

- Real-time webcam feed with live emotion classification
- Detects 7 distinct emotions: **Angry**, **Disgust**, **Fear**, **Happy**, **Sad**, **Surprise**, and **Neutral**
- Lightweight and runs locally — no internet connection needed
- Compatible with macOS and other platforms

---

## 🧠 How It Works

1. Each video frame is captured from the webcam and converted to grayscale.
2. OpenCV's Haar Cascade classifier detects faces in the frame.
3. Each detected face is cropped, resized to 64×64 pixels, and normalized.
4. A Keras CNN model predicts the emotion from the face region.
5. The detected emotion label and a bounding box are overlaid on the live video feed.

---

## 📋 Requirements

- Python 3.7+
- OpenCV
- NumPy
- Keras (with TensorFlow backend)
- A pre-trained emotion model file: `emotion_model.hdf5`

---

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/emotion-detection.git
   cd emotion-detection
   ```

2. **Install dependencies**
   ```bash
   pip install opencv-python numpy tensorflow keras
   ```

3. **Add the model file**

   Place your pre-trained `emotion_model.hdf5` file in the root directory of the project. The model should accept grayscale images of size **64×64** and output probabilities for 7 emotion classes.

---

## 🚀 Usage

```bash
python emotion_detection.py
```

- A window titled **"Emotion Detection System"** will open showing your webcam feed.
- Detected faces will be highlighted with a green bounding box and labeled with the predicted emotion.
- Press **`q`** to quit the application.

---

## 📁 Project Structure

```
emotion-detection/
│
├── emotion_detection.py    # Main application script
├── emotion_model.hdf5      # Pre-trained Keras model (add manually)
└── README.md
```

---

## 🏷️ Emotion Labels

| Index | Emotion  |
|-------|----------|
| 0     | Angry    |
| 1     | Disgust  |
| 2     | Fear     |
| 3     | Happy    |
| 4     | Sad      |
| 5     | Surprise |
| 6     | Neutral  |

---

## ⚙️ Model Details

The system expects a Keras model (`emotion_model.hdf5`) trained on grayscale facial images with the following input spec:

- **Input shape:** `(1, 64, 64, 1)`
- **Output:** Softmax probabilities over 7 emotion classes

Popular compatible datasets for training such a model include [FER-2013](https://www.kaggle.com/datasets/msambare/fer2013).

---

## 🐛 Troubleshooting

**Webcam not opening:** Ensure no other application is using the camera. Try changing `cv2.VideoCapture(0)` to `cv2.VideoCapture(1)` if you have multiple cameras.

**Model file not found:** Make sure `emotion_model.hdf5` is in the same directory as the script.

**Low detection accuracy:** Ensure adequate lighting and that your face is clearly visible to the camera.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
# How to run this code? (Extremely imp step)

- you should install python 3.11 version (Python recent version won't support 3.14)

- then follow these commands to run in terminal (vs code or pycharm)

- Create Virtual Environment (IMPORTANT)
# python3.11 -m venv ai_env


- Activate Environment
# source ai_env/bin/activate


- Install Required Packages
# pip install opencv-python tensorflow keras numpy


- Run Your Emotion Project
# python3 emotion_detection.py





## 🎯 IMPORTANT RULE

- Every time you want to run AI project:

- You must activate environment first:

## source ai_env/bin/activate

- Then run your script.
