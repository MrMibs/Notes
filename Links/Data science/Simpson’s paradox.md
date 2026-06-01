#datascience
## Definition
A trend observed in several groups disappears or reverses when the groups are combined.

## Why it is a problem
Ignoring important confounding variables can lead to incorrect conclusions.

## Example
People wearing a motorcycle helmet are much more likely to be killed in a motorcycle crash than people not wearing a motorcycle helmet.

Does that mean that motorcycle helmets cause fatal motorcycle crashes?

No! If you look more closely at the data you'll find that the crucial variable is whether or not the person is riding a motorcycle.

The association between helmets and fatal crashes is true when you look at the entire population, but that is because the vast majority of people not wearing a helmet are not at any risk of dying in a crash because they are not riding a motorcycle.

If you restrict the data to people riding motorcycles, you will find that those wearing helmets are less likely to die in a crash.

## Warning signs
- Results change dramatically after aggregation (combining).
- Important subgroup variables exist.

## How to avoid it
- Analyze relevant subgroups.
- Look for confounding variables.
- Examine both aggregated and stratified (to look at your data within different levels of some factor) data.

## Key idea
Combining data can hide or reverse the true relationship.