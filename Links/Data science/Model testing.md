#datascience

| Category             | Question                                       |
| -------------------- | ---------------------------------------------- |
| Log loss             | “Are predicted probabilities well calibrated?” |
| MAPE                 | “How good are forecasts over time?”            |
| Sensitivity analysis | “What inputs matter most?”                     |
| Stability            | “Is the model consistent?”                     |
| Robustness           | “Does it survive real-world noise?”            |

# Log Loss
## Question it answers
Are predicted probabilities well calibrated?

## Definition
Log loss measures how well a model predicts probabilities, penalizing confident wrong predictions heavily.

## Formula
$$
\text{Log Loss} = -\frac{1}{n} \sum_{i=1}^{n} \left[ y_i \log(p_i) + (1 - y_i)\log(1 - p_i) \right]
$$

## Intuition
- Good: high probability for correct class
- Bad: high probability for wrong class (huge penalty)

## Key idea
Evaluates **probability quality**, not just classification accuracy.

---

# MAPE (Mean Absolute Percentage Error)
## Question it answers
How good are forecasts over time?

## Definition
Measures average prediction error relative to actual values.

## Formula
$$
MAPE = \frac{1}{n} \sum_{i=1}^{n} \left| \frac{y_i - \hat{y}_i}{y_i} \right| \cdot 100
$$

## Intuition
- “On average, how far off are predictions in percentage terms?”

## Key idea
Useful when scale matters and you want **relative error**.

---

# Sensitivity Analysis
## Question it answers
What inputs matter most?

## Definition
Measures how output changes when inputs are slightly perturbed.

## Mathematical idea
$$
S = \frac{\Delta \hat{y}}{\Delta x}
$$

(or more generally partial derivatives)
$$
\frac{\partial \hat{y}}{\partial x_i}
$$

## Intuition
- Change input → observe change in prediction

## Key idea
Quantifies **input influence / importance**

---

# Stability
## Question it answers
Is the model consistent?

## Definition
Measures how much predictions vary across different training samples.

## Mathematical idea (conceptual)
$$
\text{Stability} = \text{Var}(\hat{f}_{\text{different samples}})
$$

## Intuition
- Stable model → similar outputs across retraining
- Unstable model → large variation

## Key idea
Measures **sensitivity to data sampling**

---

# Robustness
## Question it answers
Does it survive real-world noise?

## Definition
Measures performance under perturbations or distribution shifts.

## Mathematical idea (conceptual)
$$
\hat{f}(x + \epsilon) \approx \hat{f}(x)
$$

## Intuition
- Small noise in data → small change in output

## Key idea
Measures **resilience to imperfect or shifted data**