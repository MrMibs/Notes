## Definition
A model learns random fluctuations (noise) in the training data instead of the true underlying pattern.

## Why it is a problem
The model performs very well on the data it was trained on but poorly on new, unseen data.

## Example
A model predicts exam scores using students' study hours but also learns random quirks specific to the training dataset.

## Warning signs
- Extremely high training accuracy
- Much lower test accuracy
- Very complex model relative to the amount of data

## How to avoid it
- Use a separate test set
- Cross-validation
- Simpler models
- More training data
- Regularization

## Key idea
The model memorizes the data rather than learning the pattern.