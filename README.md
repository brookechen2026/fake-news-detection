# Fake News Detection

A team project for CS410: Text Information Systems at the University of Illinois Urbana-Champaign, Fall 2025.

This project compares traditional machine learning and transformer-based approaches to classifying political news using a PolitiFact subset of FakeNewsNet.

## Methods

- Text preprocessing and exploratory data analysis.
- TF-IDF features from article titles and bodies, combined with seven stylometric features.
- Logistic Regression with hyperparameter selection on a development set.
- Fine-tuning DistilBERT for binary classification.
- Evaluation using accuracy, macro-F1, ROC-AUC, confusion matrices, and error analysis.
- A Tkinter interface for predictions using trained models.

## Results

Results reported in the final course report on a held-out test set of 76 articles:

| Model | Accuracy | Macro-F1 |
|---|---:|---:|
| TF-IDF + Stylometric Features + Logistic Regression | 86.84% | 0.868 |
| DistilBERT | 92.11% | 0.921 |

DistilBERT reduced classification errors from 10 to 6, a 40% reduction. Saved output from another notebook run contains different DistilBERT results; the table above follows the final report.

## My Contribution

I contributed to data preprocessing, exploratory analysis, baseline modeling, and interpretation of model results within the team project.

## Repository Contents

- `scripts/preprocessing.py`: Extract and clean article data.
- `scripts/data_analysis.py`: Exploratory statistics and visualizations.
- `scripts/train_baseline.py`: Train the Logistic Regression baseline and create data splits.
- `scripts/train_BERT.py`: Fine-tune and evaluate DistilBERT.
- `scripts/evaluate.py`: Baseline evaluation and error analysis.
- `scripts/software_deploy.py`: Desktop prediction interface.
- `scripts/run_all.ipynb`: Notebook workflow.
- `CS_410_FinalReport.pdf`: Final course report.
- `SETUP.md`: Setup details and implementation limitations.

## Scope and Limitations

The supplied models use article text and stylometric features. Social-network and propagation features were considered in the project framing but are not inputs to these classifiers.

Results are exploratory and based on a small test set. The application predicts dataset labels; it does not independently verify factual claims.

## Team

Fred Hou, Yixiang Zhang, Xiaoxi Chen, and Xiaoxiong Lei.

## Data Source

[FakeNewsNet](https://github.com/KaiDMML/FakeNewsNet)
