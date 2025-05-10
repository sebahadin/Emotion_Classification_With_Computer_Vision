# 🌝 Facial Expression Recognition with Deep Learning

A lightweight, interactive web application for real-time **facial emotion classification** using computer vision and deep learning — powered by **Streamlit**, **PyTorch**, and **Grad-CAM**.

## 🚀 Features

- 📸 Take a photo with your webcam
- 🔍 Choose from 3 deep learning models: `CNN`, `VGG16`, and `ViT`
- 🧠 See predictions with **emotion labels** (e.g., Happiness, Sadness)
- 🌡️ Grad-CAM heatmap overlays to visualize model attention
- 🎲 Random test image predictions from the dataset
- 📈 Model metrics viewer (Loss & Accuracy curves)
- 🧹 Architecture summary with param breakdown
- 🤝 Dataset contribution form (image upload + labeling)

---

## 👩‍💻 Demo Screenshot

![Demo](demo_screenshot.png)

---

## 📦 Installation

```bash
# 1. Clone the repo
git clone https://github.com/your-username/emotion-classification.git
cd emotion-classification

# 2. Create a virtual environment
python3 -m venv .venv
source .venv/bin/activate  # or `.venv\Scripts\activate` on Windows

# 3. Install dependencies
pip install -r requirements.txt
```

---

## 🏃‍♂️ Run the App

```bash
streamlit run app.py
```

---

## 📂 Folder Structure

```
emotion-classification/
│
├── app.py                  # Main Streamlit app
├── models.py               # Model loading, preprocessing, Grad-CAM
├── data_viz.py             # Metrics and architecture visualizations
├── requirements.txt
├── Dataset/                # Train/test folders with emotion-labeled images
│   └── train/
│       └── [1-6]/
│   └── test/
│       └── [1-6]/
└── README.md
```

---

## 🧠 Model Overview

| Model   | Architecture | Input Size | Params     | Size    |
|---------|--------------|------------|------------|---------|
| CNN     | Custom 2 Conv + 2 FC     | 100×100     | ~4.7M     | 25.5 MB |
| VGG16   | Pretrained + FC Fine-tuned | 224×224     | 116M      | 2.4 GB  |
| ViT     | Vision Transformer       | 224×224     | ~5.5M     | 1.3 GB  |

---

## 🧠 Supported Emotions

```
1 → Surprise  
2 → Disgust  
3 → Happiness  
4 → Sadness  
5 → Anger  
6 → Neutral
```

---

## 🤜 Contribute Your Own Expression!

Use the **"Contribute to Dataset"** page to:

- Capture images from your webcam
- Label them with an emotion
- Save them locally (auto-sorted into folders)

You can then retrain the model with the new data.

---

## 📈 Example Metrics

- CNN achieves >93% accuracy after 30 epochs
- VGG16 and ViT support transfer learning with strong generalization

---

## 🧹 Future Work

- Add fear label back into the dataset
- Improve ViT Grad-CAM visualization
- Deploy app with image storage to Firebase or AWS S3
- Train on FER-2013 or AffectNet for generalization

---

## 📝 License

This project is released under the MIT License.

---

## ✨ Acknowledgments

- [Streamlit](https://streamlit.io)
- [PyTorch](https://pytorch.org)
- [pytorch-grad-cam](https://github.com/jacobgil/pytorch-grad-cam)
