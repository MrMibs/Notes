#datascience
## Definition
Selection bias occurs when the data used for analysis is **not representative of the population of interest** because of how the data was collected or selected.

## Core idea
The way you sample data systematically distorts the conclusions you can draw.

## Example
- Studying student performance using only honors students  
  → overestimates average performance of all students

- Online survey about internet habits  
  → excludes people who are not active online

## Common causes
- Voluntary response (people choose to participate)
- Filtering data in a non-random way
- Missing data that is not random
- Sampling only “easy to access” subjects

## Why it is a problem
- Leads to biased estimates
- Produces misleading correlations and averages
- Can make models look more accurate than they truly are

## When it shows up in ML/data science
- Training data differs from real-world data
- Only “successful” or “available” cases are included
- Data leakage through non-random filtering

## Key intuition
If your data is “pre-selected,” your conclusions only apply to that selected group—not the whole population.