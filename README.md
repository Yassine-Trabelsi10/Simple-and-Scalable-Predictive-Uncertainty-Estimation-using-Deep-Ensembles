# Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles

Partial reproduction of the paper:

> Lakshminarayanan, B., Pritzel, A., & Blundell, C. (2017).  
> *Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles*.  

## Author

**Yassine Trabelsi**  
EURECOM – Master in Computer Science (Data Science)  
Advanced Statistical Inference – Group 30

---

## Project Overview

This project reproduces several key results from the paper *Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles*.

Deep Ensembles estimate predictive uncertainty by training multiple neural networks independently and averaging their predictions. The method provides reliable uncertainty estimates without requiring complex Bayesian inference techniques.

The reproduction focuses on four representative experiments from the paper:

1. Toy Regression Uncertainty
2. MNIST Deep Ensemble Classification
3. Effect of Ensemble Size
4. Out-of-Distribution (OOD) Uncertainty

---

## Reproduced Results

### 1. Toy Regression Uncertainty

A probabilistic neural network predicts both mean and variance. Multiple independently initialized models are combined into an ensemble.

**Observation:**  
Uncertainty remains low near training data and increases significantly outside the observed region.

---

### 2. MNIST Deep Ensemble Classification

Five neural networks are trained independently on MNIST and combined into a Deep Ensemble.

Metrics reported:

- Accuracy
- Negative Log-Likelihood (NLL)
- Brier Score

**Observation:**  
The ensemble achieves high classification performance while maintaining meaningful uncertainty estimates.

---

### 3. Effect of Ensemble Size

Ensembles of different sizes are evaluated:

- M = 1
- M = 3
- M = 5

Metrics:

- Classification Error
- NLL
- Brier Score

**Observation:**  
Increasing ensemble size improves uncertainty-related metrics, especially NLL and Brier Score.

---

### 4. Out-of-Distribution Uncertainty

MNIST is used as the in-distribution dataset and FashionMNIST as an out-of-distribution dataset.

Predictive entropy is computed for both datasets.

**Observation:**  
The ensemble assigns substantially higher entropy to FashionMNIST samples, indicating greater uncertainty on unfamiliar inputs.

---

## Repository Structure

```text
.
├── deep_ensembles_colab_notebook.ipynb
├── Report.pdf
├── figures/
│   ├── toy_regression.png
│   ├── mnist_metrics.png
│   ├── ensemble_size_effect.png
│   └── predictive_entropy.png
└── README.md
```

---

## Requirements

Main libraries:

```bash
numpy
pandas
matplotlib
scikit-learn
torch
torchvision
```

---

## Running the Notebook

Open:

```text
deep_ensembles_colab_notebook.ipynb
```

in:

- Google Colab
- Jupyter Notebook

and execute all cells sequentially.

---

## Report

The full reproduction report is available in:

```text
Report.pdf
```

The report follows the NeurIPS format and includes:

- Summary of the paper
- Reproduced experiments
- Discussion of results
- Conclusion
- AI use disclosure

---

## Reference

```bibtex
@inproceedings{lakshminarayanan2017deepensembles,
  title={Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles},
  author={Lakshminarayanan, Balaji and Pritzel, Alexander and Blundell, Charles},
  booktitle={Advances in Neural Information Processing Systems},
  year={2017}
}
```

---

## Disclaimer

This repository contains a **partial reproduction** of the original paper for educational purposes as part of the Advanced Statistical Inference course at EURECOM. The goal is to reproduce representative experiments illustrating the main ideas and conclusions of the paper rather than every benchmark reported by the authors.
