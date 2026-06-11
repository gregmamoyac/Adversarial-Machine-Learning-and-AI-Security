# Adversarial Machine Learning for Cybersecurity

This repository presents a research series evaluating the vulnerability of neural network-based intrusion detection systems (IDS) to adversarial machine learning attacks. Using a cybersecurity network traffic dataset, a feedforward neural network is trained as the IDS victim model and subjected to three progressively sophisticated adversarial attack techniques: Fast Gradient Sign Method (FGSM), Projected Gradient Descent (PGD), and Adversarial Weight Perturbation (AWP). Each notebook follows a consistent pipeline — data loading, feature engineering, model training, attack implementation, and multi-metric evaluation — allowing direct comparison across attack types. The central hypothesis across all three studies is that adversarial attacks, even when constrained to small perturbation budgets, can significantly degrade IDS detection performance, with more iterative and weight-space attacks proving increasingly effective at evading detection. This work serves as a proof of concept for understanding adversarial threats to AI-driven security systems and motivates the need for robust defenses in real-world deployments.

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

Across all three notebooks, the results consistently demonstrate that neural network-based intrusion detection systems are meaningfully vulnerable to adversarial manipulation. FGSM established that even a single-step perturbation is sufficient to drive model accuracy below 25% and push attack success rates above 65% at modest epsilon values. 

PGD extended this finding by showing that iterative attacks within the same perturbation budget are substantially more destructive, converging to near-worst-case adversarial examples that collapse the model's ROC AUC toward random chance. AWP introduced a fundamentally different threat vector — attacking the model's internal weights rather than its inputs — and revealed that standard training produces models in sharp loss landscape minima that are brittle to parameter-space perturbations, while AWP-augmented training produces more resilient flat minima. 

Together, these three studies form a layered picture of adversarial risk: input-space attacks like FGSM and PGD represent deployment-time threats where adversaries craft malicious network traffic, while weight-space attacks like AWP represent infrastructure threats such as model poisoning or tampering. Effective defense of AI-driven security systems will require combining adversarial training, robust architecture choices, and model integrity verification to address threats across all of these dimensions.

---

## Author

Greg Mamoyac

Information Security | Cybersecurity Research | Machine Learning Security

