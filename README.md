# MNIST_FASHION_CLASSIFICATION
# 🧠 MNIST Digit Classification using CNN

This project implements a Convolutional Neural Network (CNN) for classifying handwritten digits from the MNIST dataset. It uses **PyTorch** for training and **Typer** for command-line interaction. The model tracks performance metrics and provides visualizations for loss, accuracy, and misclassifications.

---

## 📦 Dataset: MNIST

The MNIST dataset consists of **70,000 grayscale images** (28x28 pixels) of handwritten digits (0–9).

- **Training Set**: 60,000 images  
- **Test Set**: 10,000 images  
- **Classes**: 10 (digits 0 to 9)

The dataset is automatically downloaded using `torchvision.datasets.MNIST`.

---

## 🧠 Model Architecture

### Convolutional Layers
- 3 Convolutional layers with ReLU activation
- Each followed by **MaxPooling** to reduce spatial dimensions

### Fully Connected Layers
- 3 Dense layers for high-level feature learning and classification

---

## 🔧 Training Configuration

| Setting          | Value                     |
|------------------|---------------------------|
| Optimizer        | Adam                      |
| Learning Rate    | `0.01` (customizable)     |
| Epochs           | `20` (customizable)       |
| Loss Function    | CrossEntropyLoss          |
| Model Save Path  | `model.pth`               |

Training logs:
- **Training Loss**
- **Testing Loss**
- **Accuracy**

---

## 🖥️ Command-Line Interface (Typer)

This project uses **Typer** to provide CLI options for training configuration.

### ✅ Example Usage

```bash
python train.py --epochs 30 --lr 0.005
