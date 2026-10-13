
# ADHD Detection in ASD Children Using Handwriting Analysis

A deep learning-based system that analyzes handwriting images to classify samples into **ADHD, ASD, and Control** categories using ResNet50V2 and custom CNN layers.

## 📌 Overview

This project explores the application of deep learning and computer vision for analyzing handwriting patterns as a potential aid for preliminary screening research. It combines transfer learning using ResNet50V2 with a custom Convolutional Neural Network (CNN) classification head to identify patterns in handwriting images.

The system supports image preprocessing, feature extraction, three-class classification, and an optional web interface for uploading handwriting samples and viewing predictions.

**Note:** This project is an experimental research prototype and does not replace professional clinical diagnosis.

## 🎯 Objectives

- Classify handwriting images into ADHD, ASD, and Control categories.
- Apply transfer learning using ResNet50V2.
- Extract relevant image features using custom CNN layers.
- Support GPU-compatible model training.
- Provide an interface for uploading images and viewing predictions.
- Evaluate model performance using standard classification metrics.

## ✨ Key Features

- Handwriting image classification.
- ResNet50V2-based feature extraction.
- Custom CNN classification head.
- Image preprocessing and normalization.
- GPU-compatible training.
- Optional Streamlit web interface.
- Performance evaluation and visualization.

## 🏗️ System Architecture

```text
Handwriting Image Input
          |
          v
Image Preprocessing
(Resize and Normalize)
          |
          v
ResNet50V2 Feature Extraction
          |
          v
Custom CNN Classification
          |
          v
Three-Class Prediction
          |
          v
ADHD / ASD / Control
          |
          v
Display Results
```

## 🧠 Model Architecture

The model combines a pretrained ResNet50V2 feature extractor with custom classification layers.

| Component | Configuration |
|---|---|
| Base Model | ResNet50V2 |
| Feature Extraction | include_top=False |
| Pooling Layer | GlobalAveragePooling2D |
| Dense Layer | 128 neurons, ReLU |
| Dropout | 0.5 |
| Output Layer | 3 neurons, Softmax |
| Optimizer | Adam |
| Loss Function | Categorical Cross-Entropy |
| Evaluation Metric | Accuracy |

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Deep Learning:** TensorFlow, Keras
- **Model Architecture:** ResNet50V2, CNN
- **Image Processing:** OpenCV
- **Numerical Computing:** NumPy
- **Visualization:** Matplotlib
- **Web Interface:** Streamlit (optional)
- **Development Environment:** Jupyter Notebook

## 📊 Dataset

The project uses handwriting samples from a Kaggle ADHD dataset to explore classification across ADHD, ASD, and Control categories.

- **Input:** Handwriting images.
- **Classes:** ADHD, ASD, Control.
- **Preprocessing:** Image resizing and normalization.
- **Evaluation:** Accuracy, confusion matrix, and loss curves.

**Dataset Source:** Add the exact Kaggle dataset URL used in your project.

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/althameez-01/ADHD_DETECTION_IN_ASD_CHILDREN_USING_HANDWRITING_ANALYSIS.git
```

```bash
cd ADHD_DETECTION_IN_ASD_CHILDREN_USING_HANDWRITING_ANALYSIS
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## ▶️ Usage

### Run the Basic Model

```bash
python adhd_detection.py
```

### Run the Advanced GPU-Compatible Model

```bash
python adhd_advanced_gpu.py
```

### Launch the Streamlit Interface

If your project includes a Streamlit application, run:

```bash
streamlit run app.py
```

Replace `app.py` with the actual interface filename if necessary.

Upload a supported handwriting image and view the predicted category.

## 📈 Results

The advanced CNN model achieved approximately **87% accuracy** on the evaluated dataset.

Evaluation metrics include:

- Accuracy
- Confusion Matrix
- Training and Validation Loss Curves

The reported accuracy reflects the project's evaluation setup and does not establish clinical diagnostic performance.

## ⚠️ Limitations

- Dataset size and diversity may affect model performance.
- Handwriting varies with age, education, language, and motor abilities.
- Image quality may influence predictions.
- Generalization to unseen populations requires further validation.
- Predictions are not a substitute for professional clinical assessment.

## 🔮 Future Enhancements

- Expand the dataset with diverse handwriting samples.
- Validate the model using independent datasets.
- Integrate Grad-CAM visualizations for model explainability.
- Develop a complete web application with prediction history.
- Improve model generalization and confidence calibration.
- Strengthen privacy protection for children's data.

## 💡 Applications

- Handwriting image classification.
- Deep learning and computer vision research.
- Exploration of AI-assisted preliminary screening.
- Educational demonstrations of transfer learning.

## 👩‍💻 Author

**Al Thameez S.**


This project is licensed under the MIT License, provided that the repository's `LICENSE` file contains the MIT License. See the `LICENSE` file for details.
