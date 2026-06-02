#datascience
metric_set() is used here
![[Pasted image 20260601130551.png]]
## Definition
Practical model quality metrics measure **how well a model performs on real tasks**, usually in terms of prediction error or classification performance.

They are used to compare models and evaluate how useful they are in practice.

---

# Error Metrics (Regression)

## Mean Absolute Error (MAE)
- Average absolute difference between predictions and true values
- Interpretable in original units

$$
MAE = \frac{1}{n} \sum |y_i - \hat{y}_i|
$$

### Intuition
“How far off are predictions on average?”

---

## Mean Squared Error (MSE)
- Average squared error
- Penalizes large errors more heavily

$$
MSE = \frac{1}{n} \sum (y_i - \hat{y}_i)^2
$$

### Intuition
“Big mistakes are very bad.”

---

## Root Mean Squared Error (RMSE)
- Square root of MSE
- Same units as target variable

$$
RMSE = \sqrt{MSE}
$$

### Intuition
“Typical size of prediction error.”

---

# Classification Metrics

|Case|Meaning|
|---|---|
|TP|Correctly found a positive|
|TN|Correctly rejected a negative|
|FP|Incorrectly flagged something|
|FN|Missed something important|
## Accuracy
- Fraction of correct predictions

$$
Accuracy = \frac{TP + TN}{TP + TN + FP + FN}
$$

### Intuition
“How often is the model correct?”
"Most of the classification results are correct, regardless of base rates"

⚠️ Problem: misleading for imbalanced data

---

## Precision (Sensitivity)
- Of predicted positives, how many are actually positive?

$$
Precision = \frac{TP}{Positive=TP + FP}
$$

### Intuition
“How many positive predictions are correct?”
"The model is good at detecting all the target elements"

---

## Recall (Specificity)
- Same as above but for negatives

$$
Recall = \frac{TN}{Negative=FP + TN}
$$

### Intuition
“How many real negatives did we find?”
"The model is good at excluding all the non-target elements"

---

## F1 Score
- Harmonic mean of precision and recall

$$
F1 = 2 \cdot \frac{Precision \cdot Recall}{Precision + Recall}
$$

### Intuition
“Balance between precision and recall.”

---

## AUC ([[Categorical ROC Curve (Receiver Operating Characteristic)]]-AUC)
- Measures ability to rank positives above negatives
- Area under ROC curve (recall vs false positive rate)
$$TPR = \frac{FP}{FP+TN}$$

### Intuition
“How well does the model separate classes across thresholds?”
"The probability of negatives and the probability of positives are well separated, regardless of threshold"

![[Pasted image 20260531124842.png]]

---

# 🔑 Key takeaway

- Regression → MAE / MSE / RMSE measure error size
- Classification → precision/recall trade-offs
- AUC → ranking quality

👉 No single metric is universally best; it depends on the task.

[[Model testing]]