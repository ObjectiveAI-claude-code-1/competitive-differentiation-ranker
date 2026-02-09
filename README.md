# Competitive Differentiation Ranker

A vector function that evaluates a batch of startup ideas for relative competitive differentiation, producing a probability distribution where each score represents an idea's share of total differentiation value.

## Overview

Unlike traditional evaluation functions that score items in isolation, this function compares all startup ideas simultaneously to determine which occupy the most unique, defensible, and strategically distinct positions relative to others in the batch.

## Input

The function accepts an object with an `items` array containing startup ideas:

```json
{
  "items": [
    "Text pitch for startup A...",
    "Text pitch for startup B...",
    {"type": "image_url", "image_url": {"url": "https://example.com/pitch-deck.png"}},
    ["Composite pitch", {"type": "video_url", "video_url": {"url": "https://example.com/demo.mp4"}}]
  ]
}
```

Each item can be:
- **Text**: A text-based startup pitch (string)
- **Image**: A pitch deck slide, product mockup, or diagram
- **Audio**: A verbal elevator pitch
- **Video**: A demo video or founder pitch
- **Composite**: An array combining multiple formats

**Minimum 2 items required** for meaningful comparison.

## Output

A vector of scores (one per item) summing to approximately 1:

```json
[0.35, 0.25, 0.20, 0.15, 0.05]
```

Higher scores indicate ideas that are more differentiated from others in the batch.

## Evaluation Criteria

The function evaluates ideas across six dimensions organized into four pillars:

### 1. Relative Uniqueness
- Novel problem framing vs. conventional approaches
- Unexplored domain intersections
- How far the idea sits from the "centroid" of the batch

### 2. Defensibility and Moats
- Network effects potential
- Data moats and proprietary advantages
- Switching costs and lock-in
- Economies of scale

### 3. Competitive Positioning
- Value proposition clarity
- Strategic coherence
- Market timing
- Category creation vs. competition in crowded markets

### 4. Pivot Barriers
- Technical barriers to replication
- Domain expertise requirements
- Business model conflicts
- First-mover advantages

### 5. Isolation Analysis
- Cluster identification
- Similarity detection
- Which ideas stand alone vs. exist in crowded clusters

### 6. Holistic Assessment
- Overall differentiation across all dimensions

## Use Cases

- **Investor Screening**: Quickly identify the most differentiated ideas in a batch of pitches
- **Accelerator Selection**: Evaluate cohort applicants for competitive overlap
- **Portfolio Analysis**: Assess differentiation within an existing portfolio
- **Competition Mapping**: Understand relative positioning of market players
- **Ideation Ranking**: Prioritize new product concepts by differentiation potential

## Interpretation

- **High Concentration** (one idea with 0.8+): One standout in a batch of similar ideas
- **Uniform Distribution** (~0.2 each for 5 ideas): All ideas are equally differentiated
- **Clustered Scores**: Groups of similar ideas sharing differentiation value

## Example

```json
{
  "items": [
    "AI chatbot for customer support. SaaS model.",
    "AI chatbot for customer service. Uses GPT-4.",
    "Customer support automation using AI.",
    "Blockchain supply chain tracking for luxury goods."
  ]
}
```

Expected output: Ideas 1-3 share a smaller portion (they're similar), while idea 4 gets a larger share (unique in this batch).
