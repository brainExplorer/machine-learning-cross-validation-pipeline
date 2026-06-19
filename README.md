# 🧠 Preventing Data Leakage with Cross Validation & Scikit-Learn Pipeline

A practical Machine Learning notebook demonstrating the importance of **Cross Validation**, **Scikit-Learn Pipeline**, and preventing **Data Leakage** during model evaluation.

This project compares incorrect and correct preprocessing workflows and explains why using a Pipeline is considered a Machine Learning best practice.

---

## 📌 Project Overview

Data leakage is one of the most common mistakes in Machine Learning. It occurs when information from the validation or test data unintentionally influences the training process, leading to overly optimistic performance estimates.

In this notebook, you'll learn how to properly evaluate a classification model using Cross Validation while avoiding data leakage with Scikit-Learn's `Pipeline`.

---

## 🚀 Topics Covered

- Train/Test Split
- Manual K-Fold Cross Validation
- Automatic Cross Validation (`cross_val_score`)
- Stratified K-Fold Cross Validation
- Feature Scaling with `StandardScaler`
- Logistic Regression
- Scikit-Learn Pipeline
- Preventing Data Leakage
- Final Test Set Evaluation

---

## 📂 Dataset

The project uses the **Breast Cancer Wisconsin Dataset**, which is included in Scikit-Learn.

```python
from sklearn.datasets import load_breast_cancer
```

No external dataset is required.

---

## 🛠 Technologies

- Python
- NumPy
- Pandas
- Scikit-Learn
- Jupyter Notebook

---

## 📖 Notebook Workflow

### 1. Load Dataset

- Import the Breast Cancer dataset
- Create feature and target variables

### 2. Train/Test Split

- Separate training and testing data

### 3. Manual Cross Validation

- Perform K-Fold Cross Validation manually
- Train and evaluate the model for each fold

### 4. Automatic Cross Validation

- Use `cross_val_score()` for model evaluation

### 5. Stratified K-Fold

- Preserve class distribution across folds

### 6. Feature Scaling

- Apply `StandardScaler`
- Compare preprocessing strategies

### 7. Pipeline

- Build a Scikit-Learn Pipeline
- Prevent Data Leakage by performing scaling inside each fold

### 8. Final Evaluation

- Train the final model
- Evaluate performance on the unseen test set

---

## ⚠️ Why Pipeline Matters

### ❌ Incorrect Workflow

```text
Scale Entire Dataset
        ↓
Cross Validation
        ↓
Model Training
```

The validation data influences the scaling process, causing **Data Leakage**.

---

### ✅ Correct Workflow

```text
Cross Validation
        ↓
Scaling (inside each fold)
        ↓
Model Training
        ↓
Validation
```

Using a **Pipeline** ensures preprocessing is performed independently for each training fold.

---

## 📈 Learning Outcomes

By completing this notebook, you will understand:

- Why Data Leakage is dangerous
- How Cross Validation works
- When to use Stratified K-Fold
- How Scikit-Learn Pipeline prevents leakage
- Best practices for evaluating Machine Learning models

---

## 📁 Repository Structure

```text
.
├── CV&Pipeline.ipynb
├── README.md
└── requirements.txt
```

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/preventing-data-leakage-with-pipeline.git
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Or install them manually:

```bash
pip install numpy pandas scikit-learn jupyter
```

---

## ▶️ Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
CV&Pipeline.ipynb
```

---

## 💡 Key Takeaway

> **Always perform preprocessing inside Cross Validation.**

Using a **Pipeline** ensures that every preprocessing step is learned only from the training fold, preventing Data Leakage and producing reliable evaluation results.

---

## 🤝 Contributions

Suggestions and improvements are always welcome!

If you find this project useful, feel free to ⭐ the repository.

---

## 👨‍💻 Author

**Ümit Yavuz**

Python • Machine Learning • Data Analysis • Test Automation
