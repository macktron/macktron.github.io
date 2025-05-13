---
layout: blank
title: Custom Index
permalink: /customindex/
---

![Custom Index Formula](../images/custom_index.png)

The **Agreement Index** is a way to measure how similarly two political groups vote in the European Parliament — not how united each group is internally, but how close their voting outcomes are **to each other**.

### How it works

The index looks at three types of votes:
- **Yes**
- **No**
- **Abstain**

For any two groups, it compares the percentage of each type of vote and calculates how far apart they are. The formula then converts this difference into a number between 0 and 1:

- **1** means perfect agreement (they voted the same way)
- **0** means complete disagreement

### Variables:
- `%Y₁` and `%Y₂` = Percentage of **Yes** votes for Group 1 and Group 2
- `%N₁` and `%N₂` = Percentage of **No** votes
- `%A₁` and `%A₂` = Percentage of **Abstain** votes

The full formula:

\[
\text{Agreement Index} = 1 - \frac{1}{2} \left( | \%Y_1 - \%Y_2 | + | \%N_1 - \%N_2 | + | \%A_1 - \%A_2 | \right)
\]

### Why use this?

This metric is useful when:
- You want to see how closely two political groups align on actual votes
- You care more about **outcomes** than internal group discipline

For a real-world application, check out how [EPG voting alignment changes over time →](/pca_epg_similarity/)
