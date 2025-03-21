# **Robust Training of Multilayer Perceptrons (MLPs) on Noisy Data**

## **Project Overview**
This project explores the impact of **noisy data on Multilayer Perceptrons (MLPs)** and methods to improve model robustness. The study focuses on **training MLPs on noisy MNIST data**, evaluating their performance, and implementing techniques such as **Batch Normalization, Dropout, and L2 Regularization** to enhance generalization.

## **Dataset**
We use the **MNIST dataset**, which contains 28×28 grayscale images of handwritten digits (0-9). To simulate real-world scenarios, **Gaussian noise** is added to both training and test images.

## **Objectives**
- Train an **MLP model** on noisy data and evaluate its performance.
- Compare **accuracy on clean vs. noisy test data**.
- Visualize **loss curves and accuracy trends**.
- Implement **noise mitigation techniques** such as **Dropout, Batch Normalization, and L2 Regularization**.

---

## **Model Architecture**
The MLP model consists of:
- **Input Layer**: Flattened 28×28 pixel images into a **1D vector (784 features)**.
- **Hidden Layers**:
  - **Dense (256 neurons, ReLU activation)**
  - **Batch Normalization** (stabilizes training)
  - **Dropout (30%)** (prevents overfitting)
  - **Dense (128 neurons, ReLU activation)**
  - **Batch Normalization & Dropout (30%)**
- **Output Layer**: **Softmax activation** with 10 neurons (for digits 0-9).

---

## **Installation & Requirements**
To run the code, install the required dependencies:
pip install tensorflow numpy matplotlib


### Code Implementation
**Data Preprocessing**
Normalize MNIST images to [0,1].
Add Gaussian noise with noise_factor = 0.3.
**Model Definition**
Use Dense layers for feature learning.
Apply Batch Normalization for stable training.
Implement Dropout (30%) for regularization.
Use L2 Regularization to reduce overfitting.
**Training & Evaluation**
Train the model on noisy MNIST images.
Evaluate accuracy on clean and noisy test data.
Plot loss and accuracy curves to analyze model performance.
### Results
Accuracy on Clean Data: ~94-96%
Accuracy on Noisy Data: Lower than clean accuracy (affected by noise)
Loss & Accuracy Curves:
Loss Curve: Helps detect overfitting.
Accuracy Curve: Shows how well the model generalizes.
### Noise Mitigation Strategies
To improve model robustness, we implement: 
Data Augmentation – Introduces noise to improve generalization.
Dropout (30%) – Randomly disables neurons to prevent overfitting.
Batch Normalization – Normalizes activations to stabilize learning.
L2 Regularization – Penalizes large weights to improve generalization.
Robust Loss Functions – Huber loss or MAE instead of MSE for stability.
### Author
👩‍💻 Thulluri Ramya
## **License**
This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this code with proper attribution.  
See the [LICENSE](LICENSE) file for more details.
