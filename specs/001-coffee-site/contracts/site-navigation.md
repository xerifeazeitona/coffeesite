# Contract: Site Navigation

## Overview

This contract defines the static navigation links for the CoffeeSite website.

## Navigation Links

- `Home`
  - `href`: `/`
  - `description`: Landing page introducing the coffee shop and guiding visitors to the menu and FAQ.

- `Menu`
  - `href`: `/menu`
  - `description`: Shows a curated list of mocked coffee beverages.

- `FAQ`
  - `href`: `/faq`
  - `description`: Provides answers to common customer questions.

## Expected Behavior

- Navigation links are present in the site header on all pages.
- Links are keyboard accessible and visible on mobile and desktop.
- Clicking a link navigates to the corresponding static page.

## Validation

- Each link must resolve to an existing route.
- No broken internal links are allowed.
- Navigation must function in both client-side routing and static export contexts.
