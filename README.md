# Galaxy Morphology Classification using Deep Learning & Explainable AI (SHAP)

## Overview

This project focuses on classifying galaxy morphologies using the Galaxy Zoo dataset from Kaggle. A deep learning model will be trained to identify different galaxy types, and SHAP (SHapley Additive exPlanations) will be used to explain the model's predictions.

## Objectives

- Explore and understand the Galaxy Zoo dataset.
- Perform label engineering from the original probability-based annotations.
- Train a deep learning image classification model.
- Evaluate model performance.
- Explain predictions using SHAP.
- Maintain a clean and reproducible ML workflow.

---

## Dataset

- **Source:** Kaggle – Galaxy Zoo: The Galaxy Challenge
- **Images:** 61,578 training images
- **Labels:** 37 probability-based morphology labels

---

## Project Structure

```
Galaxy Classification/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── docs/
├── notebooks/
├── models/
├── outputs/
├── src/
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Progress

- [x] Project setup
- [x] Dataset download
- [x] Dataset exploration
- [x] Label engineering
- [x] Image exploration
- [x] Data preparation
- [ ] Model training (ResNet18)
- [ ] Model evaluation
- [ ] SHAP Explainability
---

## Current Status

**Phase 1:** ✅ Data Collection & Understanding

**Phase 2:** ✅ Data Preparation

**Phase 3:** 🟡 Model Development (Next)

**Phase 4:** ⏳ Explainable AI (SHAP)

**Phase 5:** ⏳ Final Evaluation

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- PyTorch
- SHAP
- OpenCV

---

## License

This project is developed for learning and portfolio purposes.