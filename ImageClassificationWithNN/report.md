# Animal Image Classification using Feedforward Neural Network with Backpropagation

## 1. Objective
The goal of this project is to classify animal images into three categories: **dog**, **butterfly**, and **elephant** using a **Feedforward Neural Network (FNN)** with backpropagation and categorical cross-entropy loss.

---

## 2. Dataset
- **Dataset Used**: Animals-10 dataset (subset)
- **Classes Selected**: `dog`, `butterfly`, `elephant`
- **Preprocessing**:
  - Images resized to `64x64`
  - Normalized using mean and std = 0.5
  - Converted to tensors
- **Class Balancing**:
  - The smallest class (`elephant`) had **1433 images**
  - Selected **1433 samples** from each of the other classes to maintain class balance

---

## 3. Model Architecture
A simple **3-layer feedforward neural network**:

| Layer        | Description                      |
|--------------|----------------------------------|
| Input Layer  | Flattened 64x64x3 image → 12288 features |
| Hidden Layer 1 | Fully connected (12288 → 128), ReLU |
| Hidden Layer 2 | Fully connected (128 → 64), ReLU |
| Output Layer | Fully connected (64 → 3), no activation (logits) |

- **Activation Function**: ReLU (Rectified Linear Unit)
- **Loss Function**: `CrossEntropyLoss()` (suitable for multi-class classification)
- **Optimizer**: `Stochastic Gradient Descent` (SGD)
- **Learning Rate**: `0.01`
- **Epochs**:
  - Initially trained for 10 epochs
  - Improved results observed after extending to 40 epochs

---

## 4. Results

### ✅ Confusion Matrix (on test set)

|                | Predicted: Dog | Predicted: Butterfly | Predicted: Elephant |
|----------------|----------------|-----------------------|---------------------|
| **Actual: Dog**      | 229            | 61                    | 32                  |
| **Actual: Butterfly**| 64             | 155                   | 61                  |
| **Actual: Elephant** | 25             | 59                    | 182                 |

- The model shows **reasonable separation** across the classes, though performance on butterfly was somewhat weaker due to class similarities or training limitations.
- Accuracy can be improved further with more tuning.

---

## 5. Challenges Faced

| Issue | Solution |
|-------|----------|
| **Sigmoid Activation Used Initially** | Initially used sigmoid with Binary Cross Entropy Loss, which caused mismatch with multi-class labels. |
| **Wrong Loss Function** | Realized `BinaryCrossEntropy` is only for binary classification. Switched to `CrossEntropyLoss`, which internally applies softmax. |
| **Unbalanced Dataset** | Original dataset had imbalanced samples. Chose to **limit all classes to 1433 samples** for fair training. |
| **Model Output Format** | Adjusted output layer and label formats to be compatible with `CrossEntropyLoss` (raw logits, integer labels). |

---

## 6. Future Work

- Try increasing **epochs** to improve convergence.
- Tune the **learning rate** for more stable and accurate training.
- Add **data augmentation** for generalization.
- Explore **CNNs** for better image feature extraction.
- Implement accuracy tracking, precision/recall and training graphs.

---

## 7. Conclusion
This project successfully implemented a feedforward neural network to classify animal images into 3 categories. Through experimentation with loss functions, activation choices, and data balancing, we created a baseline model that achieves decent performance. There is room for improvement by increasing complexity, tuning hyperparameters, or switching to convolutional networks.

