# Competitive Differentiation Ranker

A vector function that evaluates startup ideas for relative competitive differentiation, producing a probability distribution where higher scores indicate stronger differentiation compared to others in the set.

## Overview

This function solves a key challenge in startup evaluation: determining which ideas occupy the most defensible and distinctive competitive territory when compared side-by-side. Unlike scoring individual ideas in isolation, this function performs simultaneous comparative analysis, producing a probability distribution that represents relative differentiation strength.

## Input

The function accepts an object with a single `items` field containing an array of 2+ startup ideas. Each item can be:

- **Text**: A plain text startup pitch (elevator pitch, one-pager, business plan excerpt)
- **Image**: A visual representation (pitch deck slide, product mockup, business model canvas)
- **Audio**: An audio pitch (verbal elevator pitch, podcast excerpt, voice memo)
- **Video**: A video presentation (demo day pitch, product demo, founder interview)
- **Composite**: An array combining any mix of the above modalities

### Example Input

```json
{
  "items": [
    "AI-powered legal document review platform for small law firms, using proprietary NLP trained on 10 years of court filings. B2B SaaS model with per-document pricing.",
    "Marketplace connecting freelance lawyers with clients for on-demand legal consultations. Takes 15% commission on each transaction.",
    "Blockchain-based smart contract platform for real estate transactions, eliminating need for traditional escrow services."
  ]
}
```

## Output

A vector of scores (one per input item) that sum to approximately 1.0, representing a probability distribution of relative competitive differentiation. Higher scores indicate stronger differentiation relative to the other ideas in the set.

### Example Output

```json
[0.42, 0.23, 0.35]
```

This indicates the first idea captures 42% of the total differentiation value, the third idea 35%, and the second idea 23% in this competitive set.

## Evaluation Criteria

The function evaluates four key dimensions of competitive differentiation:

### 1. Relative Uniqueness
Does the idea occupy unique conceptual territory? Considers:
- Novel problem framing vs. conventional approaches
- Unexplored domain intersections
- Which ideas would be seen as substitutes for each other

### 2. Defensibility and Moats
Does the idea have structural advantages that protect its position? Evaluates:
- Network effects potential
- Data moats and proprietary assets
- Switching costs for users
- Economies of scale
- Brand and trust advantages

### 3. Competitive Positioning
Is the idea clearly superior to others in meaningful ways? Assesses:
- Dominance relationships between ideas
- Category creation vs. crowded competition
- Clarity and sharpness of market position

### 4. Cross-Idea Pivot Barriers
How protected is the idea from others pivoting into its space? Considers:
- Technical barriers to replication
- Domain expertise requirements
- Business model incompatibilities
- Resource and timing advantages

## Use Cases

- **Investment Decisions**: Compare multiple startup opportunities to identify the most defensibly positioned
- **Portfolio Construction**: Evaluate overlap vs. diversity across portfolio companies
- **Competitive Strategy**: Understand positioning strengths and vulnerabilities relative to alternatives
- **Pitch Development**: Identify which aspects of differentiation are most compelling

## Notes

- Scores are relative to the specific comparison set—the same idea may score differently against different alternatives
- When ideas are nearly identical, they split their combined differentiation score
- Ideas targeting completely different markets are evaluated on absolute differentiation quality
