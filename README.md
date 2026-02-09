# Competitive Differentiation Ranker

A vector function that evaluates startup ideas simultaneously to assess their relative differentiation and defensibility within a competitive set.

## Overview

This function takes a set of startup ideas and returns a probability distribution representing their relative competitive differentiation. Unlike functions that evaluate items in isolation, this function embraces an inherently comparative paradigm—recognizing that competitive positioning is fundamentally relational.

## Input

The input is an object with an `items` field containing an array of startup ideas to compare:

```json
{
  "items": [
    "An AI-powered personal stylist.",
    "A decentralized tutoring marketplace.",
    "Yet another to-do list app with gamification."
  ]
}
```

Each item can be:
- A **string** (text pitch)
- An **image**, **audio**, or **video** (multimodal pitch)
- An **array** of the above (composite pitch combining multiple media)

## Output

A vector of scores (one per item) summing to approximately 1, representing relative competitive differentiation. Higher scores indicate more differentiated and defensible positions within the set.

For example, the input above might produce:
```json
[0.35, 0.45, 0.20]
```

This indicates that the decentralized tutoring marketplace has the highest differentiation, followed by the AI stylist, with the to-do list app having the lowest differentiation.

## Evaluation Criteria

The function evaluates all ideas relative to each other across four dimensions:

### 1. Relative Uniqueness
Which ideas occupy unique conceptual territory versus overlapping space? Considers:
- Novel problem framing vs. conventional approaches
- Unexplored domain intersections
- Paradigm challenges vs. accepting industry orthodoxy
- Substitutability between ideas in the set

### 2. Defensibility and Moats
Which ideas have structural advantages that protect their position over time? Considers:
- Network effects (direct, indirect, data)
- Data moats (proprietary, compounding, defensible data)
- Switching costs (integration depth, data portability, learning curves)
- Economies of scale
- Brand and trust advantages

### 3. Competitive Positioning
Which ideas have the strongest competitive position within this specific set? Considers:
- Dominance relationships (is any idea clearly superior to others?)
- Category creation vs. category competition
- Blue ocean vs. red ocean dynamics
- Positional clarity

### 4. Cross-Idea Pivot Barriers
How hard would it be for other ideas in the set to pivot into each idea's space? Considers:
- Technical barriers
- Domain expertise barriers
- Business model barriers
- Resource and time barriers

## Use Cases

- **Investor Portfolio Screening**: Rapidly identify the most differentiated ideas in a batch
- **Startup Competitive Analysis**: Understand relative positioning against competitors
- **Accelerator Cohort Selection**: Ensure diversity of positioning in selected cohorts
- **Strategic Pivot Analysis**: Compare current positioning against alternative directions

## Behavior Notes

- **Homogeneous sets**: When all ideas are similar, the function produces a relatively flat distribution, signaling that true differentiation is absent.
- **Dominant ideas**: When one idea clearly outclasses others, it will receive a significantly higher score.
- **Heterogeneous sets**: When ideas are in completely different domains, each is evaluated on its standalone differentiation potential.
