# Handwritten Arabic Numerals Recognition 🔢

A Convolutional Neural Network (CNN) for classifying handwritten Arabic-Indic digits (0–9),
achieving **98.15% test accuracy** and **99.07% best validation accuracy** on the Mendeley Arabic Numerals Dataset.

Built as a final project for ENCS5343 - Computer Vision | Birzeit University.

---

## 🧠 Model Architecture

A custom lightweight CNN — **ArabicNumeralCNN** — with ~1.1M parameters:

- 3 Convolutional blocks (Conv → BatchNorm → ReLU → MaxPool)
- Channels: 32 → 64 → 128
- Fully connected classifier: 2048 → 512 → 10
- Dropout (p=0.5) for regularization

---

## 📊 Results

| Split      | Loss   | Accuracy |
|------------|--------|----------|
| Train      | 0.0603 | 98.11%   |
| Validation | 0.0287 | 99.07%   |
| Test       | —      | 98.15%   |

- **1,377 / 1,402** test images correctly classified
- All 10 classes achieve F1-score ≥ 0.96
- Digits 4 and 8 reach perfect F1 = 1.00

---

## 📂 Dataset

**Mendeley Handwritten Arabic Numerals Dataset**  
- 9,350 grayscale images, 10 balanced classes (935 per class)  
- Split: 70% train / 15% validation / 15% test  
- Link: https://data.mendeley.com/datasets/5hpkf8v7bg/1

---

## ⚙️ Training Configuration

| Hyperparameter | Value |
|----------------|-------|
| Optimizer | Adam (β1=0.9, β2=0.999) |
| Learning Rate | 0.001 (initial) |
| LR Scheduler | StepLR — halved every 8 epochs |
| Epochs | 25 |
| Batch Size | 64 |
| Loss Function | Cross-Entropy |

---

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/arabic-numerals-recognition.git
cd arabic-numerals-recognition
pip install -r requirements.txt
jupyter notebook FinalVision.ipynb
```

---

## 🛠️ Tech Stack

- Python · PyTorch · torchvision
- NumPy · Matplotlib · scikit-learn
- Jupyter Notebook

---

## 📌 Course Info

**ENCS5343 — Computer Vision**  
Birzeit University | First Semester 2025/2026  
Instructor: Dr. Aziz Qaroush  
Student: Aya Abdelrahman Fares
