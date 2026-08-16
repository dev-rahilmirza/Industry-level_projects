# 🎯 Face Detection System

A real-time face detection application built with Python and OpenCV, using the Haar Cascade Classifier to detect and highlight faces through a webcam feed.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?logo=opencv&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📸 Demo

<img width="1892" height="943" alt="Screenshot 2026-08-16 210326" src="https://github.com/user-attachments/assets/85928823-eeed-4091-94d8-715665448a09" />


---

## ✨ Features

- **Real-time face detection** via webcam using OpenCV's Haar Cascade model
- **Live face counter** displayed on the video feed
- **Snapshot capture** — save the current frame as a `.jpg` with a keypress
- **Lightweight & dependency-free** beyond OpenCV — no deep learning framework required

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| OpenCV (`cv2`) | Computer vision & webcam I/O |
| Haar Cascade Classifier | Pre-trained face detection model |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x installed
- A working webcam

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/face-detection.git
   cd face-detection
   ```

2. **Install dependencies**
   ```bash
   pip install opencv-python
   ```

### Running the App

```bash
python3 face_detection.py
```

---

## 🎮 Controls

| Key | Action |
|-----|--------|
| `s` | Save the current frame as `captured_face.jpg` |
| `q` | Quit the application |

---

## ⚙️ Configuration

You can tweak detection sensitivity inside `face_detection.py`:

```python
faces = face_cascade.detectMultiScale(
    gray,
    scaleFactor=1.3,   # How much the image is reduced at each scale (higher = faster, less accurate)
    minNeighbors=5     # How many neighbor rectangles needed to confirm a face (higher = fewer false positives)
)
```

**Webcam index** — if your webcam isn't detected, change the device index:
```python
cap = cv2.VideoCapture(0)  # Try 0, 1, or 2 depending on your system
```

> **macOS users:** The script uses `cv2.CAP_AVFOUNDATION` as the backend, which is the recommended capture API for macOS.

---

## 📁 Project Structure

```
face-detection/
│
├── face_detection.py     # Main application script
├── requirements.txt      # Dependencies & setup instructions
└── README.md             # Project documentation
```

---

## 🧠 How It Works

1. **Capture** — OpenCV opens the webcam and reads frames in a loop.
2. **Preprocess** — Each frame is converted to grayscale, which is what the Haar Cascade model expects.
3. **Detect** — The `detectMultiScale` function scans the grayscale frame at multiple scales to locate faces.
4. **Annotate** — Green rectangles are drawn around each detected face, and a face count is overlaid on the frame.
5. **Display** — The annotated frame is shown in a live window.

---

## 📦 Dependencies

```
opencv-python
```

Install with:
```bash
pip install opencv-python
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open a pull request or file an issue.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
