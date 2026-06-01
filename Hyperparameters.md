#datascience 
# Hyperparameters

## Definition
Hyperparameters are **configurable settings in a machine learning model that are set before training begins**. They control the *learning process itself* rather than being learned from the data.

Unlike model parameters, hyperparameters are not updated during training. Instead, they influence **how the model learns**, not *what it learns*.

---

## Key Idea
- **Hyperparameters are chosen externally**
- They determine the behavior, flexibility, and performance of a model
- They are often tuned using validation data or methods like grid search / random search

---

## Hyperparameters vs Parameters

| Type | Learned from data? | Set by | Example |
|------|--------------------|--------|---------|
| Parameters | Yes | Model during training | Weights in linear regression, neural network weights |
| Hyperparameters | No | User / researcher | Learning rate, number of trees, k in k-NN |

---

## Common Examples of Hyperparameters

### 1. Learning Rate
Controls how big a step the model takes when updating parameters during training.

- Too high → model may overshoot optimal solution
- Too low → training becomes slow or stuck

---

### 2. Number of Epochs
How many times the model goes through the entire training dataset.

- Too few → underfitting
- Too many → overfitting

---

### 3. k in k-Nearest Neighbors (k-NN)
Number of neighbors used to classify a data point.

- Small k → sensitive to noise (overfitting)
- Large k → smoother decision boundary (possible underfitting)

---

### 4. Number of Trees (Random Forest)
How many decision trees are built in the ensemble.

- More trees → usually better performance (but slower)
- Too few trees → unstable predictions

---

### 5. Regularization Strength (λ / alpha)
Controls how much complexity is penalized.

- High regularization → simpler model, risk of underfitting
- Low regularization → more complex model, risk of overfitting

---

### 6. Batch Size (Neural Networks)
Number of samples processed before updating model weights.

- Small batch → noisy but can generalize well
- Large batch → stable but requires more memory

---

## Why Hyperparameters Matter
Hyperparameters strongly influence:
- Model accuracy
- Generalization ability (performance on unseen data)
- Training time
- Risk of overfitting or underfitting

Even a good model can perform poorly if hyperparameters are poorly chosen.

---

## How Hyperparameters Are Chosen

### Manual tuning
Trying values based on experience or intuition

### Grid search
Testing all combinations from a predefined set

### Random search
Sampling random combinations (often more efficient than grid search)

### Bayesian optimization
Uses previous results to intelligently choose next hyperparameters

---

## Intuition
Think of building a machine learning model like cooking:

- **Parameters** = the final taste of the dish (learned during cooking)
- **Hyperparameters** = oven temperature, cooking time, spice level (set before cooking)

---

## Summary
Hyperparameters are **external controls that shape how a model learns from data**. Choosing good hyperparameters is often just as important as choosing the model itself.