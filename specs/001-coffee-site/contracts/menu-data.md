# Contract: Menu Data

## Overview

This contract defines the structure for mocked coffee beverage data used on the Menu page.

## Beverage Schema

```ts
interface Beverage {
  id: string;
  name: string;
  description: string;
  price?: string;
  image: string;
  category: string;
  tags?: string[];
}
```

## Required Fields

- `id`: unique string identifier
- `name`: beverage name
- `description`: descriptive text that explains the beverage
- `image`: local asset path or static image URL
- `category`: drinks category such as `espresso`, `latte`, `cold brew`

## Optional Fields

- `price`: visible pricing text (e.g., `$4.50`)
- `tags`: additional labels such as `Popular`, `Seasonal`, or `Vegan`

## Data Requirements

- The Menu page MUST display at least three beverages.
- Each beverage must include a visual presentation (image or icon).
- Menu data must be embedded in the site source as static content.
- No external data requests or runtime fetching may occur.

## Validation

- `name`, `description`, `image`, and `category` must be non-empty.
- `id` must be unique across all beverage entries.
- `image` paths must resolve to assets included in the static build.
