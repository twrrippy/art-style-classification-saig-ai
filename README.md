# 🎨 Art Style Classification Project

This repository contains the final submission for the **Art Style Classification** project.  
The model is trained on a dataset of 11 classes (10 known + 1 hidden "UNK" class for evaluation).

---

## 📂 Files in this Repository

- **`notebook12-2.ipynb`**  
  Jupyter Notebook containing the full workflow: data preparation, model training (EfficientNetV2B0), evaluation, and inference.

- **`final.weights (1).h5`**  
  The trained model weights (Keras format, weights-only).  
  Use this file together with the notebook to reproduce predictions.

---

## 🧩 Model Details

- **Backbone:** EfficientNetV2B0 (`tf.keras.applications.EfficientNetV2B0`)
- **Image size:** 256 × 256
- **Classes (11 total):**
  - Ink scenery  
  - comic  
  - cyberpunk  
  - futuristic UI  
  - lowpoly  
  - oil painting  
  - pixel  
  - realistic  
  - steampunk  
  - water color  
  - UNK (only appears in test/hidden set)

- **Training strategy:**
  - Stage 1: Train head with backbone frozen
  - Stage 2: Fine-tune with partial unfreeze
  - Loss: SparseCategoricalCrossentropy
  - Optimizer: Adam / AdamW
  - Validation split: 20%

---

## 🚀 How to Use

1. Clone this repo and install dependencies (TensorFlow 2.15+ recommended).

2. Open `notebook12-2.ipynb` in Kaggle/Colab/your local Jupyter environment.

3. Rebuild the same model architecture (see notebook).
