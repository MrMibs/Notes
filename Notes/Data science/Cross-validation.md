## Definition
Cross-validation is a model evaluation technique used to estimate how well a model will generalize to unseen data by repeatedly splitting the dataset into training and validation sets.

---

## 🧠 Core idea
Instead of evaluating a model once, we:
> train and test it multiple times on different data splits

This gives a more reliable estimate of performance.

---

# 🔁 k-Fold Cross-Validation

## How it works
1. Split dataset into **k equally sized folds**
2. For each fold:
   - Train on k−1 folds
   - Test on the remaining fold
3. Repeat k times
4. Average the performance

---

## Formula idea
If metric is \(M_i\) for fold i:

$$
\text{CV score} = \frac{1}{k} \sum_{i=1}^{k} M_i
$$

---

## Example (k = 5)

- Split data into 5 parts
- Train 5 models:
  - each time using 4 parts for training, 1 for testing
- Average the 5 results

---

## Pros
- More stable than a single train/test split
- Uses all data for both training and validation

## Cons
- More computationally expensive

---

# 🧪 Leave-One-Out Cross-Validation (LOOCV)

## How it works
- Special case of k-fold where:
  - k = number of observations (n)

Steps:
1. Train on n−1 samples
2. Test on the remaining 1 sample
3. Repeat for every sample

---

## Key properties
- Maximum training data used each time
- Very high computational cost

---

## Pros
- Nearly unbiased estimate
- Uses almost all data for training

## Cons
- Very expensive for large datasets
- High variance in estimate

---

# 🔑 Comparison

| Method | k-Fold | LOOCV |
|--------|--------|-------|
| k value | 5–10 typical | n |
| Bias | slightly higher | lower |
| Variance | moderate | high |
| Cost | moderate | very high |

---

# 🧠 Key intuition

Cross-validation answers:

> “How stable is my model performance across different samples of data?”

It simulates repeated training on slightly different datasets to approximate real-world generalization.