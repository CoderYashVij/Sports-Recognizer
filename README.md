# Sports Action Recognition using TensorFlow and Keras

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg) ![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg) ![Keras](https://img.shields.io/badge/Keras-2.x-red.svg)

This project provides a complete pipeline for building, training, and evaluating a deep learning model for action recognition in sports videos. It uses a **Long-term Recurrent Convolutional Network (LRCN)** to effectively classify actions by learning both spatial and temporal features from video frames.

---

##  Project Overview

Action recognition is a challenging computer vision task that involves identifying different actions from video clips. This project implements an LRCN model, which combines the spatial feature extraction power of Convolutional Neural Networks (CNNs) with the sequence-modeling capability of Long Short-Term Memory (LSTM) networks. The model is trained to classify a variety of actions, making it a powerful tool for video analysis.

---

##  Key Features

-   **End-to-End Implementation**: From data collection to prediction, the entire workflow is contained within the `Action_Recognition_Sports.ipynb` notebook.
-   **LRCN Architecture**: Implements the LRCN model using `TimeDistributed` CNN layers and `LSTM` layers in Keras for high-accuracy spatio-temporal learning.
-   **YouTube Video Compatibility**: Includes utility functions to download and process videos directly from YouTube links using `pafy` and `youtube-dl`.
-   **Data Preprocessing**: A complete pipeline for video-to-frame conversion, resizing, and normalization to prepare data for the model.
-   **Model Evaluation**: Includes code to visualize model accuracy and loss curves over epochs.

---

##  Model Architecture

The model (`LRCN_model`) is built using the Keras Sequential API. Its architecture consists of two main parts:

1.  **Spatial Feature Extractor (CNN)**: A `TimeDistributed` wrapper is applied to a series of `Conv2D`, `MaxPooling2D`, and `Dropout` layers. This allows the CNN to operate on each frame of the video sequence independently to extract spatial features like shapes, textures, and objects.
2.  **Temporal Sequence Modeler (LSTM)**: The sequence of feature maps extracted by the CNN is then flattened and fed into an `LSTM` layer. The LSTM analyzes the temporal relationships between frames to understand the motion and dynamics of an action over time.
3.  **Classifier**: Finally, a `Dense` layer with a `softmax` activation function classifies the sequence into the predefined action categories.

---

##  Technologies & Libraries Used

This project relies on the following Python libraries:

-   `TensorFlow` & `Keras`
-   `OpenCV-Python`
-   `MoviePy`
-   `pafy` & `youtube-dl`
-   `scikit-learn`
-   `Matplotlib`
-   `NumPy`

---

##  How to Use

### 1. Setup

**Clone the repository:**
```bash
git clone https://github.com/Anurag-Amchi/Action-Recognition-Sports
cd Action-Recognition-Sports
