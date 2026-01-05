High Performance and Explainable Two-Level Greek Model for Threat Speech and Target Detection

TITLE
High Performance and Explainable Two-Level Greek Model for Threat Speech and Target Detection

DESCRIPTION
This repository contains the complete implementation of a high-performance and explainable two-level NLP framework for threat speech detection and target identification in Greek-language text. The framework integrates transformer-based deep learning models with explainability techniques to ensure high predictive accuracy and model transparency.

The architecture follows two stages:
1) Threat Detection (Level-1)
2) Target Detection (Level-2)

DATASET INFORMATION
The dataset consists of Greek-language textual data annotated for threatening vs non-threatening speech and threat target categories (individual, group, organisation). Data were collected from publicly available sources where applicable and anonymised according to ethical research standards.

CODE INFORMATION
The codebase includes preprocessing, model training, evaluation, explainability modules, and performance analysis scripts. The structure supports reproducible and extensible research.

USAGE INSTRUCTIONS
1. Clone the repository
2. Install dependencies using requirements.txt
3. Place dataset files in the data directory
4. Run preprocessing scripts
5. Train Level-1 and Level-2 models
6. Run inference and generate explanations

REQUIREMENTS
Python 3.8+
numpy
pandas
scikit-learn
torch
transformers
lime
shap

METHODOLOGY
Data preprocessing, transformer-based threat detection, context-aware target detection, explainability using attention and post-hoc methods, and evaluation using Precision, Recall, and F1-score.

CITATIONS
Malik, M. S. I. Threatening expression and target identification in under-resource languages using NLP techniques. AIST 2023.
Malik, M. S. I. et al. Contextual embeddings based on fine-tuned Urdu-BERT for Urdu threatening content and target identification. Journal of King Saud University – Computer and Information Sciences, 2023.
Rehan, M., Malik, M. S. I., Jamjoom, M. Fine-tuning transformer models using transfer learning for multilingual threatening text identification. IEEE Access, 2023.
Malik, M. S. I. High Performance and Explainable Two-Level Greek Model for Threat Speech and Target Detection. PeerJ Computer Science (under review), 2025.

LICENSE & CONTRIBUTIONS
MIT License. Contributions are welcome via pull requests following ethical AI and data privacy principles.
