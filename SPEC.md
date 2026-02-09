# Competitive Differentiation Ranker

A vector function that evaluates all startup ideas simultaneously for relative differentiation.

## Input Schema

The input is an object with an `items` field containing an array of startup ideas. Each item uses anyOf to accept:
- A string (text pitch)
- An image (type: image)
- An audio (type: audio)
- A video (type: video)
- An array of the above (composite pitch)

Example input schema structure:
```json
{
  "type": "object",
  "properties": {
    "items": {
      "type": "array",
      "items": {
        "anyOf": [
          {"type": "string"},
          {"type": "image"},
          {"type": "audio"},
          {"type": "video"},
          {"type": "array", "items": {"anyOf": [{"type": "string"}, {"type": "image"}, {"type": "audio"}, {"type": "video"}]}}
        ]
      }
    }
  },
  "required": ["items"]
}
```

## Output

A vector of scores (one per item) summing to ~1.

## Output Length

Dynamic - equals len(input['items']).

## Evaluation Criteria

1. **Relative Uniqueness**: Which ideas occupy unique territory?
2. **Defensibility and Moats**: Which have structural advantages?
3. **Competitive Positioning**: Which are clearly superior?
4. **Cross-Idea Pivot Barriers**: How hard to pivot into each space?