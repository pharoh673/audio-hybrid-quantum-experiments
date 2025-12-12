# Hybrid CNN + QNN Audio Classifier

## Included Artifacts
- `confusion_matrix.png`  
  Confusion matrix generated during evaluation


  ---
This repository contains a Google Colab notebook for experimenting with a
**hybrid classical–quantum audio classification model** trained on the
**UrbanSound8K** dataset.

The project focuses on **model architecture, training behavior, checkpointing,
and analysis**, and is mainly intended for **personal experimentation and reference**.

---

## Dataset

- **UrbanSound8K**
- Environmental sound classification dataset with 10 classes

---

## Model Overview

The main model is a **Hybrid CNN + Quantum Neural Network (QNN)**.

### Classical Backbone
- Architecture: `AudioCNNBackboneBig`
- Output embedding dimension: **256**
- Purpose: extract high-level audio features from log-Mel spectrograms

### Quantum Component
- Quantum circuit with **8 qubits**
- **2 variational layers**
- Implemented using **PennyLane**
- Operates on a compressed version of the CNN embedding

### Hybrid Combination
- Classical logits weight: `alpha = 1.0`
- Quantum logits weight: `beta = 0.5`
- Final prediction is a weighted combination of classical and quantum outputs

---

## Training Details

- Training device: **CUDA (GPU)**
- Supports checkpointing and resuming long training runs
- Best model selected based on validation performance
- Training logic and configuration are defined directly in the notebook

---

## Saved Models

Training produces the following model files:

- `final_hybrid_cnn_qnn_model.pth`  
  Final trained hybrid model

- `hybrid_cnn_qnn_best.pth`  
  Best-performing checkpoint during training


> Model weights are not necessarily included in this repository.



---

## Notes

- Full training can be time-consuming and resource-intensive
- Some outputs are precomputed and shown for reference
- The notebook is not intended to be fully re-run from scratch
- This repository is mainly for **experimentation and personal use**

---

## Usage

Open the notebook in **Google Colab**, mount Google Drive if needed,
and run selected cells to inspect the model, training process, or saved results.

---

## Final Note

This repository is intentionally minimal and serves as a **record of experiments**
rather than a production-ready implementation.
