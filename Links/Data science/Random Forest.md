## Definition
Random Forest is an ensemble learning method that builds many decision trees and combines their predictions to improve accuracy and reduce overfitting.

---

## 🌲 Core idea
Instead of relying on one decision tree, Random Forest uses a **collection (forest) of trees**, each trained on slightly different data.

Final prediction is:
- **Regression:** average of all tree predictions
- **Classification:** majority vote of all trees

---

## ⚙️ 1. Bagging (Bootstrap Aggregation)

- Create **B bootstrap samples** from the training data
- Each sample is drawn **with replacement**
- Train one decision tree per sample

👉 Result:
Each tree sees a slightly different dataset

---

## 🌿 2. Feature Bagging (Random Feature Selection)

At each split in a tree:
- Randomly select a subset of features
- Choose the best split only among those features

👉 Result:
- Trees become less correlated
- Model generalizes better

---

## 🧠 3. Aggregation of predictions

### Regression:
$$
\hat{y} = \frac{1}{B} \sum_{b=1}^{B} \hat{y}_b
$$

### Classification:
- Each tree votes for a class
- Final prediction = majority vote

---

## 🔑 Why Random Forest works

- **Bagging reduces variance**
- **Feature randomness decorrelates trees**
- Combining many weakly correlated trees produces a strong model

---

## 📉 Intuition

A single decision tree:
- high variance
- overfits easily

Random forest:
- many noisy trees
- noise cancels out when averaged

---

## 🧪 Key parameters
- `ntree` (B): number of trees
- `mtry`: number of features sampled at each split
- tree depth (often fully grown)

---

## 💡 One-line summary

Random Forest =

> many decision trees trained on bootstrapped data + random feature selection + averaging/voting to stabilize predictions