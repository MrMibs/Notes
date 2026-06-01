## Definition
Data leakage occurs when information from the test set (or future data) is accidentally used during training.

## Core idea
The model gets access to “cheat information” it would not have in real deployment.

## Example
- Normalization done using full dataset (train + test)
- Including future information (e.g. stock prices from tomorrow)
- Target variable indirectly included in features

## Why it is a problem
- Produces unrealistically high performance during evaluation
- Fails when deployed on real unseen data

## Key intuition
The model is evaluated on an unfair advantage it will never have in reality.