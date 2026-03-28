# Skin-Disease-Detection-System

# 🩺 Skin Diseases Detection System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red?logo=streamlit&logoColor=white)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A deep learning–based system for automated detection and classification of skin diseases from dermoscopic images. This project covers the complete machine learning pipeline — from data acquisition and preprocessing to model training and deployment via a Streamlit web application.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [ML Pipeline](#ml-pipeline)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Running the App](#running-the-app)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

---

## 🔍 Overview

Skin diseases are among the most common health conditions worldwide. Early and accurate diagnosis can significantly improve patient outcomes. This project leverages Convolutional Neural Networks (CNNs) to classify dermoscopic skin images into multiple disease categories, providing a fast and accessible tool for preliminary skin condition screening.

Key highlights:
- End-to-end ML pipeline from raw data to a deployed web app
- Data augmentation to address class imbalance
- Streamlit-powered interactive frontend for real-time predictions
- Comprehensive testing and documentation notebooks

---

## 📁 Project Structure

```
skin-diseases-detection-system/
│
├── 01-kaggle-data-setup.ipynb          # Download & configure Kaggle dataset
├── 02-data-analysis-ipynb.ipynb        # Exploratory Data Analysis (EDA)
├── 03-data-cleaning-ipynb.ipynb        # Data cleaning & preprocessing
├── 04-train-val-split-ipynb.ipynb      # Train/validation/test split
├── 05-data-augmentation-ipynb.ipynb    # Image augmentation techniques
├── 06-save-to-drive-ipynb.ipynb        # Save processed data to Google Drive
├── 07-model-architecture-ipynb.ipynb   # CNN model architecture definition
├── 08-model-training-ipynb-2.ipynb     # Model training & evaluation
├── 09-run-streamlit-ipynb-3.ipynb      # Launch Streamlit web application
├── 10-testing-documentation.ipynb      # Testing & documentation
├── .gitignore
└── README.md
```

---

## 🔄 ML Pipeline

```
Kaggle Dataset
     ↓
Exploratory Data Analysis
     ↓
Data Cleaning & Preprocessing
     ↓
Train / Validation / Test Split
     ↓
Data Augmentation
     ↓
Save Processed Data (Google Drive)
     ↓
Model Architecture (CNN)
     ↓
Model Training & Evaluation
     ↓
Streamlit Web App Deployment
     ↓
Testing & Documentation
```

---

## 🛠️ Technologies Used

| Category | Tools / Libraries |
|---|---|
| Language | Python 3.8+ |
| Deep Learning | TensorFlow / Keras |
| Data Processing | NumPy, Pandas, OpenCV |
| Visualization | Matplotlib, Seaborn |
| Augmentation | Keras ImageDataGenerator / Albumentations |
| Web App | Streamlit |
| Dataset Source | Kaggle |
| Storage | Google Drive |
| Environment | Jupyter Notebook / Google Colab |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

```bash
Python >= 3.8
pip
Jupyter Notebook or Google Colab
```

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/Kevinchovatiya/skin-diseases-detection-system.git
cd skin-diseases-detection-system
```

2. **Install required dependencies**

```bash
pip install tensorflow keras numpy pandas matplotlib seaborn opencv-python streamlit kaggle
```

3. **Configure Kaggle API**

   - Go to [kaggle.com](https://www.kaggle.com) → Account → Create New API Token
   - Place the downloaded `kaggle.json` in `~/.kaggle/`

4. **Run the notebooks in order** (01 → 10) for the full pipeline.

---

## 📦 Dataset

The dataset is sourced from **Kaggle** and contains dermoscopic images of multiple skin disease categories. The setup notebook (`01-kaggle-data-setup.ipynb`) automates the download and directory setup.

- **Source:** Kaggle (dermoscopy / skin lesion dataset)
- **Preprocessing:** Resizing, normalization, noise removal
- **Augmentation:** Flipping, rotation, zoom, brightness adjustment
- **Split:** Train / Validation / Test

> **Note:** You need a valid Kaggle API key to download the dataset automatically.

---

## 🧠 Model Architecture

The model is built using a Convolutional Neural Network (CNN) architecture defined in `07-model-architecture-ipynb.ipynb`. Key design choices include:

- Multiple convolutional and pooling layers for feature extraction
- Batch normalization for training stability
- Dropout layers to prevent overfitting
- Dense output layer with softmax activation for multi-class classification
- Transfer learning support (e.g., EfficientNet / MobileNet as backbone)

Training details are covered in `08-model-training-ipynb-2.ipynb`, including loss curves, accuracy metrics, and confusion matrix visualization.

---

## 🌐 Running the App

The Streamlit app allows users to upload a skin image and receive a disease classification prediction in real time.

To launch the app, run `09-run-streamlit-ipynb-3.ipynb` or execute:

```bash
streamlit run app.py
```

> **Note:** Ensure the trained model file (`.h5` or `.keras`) is available in the expected path before launching.

The app will open at `http://localhost:8501` in your browser.

---

## ✅ Testing

Testing and validation procedures are documented in `10-testing-documentation.ipynb`. This includes:

- Model performance metrics (accuracy, precision, recall, F1-score)
- Confusion matrix analysis
- Sample prediction outputs
- Edge case testing with unseen images

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork this repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Open a Pull Request

Please ensure your code is well-documented and tested before submitting.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**Kevin Chovatiya**
- GitHub: [@Kevinchovatiya](https://github.com/Kevinchovatiya)

---

> ⚠️ **Disclaimer:** This project is intended for educational and research purposes only. It is not a substitute for professional medical diagnosis. Always consult a qualified dermatologist for medical advice.
