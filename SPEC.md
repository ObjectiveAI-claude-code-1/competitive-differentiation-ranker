# Competitive Differentiation Ranker

A vector function that evaluates all startup ideas simultaneously to assess their relative differentiation and defensibility within the competitive set.

## Input Schema

The input is an object with an `items` field containing an array of startup ideas to compare. Each item can be:
- A string (text pitch)
- An image, audio, or video (multimodal pitch)
- An array of the above (composite pitch)

```json
{
  "items": [
    "An AI-powered personal stylist.",
    "A decentralized tutoring marketplace.",
    "Yet another to-do list app with gamification."
  ]
}
```

## Output

A vector of scores (one per item) summing to ~1, representing relative competitive differentiation. Higher scores indicate more differentiated and defensible positions.

## Output Length

Dynamic - equals the number of items in the input array.

## Evaluation Criteria

This is inherently comparative - evaluate all ideas relative to each other:

1. **Relative Uniqueness**: Which ideas occupy unique conceptual territory? Which overlap significantly?

2. **Defensibility and Moats**: Which ideas have structural advantages (network effects, data moats, switching costs)?

3. **Competitive Positioning**: Which ideas are clearly superior to others in the batch? Which create new categories?

4. **Cross-Idea Pivot Barriers**: How hard would it be for other ideas in the batch to pivot into each idea's space?