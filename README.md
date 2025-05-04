# 🧠 Urdu Deepfake Detection App

This is a web-based deepfake detection system tailored for the **Urdu language**, powered by machine learning models. It allows users to input text and instantly detect whether the content may be a deepfake — using Logistic Regression, SVM, or a Deep Neural Network model — all wrapped in an easy-to-use Gradio interface.
this project aims to combat the rising threat of misinformation in regional languages by providing an accessible and reliable detection tool.

---


## ✨ Features

- 🔍 **Deepfake detection for Urdu text**
- 🤖 Choose from 3 models: Logistic Regression, SVM, or Deep Neural Network
- 📈 Confidence scores shown via interactive Plotly bar charts
- 📋 Results displayed in a clean HTML table
- 🖼️ Minimal, user-friendly Gradio interface
- 💾 Ready for deployment on Hugging Face Spaces

---

## 🧠 Models Used

All models were trained on the [CSALT Urdu Deepfake Detection Dataset](https://huggingface.co/datasets/CSALT/deepfake_detection_dataset_urdu).

- **Logistic Regression**: Light-weight and fast baseline
- **Support Vector Machine (SVM)**: More robust to outliers
- **Deep Neural Network (DNN)**: Better at capturing complex patterns

Text data is vectorized using **TF-IDF**, and models are trained for binary classification (`real` vs `deepfake`).

---

## 🖥️ Interface Preview

| Prediction Output | Confidence Scores |
|------------------|------------------|
| ✅ Real / Deepfake | 📊 Interactive Bar Chart |

---

## 🔧 How It Works

1. User pastes or types Urdu text into the app.
2. The text is converted into numerical features using TF-IDF.
3. The selected model makes a prediction.
4. Output shows whether it's likely a deepfake and displays a confidence chart.

---

## 📂 Project Structure

```bash
├── app.py                    # Main Gradio app
├── models/                   # Saved ML models
│   ├── lr_model.pkl
│   ├── svm_model.pkl
│   ├── dnn_model.pkl
│   ├── vectorizer.pkl
│   └── label_columns.pkl
├── requirements.txt          # Python dependencies
├── README.md                 # This file
