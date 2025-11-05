# 🏅 Sports Action Recognition using TensorFlow & Keras

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red)
![License](https://img.shields.io/badge/License-MIT-green)

## 🔍 Overview

Sports action recognition is a challenging computer vision task focused on identifying different human actions from videos. This project implements a deep learning pipeline using **LRCN (Long-term Recurrent Convolutional Network)**—combining CNNs for spatial feature learning and LSTMs for temporal motion understanding.

The notebook provides:

- ✅ **Video → Frames → Training → Prediction pipeline**
- ✅ **YouTube & local video support**
- ✅ **Model training & evaluation tools**

---

## 🚀 Key Features

| Feature | Description |
|---------|-------------|
| 🎥 **Video-based action classification** | Recognizes different sports actions |
| 🧠 **LRCN Deep Learning Model** | CNN + LSTM for spatio-temporal learning |
| 📦 **End-to-End Notebook** | Dataset preprocessing → Model → Prediction |
| ⬇️ **YouTube Video Support** | Download training videos from YouTube |
| 🛠 **Complete Pre-processing Pipeline** | Frame extraction, resizing, normalization |
| 📈 **Model Evaluation** | Visualize accuracy & loss |

---

## 🏗️ Model Architecture

### 📘 Concept

```
Input Video Frames  
        ↓
[TimeDistributed Conv2D + MaxPool] × N  
        ↓
TimeDistributed Flatten  
        ↓
LSTM Layers  
        ↓
Dense + Softmax  
        ↓
Predicted Action
```

### ✨ Core Idea

- **CNN layers** learn frame-wise spatial features
- **LSTM** captures motion & temporal relationships
- **Dense softmax** classifies final action

---

## 📦 Technologies & Libraries

| Category | Tools |
|----------|-------|
| **Deep Learning** | TensorFlow, Keras |
| **Video Processing** | OpenCV, MoviePy |
| **Web Video Support** | pafy, youtube-dl |
| **Utilities** | NumPy, scikit-learn |
| **Visualization** | Matplotlib |

---

## 📂 Directory Structure

```
Sports-Recoganizer/
│── data/
│   ├── raw_videos/
│   └── processed_frames/
│── models/
│   └── lrcn_model.h5
│── notebooks/
│   └── Action_Recognition_Sports.ipynb
│── utils/
│   ├── video_downloader.py
│   ├── frame_extractor.py
│   └── data_pipeline.py
│── README.md
└── requirements.txt
```

> **Note:** Folders may be auto-created during execution

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/CoderYashVij/Sports-Recoganizer.git
cd Sports-Recoganizer
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Open Notebook

```bash
jupyter notebook
```

Then open: `notebooks/Action_Recognition_Sports.ipynb`

---

## ▶️ Run the Pipeline

### ✅ Training

1. Load dataset or download videos
2. Notebook auto-processes frames
3. Trains LRCN model on sequences

### ✅ Prediction Example

```python
predict_on_video("example.mp4")
```

---

## 📊 Model Performance

- ✅ **Spatial + Temporal** deep learning
- ✅ Works on **sports motion videos**
- ✅ Accuracy & loss curves available in notebook
- ✅ Model improves with more labeled sports video data

---

## 🔧 Future Improvements

- [ ] Real-time webcam prediction
- [ ] Streamlit/Gradio UI dashboard
- [ ] Replace LRCN with **I3D / ConvLSTM / ViT-based** architecture
- [ ] Fine-tuning using **Sports-1M / Kinetics** dataset
- [ ] Lightweight **TFLite** mobile deployment

---

## 🤝 Contribution Guidelines

Contributions are welcome! 🎉

**Fork → Create Branch → Commit → Push → Pull Request**

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Yash Vij**

- 🔗 GitHub: [@CoderYashVij](https://github.com/CoderYashVij)

---

## ⭐ Support

If you find this useful, please **⭐ the repo** — it motivates development & helps others find it!

---

### 📸 Screenshots

> Add screenshots of your model training, predictions, or UI here!

---

### 🙏 Acknowledgments

- TensorFlow & Keras teams for amazing deep learning frameworks
- OpenCV community for video processing tools
- Research papers on LRCN and action recognition

---

**Happy Coding! 🚀**
