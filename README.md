# 🏙️ Street View House Numbers (SVHN) Digit Recognition

Welcome to our deep learning project for recognizing digits from real-world images using the **Street View House Numbers (SVHN)** dataset!

🔗 **Live Repo:** [Smartlyfe21/Street-View-House-Numbers-Digit-Recognition](https://github.com/Smartlyfe21/Street-View-House-Numbers-Digit-Recognition)

---

## 📦 Dataset

We used the official [SVHN dataset from Kaggle](https://www.kaggle.com/datasets/stanfordu/street-view-house-numbers). It contains:

- Real-world digit images cropped from Google Street View.
- `.png` image files
- Annotations stored in `digitStruct.mat` for bounding boxes and labels.

> 🔁 Note: Digit '0' is represented as '10' in the dataset and converted back to 0 during preprocessing.

---

## 🧠 Project Pipeline

Here's what we did step-by-step:

### 📁 Data Exploration & Access
- Verified image paths and listed `.png` files
- Displayed sample images using `matplotlib`

### 🔍 Annotation Parsing
- Loaded and parsed `digitStruct.mat` using `h5py`
- Extracted:
  - Image file names
  - Bounding box details (left, top, width, height)
  - Labels for each digit

### ✂️ Digit Cropping & Preprocessing
- Cropped individual digits from multi-digit images
- Resized digits to 32x32 and normalized for training
- Prepared `X_data` and `y_data` arrays

### 🧰 Visualizations
- Plotted images with bounding boxes using `matplotlib.patches`
- Displayed cropped digits with their corresponding labels

### 🧠 Model Training
- Built a CNN using TensorFlow/Keras
- Trained on extracted digit images
- Plotted training vs validation loss and accuracy over epochs

---

## 📊 Results Snapshot

Our model learned to accurately classify digits (0–9) with good performance.

Training Curves:

![Accuracy Plot](assets/accuracy_plot.png)
![Loss Plot](assets/loss_plot.png)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Smartlyfe21/Street-View-House-Numbers-Digit-Recognition.git
cd Street-View-House-Numbers-Digit-Recognition





📚 References

Dataset: Kaggle - SVHN
Paper: Reading Digits in Natural Images with Unsupervised Feature Learning by Yuval Netzer et al.
Tools: Python, NumPy, Pandas, PIL, Matplotlib, TensorFlow/Keras
👥 Authors

Mukama Louis — GitHub
📄 License

This project is licensed under the MIT License.
