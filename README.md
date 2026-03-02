

---

# 🧠 Job Interview Guide Workshop

**Machine Learning Interview Preparation — Junior Data Scientist (Canada Focus 🇨🇦)**

---

## 📌 Project Overview

This repository contains a structured, end-to-end Machine Learning interview preparation workshop. The goal of this project is to strengthen core ML fundamentals, simulate real interview environments, identify knowledge gaps, and reinforce weak areas through targeted exercises.

The workshop integrates:

* Conceptual ML theory
* Practical implementation (scikit-learn)
* Interview-style quizzes
* FAANG-level technical questioning
* Behavioral STAR preparation
* Canadian hiring panel simulation
* Math-heavy derivation stress testing

This repository demonstrates both technical competence and structured self-improvement.

---

## 📂 Repository Structure

```
JOBINTERVIEWGUIDE_WORKSHOP-MAIN/
│
├── StudyMaterials.zip
├── StudyGuide.txt
├── JobInterviewGuide_Workshop_SumanthR...ipynb
├── JobInterviewGuide_Workshop_ParamRasa...ipynb
├── JobInterviewGuide_Workshop_VirajMistry...ipynb
├── requirements.txt
└── README.md
```

---

## 🎯 Objectives

This workshop was designed to:

* Reinforce supervised vs. unsupervised learning fundamentals
* Clarify dependent vs. independent variables
* Apply disciplined train/validation/test splits
* Interpret regression metrics (MSE, R²)
* Understand logistic regression (log-odds, cross-entropy)
* Tune KNN hyperparameters properly
* Explain decision tree leaf predictions
* Diagnose overfitting vs underfitting
* Practice real-world ML communication

---

# JobInterviewGuide Workshop — Targeted Practice Notebook

This repository contains a Jupyter Notebook focused on **targeted interview practice** for common AI/ML concepts that are frequently tested in quizzes and job interviews.  
The notebook follows a workshop format: **short talking points + clear steps + sanity checks + mini exercises**.

## Notebook
- `JobInterviewGuide_Workshop_VirajMistry.ipynb`

## What this notebook covers
The notebook focuses on topics that are common in interviews and quizzes:

1. **Data Leakage + correct Train/Val/Test usage**
   - What leakage is and why it causes “too good to be true” validation scores
   - Best-practice workflow: split → fit preprocessing on train → evaluate on val/test

2. **Scaling Leakage (the subtle one)**
   - Why fitting scalers/encoders on full data leaks information
   - Correct solution using scikit-learn Pipelines / ColumnTransformer

3. **Metrics for Imbalanced Classification**
   - Why accuracy can be misleading (e.g., 1% positive class)
   - Precision, Recall, F1, ROC-AUC, **PR-AUC (Average Precision)**

4. **Linear Regression: MSE and R² + Overfitting vs data issues**
   - How to interpret regression metrics
   - Bias/variance intuition and recognizing data/label noise

5. **Logistic Regression Objective**
   - Cross-entropy / **log loss**
   - Why probability confidence matters (not just predicted class)

6. **KNN Hyperparameters + Scaling**
   - Why KNN is sensitive to feature scaling
   - Effect of **k** and distance choice on bias/variance

7. **Decision Trees: Leaf Nodes and Predictions**
   - Classification tree leaves → majority class + class probabilities
   - Regression tree leaves → mean target value in the leaf

8. **Interview Drill (30-second explanations)**
   - Quick prompts to practice speaking clearly under pressure

9. **Reflection**
   - Short reflection on mistakes + habits to avoid leakage and metric misuse

## Requirements
This notebook uses standard Python ML libraries:

- Python 3.x  
- numpy  
- pandas  
- matplotlib  
- scikit-learn  

Install with pip:
```bash
pip install numpy pandas matplotlib scikit-learn
```

## How to run
1. Open the notebook in Jupyter Notebook / JupyterLab / VS Code:
   - `JobInterviewGuide_Workshop_VirajMistry.ipynb`
2. Run cells from top to bottom.
3. Fill in the **TODO exercises** as practice (included to simulate interview-style thinking).

## Outputs you will see
- Small example DataFrames demonstrating leakage patterns  
- Train/test splits and pipeline examples  
- Classification metric outputs (precision/recall/F1, PR-AUC, ROC-AUC, confusion matrix)  
- Regression metric outputs (MSE, R²)  
- Short written interview answers + reflection responses

## Goal (how to use this for interviews)
The goal isn’t only to compute results—it's to **explain them**:
- What went wrong (leakage, wrong metric, scaling mistakes)
- What the correct pattern is (pipeline + strict split)
- Which metric you’d choose and why (imbalanced vs balanced problems)

## Author
Viraj Mistry

------------------------------------------------------------------------------------------------------------

# JobInterviewGuide Workshop — Param Rasaniya
 
This repo contains a single Jupyter Notebook that reviews key ML concepts that commonly show up in quizzes and interviews (metrics, data leakage, scaling, class imbalance, etc.).
 
- **Notebook:** `JobInterviewGuide_Workshop_ParamRasaniya.ipynb`
- **Name:** Param Rasaniya  
- **Student ID:** 9086095  
 
---
 
## How to run (top to bottom)
 
### Option A — VS Code
1. Install the **Python** extension and **Jupyter** extension in VS Code.
2. Open this folder in VS Code.
3. Open `JobInterviewGuide_Workshop_ParamRasaniya.ipynb`.
4. Select a Python kernel (recommended: a fresh virtual environment).
5. Click **Run All**.
 
### Option B — Jupyter (classic / Lab)
1. (Optional) Create and activate a virtual environment.
2. Install requirements.
3. Launch Jupyter and open the notebook.
4. Run all cells in order.
 
---
 
## Requirements
 
This notebook uses:
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`
 
Install with pip:
```bash
pip install numpy pandas scikit-learn matplotlib
```
 
> Note: The notebook is self-contained and uses small **synthetic datasets**, so it runs quickly and does not need external CSV files.
 
---
 
## What’s inside the notebook (sections)
 
### 0) Setup
- Imports required libraries.
- Sets a random seed for reproducibility.
- **Talking points included** to explain what each part is doing.
 
### 1) Independent vs Dependent Variables (X vs y)
- Simple example showing feature columns (**X**) vs target (**y**) using a house-price-style toy dataset.
 
### 2) Regression vs Classification: choosing the right metric
- Quick rules of thumb for when to use regression metrics vs classification metrics.
 
### 3) MSE (Mean Squared Error)
- Explains what MSE measures and why squaring matters.
 
### 4) Data leakage (common mistake)
- Shows the right order:
  1. split train/test
  2. fit preprocessing **only on train**
  3. transform train + test using the same fitted transform
 
### 5) Scaling and why it matters (KNN example)
- Demonstrates how distance-based models (like KNN) are affected by feature scale.
 
### 6) Confusion matrix + Precision / Recall / F1 (imbalanced classification)
- Builds an imbalanced dataset.
- Computes confusion matrix and key metrics.
- Emphasizes **recall/sensitivity** when false negatives are expensive.
 
### 7) Log Loss (probability-aware metric)
- Shows how log loss punishes overconfident wrong probabilities more than “less confident” ones.
 
### 8) Mini drill (interview-style)
- Short Q&A prompts (e.g., “What is data leakage? Give one example.”).
 
### 9) Reflection
- Short reflection summarizing what was confusing and what was improved.
 
---
 
## Outputs you should expect
 
When you run all cells:
- A couple small printed outputs / quick checks (stdout).
- Small displayed tables (pandas DataFrames).
- **At least one plot** (a simple regression line / fit visualization).
 
---
 
 
## Troubleshooting
 
- If you see `ModuleNotFoundError`, install the requirements using pip (see above) and restart the kernel.
- If plots don’t show in VS Code, ensure you’re using the Jupyter extension and that the notebook is running on a Python kernel.

------------------------------------------------------------------------------------------------------------

## 🧪 What Was Implemented

### ✅ 1. 15-Question Technical MCQ Interview

* Supervised vs Unsupervised learning
* Model evaluation metrics
* Bias–variance tradeoff
* Data leakage
* Imbalanced datasets
* Model selection trade-offs

**Final Score:** 30/30

---

### ✅ 2. Gap Analysis & Targeted Exercises

Identified improvement areas and implemented:

* 🔹 KMeans + PCA (Unsupervised learning)
* 🔹 Decision tree depth vs accuracy visualization
* 🔹 Cross-validation & GridSearchCV tuning
* 🔹 Residual diagnostics + linearization demo
* 🔹 Overfitting detection curves

---

### ✅ 3. FAANG-Style Second Round

Advanced scenario-based questioning:

* Metric trade-offs
* Drift detection
* Fairness & governance
* Regularization theory
* Production considerations

---

### ✅ 4. Behavioral Deep Dive (STAR Method)

Prepared structured responses for:

* Handling ambiguity
* Disagreement with stakeholders
* Model improvement
* Automation impact
* Explaining technical concepts

---

### ✅ 5. Canadian Hiring Manager Panel Simulation 🇨🇦

Focused on:

* Business alignment of metrics
* Privacy-first design mindset
* SQL proficiency
* Model monitoring strategy
* KPI alignment

---

### ✅ 6. Math-Heavy Derivation Stress Test

Included derivations and intuition for:

* R² formula
* MSE vs MAE
* Bias–Variance decomposition
* Cross-entropy as negative log-likelihood
* Logistic sigmoid reasoning
* L1 vs L2 regularization geometry

---

## 📊 Key Technical Strengths Demonstrated

* Proper use of **scikit-learn Pipelines**
* Avoidance of **data leakage**
* Cross-validation discipline
* Metric selection aligned with business context
* Visualization-driven diagnostics
* Interpretability awareness
* Privacy-conscious modeling mindset

---

## 🛠️ Technologies Used

* Python 3.x
* pandas
* numpy
* scikit-learn
* matplotlib

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone <your-repo-link>
cd JOBINTERVIEWGUIDE_WORKSHOP-MAIN
```

2. Open Jupyter Notebook:

```bash
jupyter notebook
```

3. Run:

```
JobInterviewGuide_Workshop_SumanthR...ipynb
```

---

## 🧠 Reflection & Growth

This project helped transition from theoretical ML knowledge to structured interview readiness. By identifying weaknesses (unsupervised learning clarity, tree interpretation, CV tuning), targeted reinforcement was applied.

The result is a stronger foundation in:

* Model selection reasoning
* Evaluation rigor
* Stakeholder communication
* Ethical awareness

---

## 📌 Final Deliverable

The primary submission file is:

```
JobInterviewGuide_Workshop_SumanthR...ipynb
```

This notebook includes:

* Quiz results
* Technical explanations
* Targeted practice
* Interview simulations
* Reflection

---


