## 👕 Deep Learning for Image Classification with CNNs and EfficientNet – Fashion MNIST Challenge

This project showcases the design, implementation, and performance comparison between two deep learning models for **image classification** using the **Fashion MNIST dataset**: a custom-built **Convolutional Neural Network (CNN)** and the advanced **EfficientNetB0** architecture.

Developed as part of the course *"Neural Network Design and Deep Learning"* at Tecnológico de Monterrey, the project aimed to evaluate the trade-offs between model simplicity and performance when applied to real-world visual classification tasks.

---

### 🧠 Objective

To classify 28x28 grayscale images of clothing items into 10 fashion categories:

`['T-shirt/top', 'Trouser', 'Pullover', 'Dress', 'Coat', 'Sandal', 'Shirt', 'Sneaker', 'Bag', 'Ankle boot']`

Two distinct convolutional architectures were developed and evaluated:

- ✅ A **custom CNN**, manually designed for speed and simplicity
- 🚀 An **EfficientNetB0** model, known for high accuracy with optimized resource usage

---

### 📂 Project Structure

- `CNN_reto.ipynb` → Custom Convolutional Neural Network
- `EfficientNetPrimerModelo.ipynb` → EfficientNetB0 Implementation
- `Proyecto de aprendizaje profundo.pdf` → Final project report with analysis and methodology

---

### 🔬 Model 1: Convolutional Neural Network (CNN)

- **Architecture**:
  - 2 convolutional layers (Conv2D)
  - 2 MaxPooling layers
  - Flatten → Dense(64) + ReLU → Dropout(0.2) → Dense(10) + Softmax
- **Training**:
  - 15 epochs
  - 1% validation split
  - Accuracy:
    - **Train:** 90.86%
    - **Test:** 90.93%
- **Strengths**:
  - Fast to train
  - Easy to tweak and extend
  - Great performance on low-resolution grayscale images

---

### ⚙️ Model 2: EfficientNetB0

- **Why EfficientNet?**  
  A state-of-the-art CNN model designed to balance accuracy and computational efficiency using compound scaling (width, depth, resolution).

- **Adaptations**:
  - Converted grayscale to RGB (required by EfficientNet)
  - Resized input from 28x28 to 32x32
  - Replaced top classifier with custom layers (AvgPooling → Dense → Dropout → Dense)
- **Training**:
  - 10 epochs
  - Validation split: 1%
  - Accuracy:
    - **Test:** 89%
- **Observations**:
  - More complex to handle
  - Longer training time
  - Slightly lower accuracy, but with better generalization control (Dropout, AvgPooling)

---

### 📊 Results Comparison

| Model          | Accuracy (Test) | Training Time | Complexity | Comments                          |
|----------------|-----------------|----------------|------------|-----------------------------------|
| Custom CNN     | 90.93%          | ⏱️ Fast         | ⭐ Simple   | Easy to build, very effective     |
| EfficientNetB0 | 89.00%          | 🐢 Slower       | ⚙️ Advanced | More modular, robust to overfitting |

---

### 🧠 Key Learnings

- CNNs are incredibly efficient for image classification with small/moderate datasets.
- EfficientNetB0 offers a scalable architecture, but requires more data preparation and tuning.
- Image preprocessing matters — from grayscale to RGB conversion, to resizing and normalization.
- Design trade-offs between performance, speed, and maintainability are crucial in deep learning.

---

### 📌 Conclusion

This project validated the power of convolutional architectures for visual recognition tasks and highlighted how architectural choices like **EfficientNet** can impact both complexity and performance. While the CNN slightly outperformed EfficientNet in accuracy, the latter offered superior modularity and regularization.

---

### 👥 Team

- José Ignacio Polanco García  
- Antonio Noemi Torres  
- Braulio Miguel Martínez Jiménez  
- Pablo Pérez Sandoval  

Course: *TC2035 - Neural Network Design and Deep Learning*  
Instructor: Dr. Santiago Conant

---

### 📬 Contact

For collaborations or model reuse inquiries:  
📩 [LinkedIn – José Ignacio Polanco](https://www.linkedin.com/in/joseignaciopolanco/)
