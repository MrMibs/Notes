#datascience
## Entropy
## Meaning
Measures uncertainty in a random variable.

## Formula
$$
H(X) = -\sum p(x)\log p(x)
$$

## Key idea
Higher entropy = more uncertainty.

---

## Mutual Information
## Meaning
Measures how much knowing one variable reduces uncertainty about another.

## Formula
$$
I(X;Y) = H(X) - H(X|Y)
$$

## Key idea
How much information X gives about Y.

---

## Entropy Reduction
## Meaning
How much uncertainty is reduced after observing data.

## Key idea
More reduction = better predictive signal.

---

## Akaike Information Criterion (AIC)
## Meaning
Trade-off between model fit and complexity.

## Formula
$$
AIC = 2k - 2\log(L)
$$

## Key idea
Lower AIC = better balance of accuracy and simplicity.