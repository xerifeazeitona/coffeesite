# Contract: FAQ Data

## Overview

This contract defines the structure for FAQ entries on the CoffeeSite website.

## FAQItem Schema

```ts
interface FAQItem {
  id: string;
  question: string;
  answer: string;
  category?: string;
  relatedLinks?: string[];
}
```

## Required Fields

- `id`: unique string identifier
- `question`: non-empty question text
- `answer`: non-empty answer text

## Optional Fields

- `category`: grouping label, such as `Ordering`, `Location`, `Ingredients`
- `relatedLinks`: array of internal page anchors or links

## Data Requirements

- The FAQ page MUST display at least ten questions.
- FAQ data must be embedded in source code as static content.
- No runtime external API or database calls are allowed.

## Validation

- `id` must be unique across all FAQ entries.
- `question` and `answer` must be relevant to a coffee shop context.
- `category` values should be consistent across entries if used.
