# 🚨 Intrusion Detection Using Supervised and Unsupervised Machine Learning

This project presents a comparative study of **supervised** and **unsupervised** machine learning algorithms for **intrusion detection** using the NSL-KDD dataset. The objective is to classify network traffic as either **normal** or **attack**, and evaluate model performance using classification metrics and ROC-AUC.

---

## 📂 Dataset

- **NSL-KDD Dataset**  
- Consists of:
  - **41 features**
  - **1 label** (`normal` or specific attack type)
  - **1 attack category** (not used in this binary classification)
- Label is preprocessed into a binary format: `normal` vs `attack`

---

## 🧠 Models Used

### ✅ Supervised Learning
| Model                 | Description                     |
|----------------------|---------------------------------|
| Logistic Regression   | Linear classifier               |
| Random Forest         | Ensemble of decision trees      |
| Support Vector Machine (SVM) | Margin-based classifier     |
| K-Nearest Neighbors   | Instance-based learning         |

### 🚫 Unsupervised Learning
| Model                | Description                      |
|---------------------|----------------------------------|
| Isolation Forest     | Tree-based anomaly detector      |
| One-Class SVM        | Learns the boundary of normal data |

---

## ⚙️ Workflow

1. Load and label NSL-KDD data
2. Encode categorical features
3. Normalize numerical features
4. Train supervised and unsupervised models
5. Evaluate using:
   - `classification_report`
   - ROC Curve + AUC
6. Visual comparison of model performance

---

## 📈 ROC Curve

All models are evaluated using ROC-AUC to compare performance between:
- Supervised learning (trained on labeled data)
- Unsupervised learning (trained only on normal traffic)


---

## 🧪 Results Snapshot

| Model              | Precision | Recall | F1-Score | AUC     |
|-------------------|-----------|--------|----------|---------|
| Random Forest      | High      | High   | High     | 0.99+   |
| SVM                | Medium    | High   | Medium   | ~0.95   |
| Isolation Forest   | Lower     | Lower  | Medium   | ~0.88   |
| One-Class SVM      | Lower     | Lower  | Medium   | ~0.84   |

*(Actual results may vary depending on data preprocessing and hyperparameters.)*

---

## 💻 Requirements

```bash
pip install pandas numpy matplotlib scikit-learn torch
