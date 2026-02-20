# 💳 Credit Card Fraud Detection — Business-Driven Logistic Regression

A complete end-to-end fraud detection project using **Logistic Regression** on the Kaggle Credit Card Fraud dataset. This notebook goes beyond model accuracy — it focuses on **business interpretability**, **cost-sensitive threshold optimization**, and **real-world deployment considerations**.

---

## 🎯 Project Objective

Build a fraud detection classifier that is:
- **Interpretable** — coefficients explainable to regulators & compliance teams
- **Business-aligned** — threshold tuned for real-world cost asymmetry (missed fraud vs. false alarms)
- **Production-aware** — evaluated using metrics that matter, not just accuracy

---

## 📊 Key Highlights

| Aspect | Details |
|---|---|
| **Algorithm** | Logistic Regression with `class_weight='balanced'` |
| **Dataset** | 284,807 transactions, 492 fraudulent (0.17%) |
| **Evaluation** | ROC-AUC, Precision-Recall Curve, Confusion Matrix |
| **Threshold Strategies** | Default (0.5), ROC-Optimal (FPR ≤ 5%), PR Equilibrium |
| **Focus** | Business decision-making, not just model training |

---

## 📁 Project Structure

```
Credit-Card-Fraud-Detection/
├── assets/
│   ├── slide1_roc_curve.png          # ROC curve visualization
│   ├── slide2_pr_curve.png           # Precision-Recall curve visualization
│   └── slide3_threshold_tradeoff.png # Threshold trade-off analysis plot
├── data/
│   └── creditcard.csv                # Dataset (download from Kaggle)
├── notebook.ipynb                    # Main analysis notebook
└── README.md                         # This file
```

---

## 🔬 Notebook Walkthrough

| Step | Title | Description |
|---|---|---|
| 1 | Import Libraries | pandas, sklearn, matplotlib, seaborn, numpy |
| 2 | Load Dataset | Load & inspect the credit card transactions dataset |
| 3 | Class Imbalance Analysis | Quantify the 99.83% vs 0.17% imbalance |
| 4 | Train/Test Split | Stratified 70/30 split preserving class ratios |
| 5 | Feature Scaling | StandardScaler on `Time` and `Amount` (no data leakage) |
| 6 | Model Training | Logistic Regression with balanced class weights |
| 7 | Initial Evaluation | Confusion matrix & classification report at default threshold |
| 8 | Threshold Tuning | Impact analysis across 8 threshold values |
| 9 | ROC Curve | ROC-AUC + optimal threshold at FPR ≤ 5% |
| 10 | Precision-Recall Curve | PR curve + precision-recall equilibrium point |
| 11 | Threshold Comparison | Side-by-side comparison of all strategies |

---

## 💡 Key Business Insights

1. **Accuracy is misleading** — A naive model predicting all transactions as legitimate achieves 99.83% accuracy but catches zero fraud.

2. **Threshold is a business decision** — The optimal cutoff depends on `Cost(Missed Fraud) / Cost(False Alarm)`, not on statistical defaults.

3. **Class weighting alone is insufficient** — `class_weight='balanced'` must be paired with threshold tuning and proper metric selection.

4. **Interpretability drives adoption** — Logistic Regression was chosen over black-box models because banking regulators require explainability.

---

## 🛠️ Tech Stack

- **Python 3.x**
- **pandas** — data manipulation
- **scikit-learn** — modeling, metrics, preprocessing
- **matplotlib / seaborn** — visualization
- **numpy** — numerical operations

---

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/MuhammadTaha1038/Credit-Card-Fraud-Detection.git
cd Credit-Card-Fraud-Detection
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
Download `creditcard.csv` from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and place it in the `data/` folder.

### 4. Run the notebook
```bash
jupyter notebook notebook.ipynb
```

---

## 📈 Sample Results

### Threshold Comparison (example output)

| Strategy | Precision | Recall | F1 | False Positives | Missed Fraud |
|---|---|---|---|---|---|
| Default (0.50) | — | — | — | — | — |
| ROC-Optimal | — | — | — | — | — |
| PR Equilibrium | — | — | — | — | — |

> *Run the notebook to see actual values based on the dataset.*

---

## 📝 Dataset Information

- **Source:** [Kaggle — Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Transactions:** 284,807 (made by European cardholders in September 2013)
- **Fraud cases:** 492 (0.172%)
- **Features:** `V1-V28` (PCA-transformed), `Time`, `Amount`, `Class`
- **Privacy:** Features are anonymized due to PCI-DSS compliance

---

## 📄 License

This project uses the [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) provided under the [Database Contents License (DbCL)](http://opendatacommons.org/licenses/dbcl/1.0/).

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for:
- Additional threshold optimization techniques
- Ensemble model comparisons
- Feature importance / odds ratio analysis
- Deployment pipeline examples

---

*Built as part of a machine learning portfolio project focused on classification with business impact.*

---

##   Contact

For questions or feedback, please open an issue on GitHub.

---
## Connect with me
Name: Muhammad Taha \
Email: contact.taha2005@gmail.com

 <div style="text-align: left; font-size: 20px; color: gray;">
 <a href="https://linkedin.com/in/muhammad-taha-b88807248/" target="_blank" style="text-decoration: none;">
            <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" width="80" />
        </a>
        <p> Linkedin</p>
</div>

*Created: January 2026 | Data Source: Yahoo Finance (SI=F)*