# Explainable Two-Level Greek Model for Threat Speech and Target Detection

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8%2B-brightgreen.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Deep_Learning-EE4C2C.svg)](https://pytorch.org/)

A Natural Language Processing project for detecting **threatening expressions in Greek text** and identifying **threat targets** using transformer-based deep learning and explainable AI techniques.

The framework addresses two classification tasks:

### Level 1 — Threat Speech Detection

* **0 — Non-Threatening**
* **1 — Threatening**

### Level 2 — Target Detection

* **0 — Group**
* **1 — Individual**

The current target-detection notebooks implement binary classification between **Group** and **Individual**.

---

## 🏗️ Models & Architectures

This repository fine-tunes **LaBSE** (`setu4993/LaBSE`) through Hugging Face Transformers for Greek threat speech detection and target classification.

The notebooks include:

* **Threat detection** — Classification of text as threatening or non-threatening.
* **Target detection** — Classification of threat targets as a group or an individual.
* **SHAP** — Token contribution visualizations, bar plots, and waterfall plots.
* **LIME** — Local explanations showing word contributions to predictions.
* **Attention visualization** — Exploration of token attention patterns in `Methodologies_1.ipynb`.

Evaluation includes **Accuracy, weighted Precision, weighted Recall, weighted F1-score**, and confusion-matrix counts.

---

## 📁 Repository Structure

| File | Description |
| --- | --- |
| `README.md` | Project overview and setup instructions |
| `LaBSE.ipynb` | LaBSE training and evaluation for threat detection |
| `Methodologies_1.ipynb` | Threat detection experiments, attention visualization, and SHAP analysis |
| `Target_identification-fine-tunning.ipynb` | Target classification training, evaluation, and explanation experiments |
| `SHAP_LIME_(first_task)_.ipynb` | SHAP and LIME analysis for threat detection |
| `SHAP_LIME_(for_first_task_non_threat).ipynb` | Explanation examples for non-threatening text |
| `SHAP_LIME_(second_task)_.ipynb` | SHAP and LIME experiments for target classification |
| `SHAP_LIME_(for_second_task_Group_target).ipynb` | Explanation examples for group targets |

---

## 🚀 Installation & Setup

Clone the repository:

```bash
git clone https://github.com/MSIMALIK/Explainable-Two-Level-Greek-Model-for-Threat-Speech-and-Target-Detection-.git
cd Explainable-Two-Level-Greek-Model-for-Threat-Speech-and-Target-Detection-
```

Install the dependencies used by the notebooks:

```bash
pip install "transformers==4.28.0" datasets torch tensorflow numpy pandas scikit-learn scipy matplotlib seaborn shap lime openpyxl jupyter
```

The notebooks specify **Transformers 4.28.0**. A `requirements.txt` file is not currently included.

Open the notebooks in **Jupyter Notebook** or **Google Colab**. A CUDA-enabled GPU is required for the SHAP cells that call `.cuda()` directly.

### Dataset Setup

Provide the following CSV files and update their paths in the notebooks:

| Task | Required files | Required columns |
| --- | --- | --- |
| Threat detection | `train_dataset.csv`, `validation_dataset.csv`, `test_dataset.csv` | `Translated_Text`, `label` |
| Target detection | `train_target_dataset.csv`, `validation_target_dataset.csv`, `test_target_dataset.csv` | `Translated_Text`, `Targets (1-Individual, 0-Group)` |

The notebooks currently read these files from `/content/`. Dataset files are not included in the current repository.

Run the relevant training notebook, review validation and test metrics, and use the explanation notebooks to inspect individual predictions.

Some target-classification notebooks retain generic LIME class names. Set them to `['Group', 'Individual']` before interpreting target explanations.

---

## ⚠️ Content Notice

The data and notebook examples may contain threatening, abusive, or sensitive Greek expressions because such examples are required for training and evaluating threat-detection models.

The content is included solely for research and academic purposes.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👤 Author

**Muhammad Shahid Iqbal Malik**  
GitHub: [@MSIMALIK](https://github.com/MSIMALIK)

