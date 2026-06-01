## Definition
A ROC curve shows the performance of a binary classifier across different decision thresholds by plotting **True Positive Rate vs False Positive Rate**.

## Axes
- y-axis: True Positive Rate (TPR) = TP / (TP + FN)
- x-axis: False Positive Rate (FPR) = FP / (FP + TN)

## Core idea
It shows the trade-off between:
- correctly detecting positives
- incorrectly labeling negatives as positives

## How it is built
Vary the classification threshold from high → low and compute TPR/FPR at each step.

## Interpretation
- Top-left corner = best performance
- Diagonal line = random guessing
- Curve closer to top-left = better model

## AUC
Area Under Curve (AUC) summarizes ROC into a single number:
- 1.0 = perfect model
- 0.5 = random model

## Key intuition
ROC measures how well a model can **separate classes across all thresholds**, not just one fixed cutoff.