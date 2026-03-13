---
title: "DEM of Difference vs. Differences of DEM"
slug: "dem-of-difference-vs-differences-of-dem"
topic: "Geomorphometry"
summary: "Why 'DEM of Difference' is semantically shaky, and why 'differences of DEMs' is cleaner and more precise."
date: 2026-03-13
updated: 2026-03-13
tags: [dem, terminology, methods]
status: published
---

## If you google DoD

you will likely land first on the US Department of Defense.
That is not the DoD we are discussing here.
Here, **DoD** is about DEMs and terrain change, not defense policy.

## Start with the equation we agree on

<p class="equation"><span class="math">DoD = DEM<sub>2</sub> - DEM<sub>1</sub></span></p>

## Why "elevation of difference" does not exist

Elevation is not just a number; it is a number **relative to a reference surface** (datum, geoid, ellipsoid, benchmark, etc.).
Without a reference, elevation is undefined.
So "elevation of difference" is a category error: a difference field is not itself an elevation quantity.

## Why "DEM of Difference" is awkward

If DEM means **Digital Elevation Model**, then "DEM of Difference" reads like a model of "elevation of difference."
But <span class="math">DoD</span> represents a difference between two elevations, not a new elevation.
Semantically, the phrase is inconsistent.

## Names that make sense

- **Difference of elevation models**
- **Differences of DEMs** (for multiple pairwise comparisons)
- **Elevation difference model**
- **Digital elevation difference model**
- **DEM difference map** (plain-language option)

## About the "D" in DEM

When was the last time we built a non-digital elevation model for this workflow?
Exactly.
In many contexts, "elevation model" is already sufficient; the digital nature is implied.

## Conclusion

If the goal is precise terminology, **DEM of Difference** should be retired.
Use **difference of elevation models** (or an explicit alternative) and define the equation once in the methods section.
