# 🧠 Tidymodels: Models, Engines & Modes (Summary)

Tidymodels (parsnip) separates modeling into:

- **Model** → what algorithm you use  
- **Engine** → how it is implemented  
- **Mode** → what type of prediction task you solve  

---

## ⚙️ Modes

- **regression** → predict continuous values (e.g. price, mpg)
- **classification** → predict categories (e.g. yes/no, classes)

---

## 📈 Common Models & Engines

### Linear Regression
- `linear_reg()`

**Engines:**
- `lm` → basic linear regression (fast, interpretable)
- `glmnet` → regularized (Lasso/Ridge), handles many predictors

---

### [[Logistic Regression]]
- `logistic_reg()`

**Engines:**
- `glm` → standard logistic regression
- `glmnet` → regularized classification

---

### [[Decision Tree]]
- `decision_tree()`

**Engine:**
- `rpart` → simple, interpretable tree model

---

### [[Random Forest]]
- `rand_forest()`

**Engines:**
- `ranger` → fast, modern, most commonly used
- `randomForest` → older, slower implementation

---

### Gradient Boosting
- `boost_tree()`

**Engines:**
- `xgboost` → high performance, widely used
- `gbm` → older boosting implementation
- `lightgbm` → fast alternative (if available)

---

### K-Nearest Neighbors
- `nearest_neighbor()`

**Engine:**
- `kknn` → standard R implementation

---

## 🧠 Core Idea

```text
model  → WHAT algorithm
engine → HOW it runs
mode   → WHAT problem you solve