# Pattern Recognition with Feedforward Neural Networks

## Executive Summary
This project utilizes the **MATLAB Deep Learning Toolbox** to engineer and optimize **Feedforward Neural Networks (FNN)** designed for computer vision tasks—specifically, the classification of geometric primitives.

The study focuses on the **Hyperparameter Tuning** process, systematically analyzing how network topology (layers/neurons), activation functions, and training algorithms (Levenberg-Marquardt) impact model accuracy and generalization capability against binary image datasets.

## Data Pipeline & Pre-processing
The input data consists of 25x25 pixel binary images, flattened into input vectors for the network. The system classifies six distinct classes:
* **Classes:** Circle, Kite, Parallelogram, Square, Trapezoid, Triangle.



### Dataset Partitioning
To ensure robust validation, the data was segregated into four tiers:
1.  **Start (Calibration):** A minimal set (5/shape) for initial topology testing.
2.  **Train (Core):** The primary dataset (50/shape) used for backpropagation learning.
3.  **Test (Validation):** Unseen data (10/shape) to measure generalization and detect overfitting.
4.  **Draw (Robustness):** Manually hand-drawn shapes to stress-test the model against imperfect inputs.

## Methodology & Experimental Stages

### 1. Network Architecture Search
Initial experiments involved training simple perceptron-based structures to establish a baseline. The project then moved to **Topology Optimization**, varying the number of hidden layers and neurons to find the optimal balance between underfitting and overfitting.

### 2. Hyperparameter Optimization
Using the *Train* dataset, extensive A/B testing was conducted on:
* **Activation Functions:** Comparing Sigmoid (`logsig`), Tanh (`tansig`), and Linear (`purelin`).
* **Training Algorithms:** Evaluating convergence speed and stability (e.g., `trainlm`).
* **Data Split Strategies:** Adjusting the Training/Validation/Testing ratios (Standard: 70/15/15).

### 3. Generalization & Stress Testing
The best-performing models were subjected to a **Combined Evaluation**, retraining them with merged datasets to maximize learning density. Finally, the models were deployed against the *Draw* dataset to evaluate real-world performance on non-standardized inputs.

### 4. MATLAB GUI Deployment
A custom **Graphical User Interface (GUI)** was developed to abstract the code complexity, allowing users to:
* Dynamically configure network topology.
* Load datasets and train models in real-time.
* Visualize performance metrics (Confusion Matrices, MSE).

## Technical Stack
* **Environment:** MATLAB (Deep Learning Toolbox).
* **Algorithm:** Feedforward Backpropagation (Supervised Learning).
* **Analysis:** Statistical performance tracking via Excel (Experiences.xlsx).

---

## Academic Context
This project was developed for the **"Knowledge and Reasoning"** course (2024/2025).

**Team Size:** 2 Members
**Final Evaluation:** 9 / 10
