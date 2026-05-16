# 🧠 CIFAR-10 Image Classification using CNN (PyTorch)

---

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** using **PyTorch** to classify images from the **CIFAR-10 dataset** into 10 different object categories.

The project covers the complete deep learning workflow, including:

- ✔ Data preprocessing  
- ✔ CNN model architecture design  
- ✔ Model training and evaluation  
- ✔ Optimizer experimentation  
- ✔ Performance visualization  

---

## 📂 Dataset

**Dataset:** CIFAR-10

The dataset contains:

- 60,000 colored images  
- Image size: **32 × 32 pixels**  
- 10 real-world object classes  

### 🏷️ Classes

- ✈️ Airplane  
- 🚗 Automobile  
- 🐦 Bird  
- 🐱 Cat  
- 🦌 Deer  
- 🐶 Dog  
- 🐸 Frog  
- 🐴 Horse  
- 🚢 Ship  
- 🚛 Truck  

### 📥 Dataset Loading

```python
torchvision.datasets.CIFAR10
```

---

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- ✔ Resize images to **32 × 32**
- ✔ Convert images to tensors
- ✔ Normalize image values
- ✔ Apply data augmentation

### 🔹 Normalization

```python
transforms.Normalize(
    (0.5, 0.5, 0.5),
    (0.5, 0.5, 0.5)
)
```

### 🔹 Data Augmentation

- Random Horizontal Flip

---

## 🧠 Model Architecture (CNN)

### 🔹 Feature Extraction Layers

- Conv2D (**3 → 32**)  
- Batch Normalization  
- ReLU Activation  
- Max Pooling  

- Conv2D (**32 → 64**)  
- Batch Normalization  
- ReLU Activation  
- Max Pooling  

- Conv2D (**64 → 128**)  
- Batch Normalization  
- ReLU Activation  
- Max Pooling  

---

### 🔹 Classification Layers

- Flatten Layer  
- Fully Connected Layer (**512 neurons**)  
- ReLU Activation  
- Dropout (**0.5**)  
- Output Layer (**10 classes**)  

---

## 🚀 Training Setup

- ✔ **Loss Function:** CrossEntropyLoss  
- ✔ **Epochs:** 10  
- ✔ **Batch Size:** 64  
- ✔ **Device:** CPU / GPU (Auto-detected)  

---

## ⚙️ Experiments

Two different optimizers were tested:

| Model | Optimizer | Accuracy | Loss |
|------|------------|-----------|------|
| Model A | Adam | ⭐ 78.53% | 0.6376 |
| Model B | SGD | ⭐ 74.45% | 0.7307 |

### ✅ Observation

The **Adam optimizer** achieved better performance compared to **SGD**.

---

## 📊 Evaluation Metrics

The model was evaluated using:

- ✔ Accuracy  
- ✔ Loss  

Evaluation was performed on the **test dataset**.

---

## 📉 Visualization

The following plots were generated:

- ✔ Training vs Validation Loss  
- ✔ Training vs Validation Accuracy  

These visualizations help with:

- Monitoring model learning behavior  
- Detecting overfitting  
- Comparing optimizer performance  

---

## 🛠️ Installation

Install the required libraries:

```bash
pip install torch torchvision matplotlib
```

---

## ▶️ How to Run

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/arwa-egy/cifar10-cnn.git
cd cifar10-cnn
```

### 2️⃣ Run Training

```bash
python main.py
```

---

## 📌 Key Features

- ✔ CNN-based image classification  
- ✔ Batch Normalization  
- ✔ Dropout Regularization  
- ✔ Data Augmentation  
- ✔ Multiple Optimizer Experiments  
- ✔ Performance Visualization  

---

## 📈 Results Summary

- ✔ **Best Accuracy:** 78.53%  
- ✔ **Best Loss:** 0.6376  
- ✔ **Best Model:** CNN with Adam Optimizer  

---

## 📚 Conclusion

This project demonstrates a complete deep learning pipeline for image classification using CNNs with PyTorch. It includes preprocessing, model design, training, evaluation, visualization, and optimizer comparison to achieve strong classification performance on the CIFAR-10 dataset.
