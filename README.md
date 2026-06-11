# Adversarial Machine Learning for Cybersecurity

This repository demonstrates the application of adversarial machine learning techniques against a neural network-based Intrusion Detection System (IDS). The project evaluates how carefully crafted adversarial examples can degrade model performance and explores defensive strategies for improving robustness.

## Research Objectives

Modern cybersecurity platforms increasingly rely on machine learning models to detect malicious activity. While these systems achieve high accuracy under normal operating conditions, they can be vulnerable to adversarial attacks that manipulate input features or model parameters.

This repository investigates:

* Fast Gradient Sign Method (FGSM)
* Projected Gradient Descent (PGD)
* Adversarial Weight Perturbation (AWP)

and their impact on machine learning-based intrusion detection.

---

## Projects

### FGSM Attack

**Notebook:** `AI-Cybersecurity_FGSM Attack.ipynb`

Implements the Fast Gradient Sign Method to generate adversarial network traffic samples designed to evade intrusion detection.

Topics:

* Gradient-based attacks
* Adversarial examples
* IDS evasion
* Model robustness evaluation

---

### PGD Attack

**Notebook:** `AI-Cybersecurity_PGD Attack.ipynb`

Implements Projected Gradient Descent, a stronger iterative attack that repeatedly perturbs inputs while remaining within a constrained perturbation budget.

Topics:

* Iterative adversarial attacks
* White-box attacks
* Robustness testing
* Worst-case adversarial examples

---

### Adversarial Weight Perturbation (AWP)

**Notebook:** `AI-Cybersecurity_AWP Attack.ipynb`

Evaluates model robustness by perturbing neural network weights and measuring degradation in detection performance.

Topics:

* Adversarial training
* Weight-space attacks
* Neural network robustness
* Secure AI systems

---

## Technologies

* Python
* PyTorch
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib

---

## Metrics Evaluated

* Classification Accuracy
* Attack Success Rate
* Receiver Operating Characteristic (ROC)
* Area Under Curve (AUC)
* Model Robustness

---

## Key Findings

This research demonstrates that even highly accurate intrusion detection systems can be vulnerable to adversarial manipulation. As attack sophistication increases from FGSM to PGD and weight-space perturbation methods, model performance degrades significantly unless defensive measures are implemented.

---

## Author

Greg Mamoyac

Information Security | Cybersecurity Research | Machine Learning Security

California State University, Los Angeles
