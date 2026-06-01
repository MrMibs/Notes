## Definition
Bayesian networks are graphical models that represent **probabilistic relationships between variables**, often interpreted as causal structures.

## Core idea
Variables are nodes, and directed edges represent conditional dependence (often causal assumptions).

## Key concept
They encode:
- P(X | parents(X)) for each variable
- Joint probability via factorization of the graph

## Intervention (do-calculus idea)
- P(Y | X) = observation
- P(Y | do(X)) = intervention (true causal effect)

## Example
Smoking → Cancer → Mortality

## Key intuition
They let you model how changing one variable *causally influences* others.

## Use cases
- Causal inference
- Decision systems
- Medical reasoning