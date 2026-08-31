# Week 1: Python ML Fundamentals & Credit Risk Basics

## Learning Objectives

By the end of Week 1, you will:
- [ ] Understand ML classification fundamentals
- [ ] Master scikit-learn API for model building
- [ ] Evaluate models using credit-specific metrics (Gini, KS, AUC)
- [ ] Implement cross-validation and hyperparameter tuning
- [ ] Build a basic credit scoring model

## Time Allocation (50 hours)

- **Monday (10h):** Theory & setup
- **Tuesday-Thursday (30h):** Hands-on coding & exercises
- **Friday (10h):** Project completion & deliverables

## Study Materials

### Core Resources

1. **scikit-learn/scikit-learn** (10 hours)
   - URL: https://github.com/scikit-learn/scikit-learn
   - Read: `/examples/classification/` directory
   - Focus:
     - `plot_classifier_comparison.py` (2h)
     - `plot_logistic_regression.py` (1h)
     - `plot_tree_regression.py` (1h)
     - `plot_ensemble_methods.py` (2h)
   - Documentation: Model evaluation metrics section

2. **rasbt/python-machine-learning-book-3rd-edition** (8 hours)
   - URL: https://github.com/rasbt/python-machine-learning-book-3rd-edition
   - Chapters:
     - Ch 03: Classification (3h)
     - Ch 06: Decision Trees & Ensemble Methods (2h)
     - Appendix: Model Evaluation (1h)

3. **ageron/handson-ml3** (6 hours)
   - URL: https://github.com/ageron/handson-ml3
   - Chapters:
     - Ch 2: End-to-End ML Project (3h)
     - Ch 3: Classification (3h)

## Environment Setup

### Python Installation

```bash
# Create virtual environment
python3.10 -m venv credit-risk-env
source credit-risk-env/bin/activate  # Linux/Mac
# or
credit-risk-env\Scripts\activate  # Windows

# Upgrade pip
pip install --upgrade pip

# Install core libraries
pip install jupyter jupyterlab
pip install numpy pandas pandas-profiling
pip install scikit-learn scikit-optimize
pip install matplotlib seaborn plotly
pip install xgboost lightgbm
pip install shap lime
pip install scipy statsmodels
```

### Verify Installation

```python
# test_setup.py
import numpy as np
import pandas as pd
import sklearn
import xgboost as xgb
import matplotlib.pyplot as plt

print(f"NumPy: {np.__version__}")
print(f"Pandas: {pd.__version__}")
print(f"scikit-learn: {sklearn.__version__}")
print(f"XGBoost: {xgb.__version__}")
print("\n✅ All libraries installed successfully!")
```

## Day-by-Day Schedule

### Monday: Theory & Environment

**Morning (3h):**
1. Read scikit-learn documentation overview (1h)
2. Watch scikit-learn tutorial video (30min)
3. Run example notebooks from scikit-learn (1.5h)

**Afternoon (3h):**
1. Read rasbt Ch 03 Introduction (1h)
2. Run classification examples (2h)

**Evening (4h):**
1. Read ageron Ch 2 (1h)
2. Set up project directory structure
3. Create first ML project notebook

### Tuesday: Classification Fundamentals

**Morning (3h):**
1. Study Logistic Regression (1.5h)
2. Implement from scratch (1.5h)

**Afternoon (4h):**
1. Study Decision Trees (2h)
2. Implement & visualize (2h)

**Evening (3h):**
1. Study ensemble methods overview
2. Run Random Forest examples

### Wednesday: Model Evaluation

**Morning (3h):**
1. Confusion Matrix & metrics (1h)
2. ROC-AUC, Precision-Recall (1h)
3. Cross-validation techniques (1h)

**Afternoon (4h):**
1. Implement credit-specific metrics:
   - Gini coefficient (1.5h)
   - KS statistic (1.5h)
   - Concordance (1h)

**Evening (3h):**
1. Hyperparameter tuning (Grid/Random Search)
2. Learning curves analysis

### Thursday: Hands-On Project

**Morning (3h):**
1. Load UCI Credit dataset (30min)
2. Basic data exploration (1.5h)
3. Data preprocessing (1h)

**Afternoon (4h):**
1. Train 3 models: Logistic Regression, Decision Tree, Random Forest (2h)
2. Compare performance metrics (1h)
3. Feature importance analysis (1h)

**Evening (3h):**
1. Optimization: Hyperparameter tuning
2. Cross-validation comparison
3. Documentation

### Friday: Project Completion

**Morning (3h):**
1. Complete model comparison notebook (1.5h)
2. Create visualizations (1.5h)

**Afternoon (3h):**
1. Write summary report
2. Documentation & comments
3. Prepare presentation

**Evening (4h):**
1. Polish notebook
2. Self-review & QA
3. Reflection & notes for Week 2

## Practical Exercises

### Exercise 1: Build Logistic Regression Model

```python
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, roc_auc_score, confusion_matrix

# Load data (UCI Credit dataset)
X = df[features]
y = df['default']

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)

# Train model
model = LogisticRegression(random_state=42)
model.fit(X_train, y_train)

# Evaluate
y_pred = model.predict(X_test)
y_pred_proba = model.predict_proba(X_test)[:, 1]

print(f"Accuracy: {accuracy_score(y_test, y_pred):.3f}")
print(f"AUC-ROC: {roc_auc_score(y_test, y_pred_proba):.3f}")
print(f"Confusion Matrix:\n{confusion_matrix(y_test, y_pred)}")
```

### Exercise 2: Gini Coefficient Calculation

```python
def calculate_gini(y_true, y_pred_proba):
    """
    Calculate Gini coefficient for binary classification.
    Gini = 2 * AUC - 1
    Ranges from -1 to 1 (1 = perfect prediction)
    """
    from sklearn.metrics import roc_auc_score
    auc = roc_auc_score(y_true, y_pred_proba)
    gini = 2 * auc - 1
    return gini

# Example usage
gini = calculate_gini(y_test, y_pred_proba)
print(f"Gini: {gini:.3f}")
```

### Exercise 3: Model Comparison

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.tree import DecisionTreeClassifier

models = {
    'Logistic Regression': LogisticRegression(),
    'Decision Tree': DecisionTreeClassifier(),
    'Random Forest': RandomForestClassifier(n_estimators=100)
}

results = {}
for name, model in models.items():
    model.fit(X_train, y_train)
    y_pred = model.predict(X_test)
    y_pred_proba = model.predict_proba(X_test)[:, 1]
    
    results[name] = {
        'Accuracy': accuracy_score(y_test, y_pred),
        'AUC-ROC': roc_auc_score(y_test, y_pred_proba),
        'Gini': calculate_gini(y_test, y_pred_proba)
    }

import pandas as pd
results_df = pd.DataFrame(results).T
print(results_df)
```

## Deliverables

### Deliverable 1: Environment Setup (Monday)
- [ ] Python 3.10+ installed
- [ ] Virtual environment created
- [ ] All libraries installed
- [ ] `test_setup.py` runs successfully
- [ ] Jupyter lab launches

### Deliverable 2: Theory Notebook (Wednesday)
- [ ] Summary of classification algorithms (1-2 pages)
- [ ] Model evaluation metrics explanation (2-3 pages)
- [ ] Code examples for each algorithm
- [ ] Hyperparameter tuning patterns

### Deliverable 3: Credit Scoring Model (Friday)
- [ ] Jupyter notebook with complete analysis
- [ ] Data exploration (EDA) section
- [ ] 3+ trained models
- [ ] Performance comparison table
- [ ] Feature importance analysis
- [ ] Conclusions & recommendations

### Deliverable 4: Summary Report
- [ ] 5-page report covering:
  - Model selection rationale
  - Performance metrics comparison
  - Key insights
  - Recommendations for Week 2

## Resources

- **Scikit-learn docs:** https://scikit-learn.org/
- **Gini coefficient:** https://en.wikipedia.org/wiki/Gini_coefficient
- **ROC curves:** https://scikit-learn.org/stable/modules/model_evaluation.html#roc-metrics
- **Cross-validation:** https://scikit-learn.org/stable/modules/cross_validation.html

## Key Takeaways

1. **Logistic Regression** = Linear model for binary classification
2. **Decision Trees** = Interpretable, prone to overfitting
3. **Random Forest** = Ensemble of trees, better generalization
4. **Gini coefficient** = Key metric for credit models (2*AUC-1)
5. **Cross-validation** = Essential for robust performance estimation
6. **Hyperparameter tuning** = Critical for model optimization

## Next Week Preview

Week 2 builds on this foundation with:
- Advanced feature engineering techniques
- Handling class imbalance (SMOTE)
- Data pipeline development
- Preparing for credit risk-specific models

---

**Good luck with Week 1! 🚀**