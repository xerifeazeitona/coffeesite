# Data Model: Modern Coffee Shop Website

## Entities

### Beverage
Represents a coffee menu item shown on the Menu page.

Fields:
- `id` (string): unique identifier for the beverage
- `name` (string): beverage name
- `description` (string): short promotional description
- `price` (string): display price, optional but recommended
- `image` (string): path or URL for the beverage image/icon
- `category` (string): coffee type category (e.g., espresso, latte, cold brew)
- `tags` (string[]): optional list of attributes, such as "Seasonal", "Plant-based", or "Popular"

### FAQItem
Represents a frequently asked question entry.

Fields:
- `id` (string): unique identifier for the FAQ entry
- `question` (string): the question text
- `answer` (string): the answer text
- `category` (string): optional grouping label (e.g., "Ordering", "Location")
- `relatedLinks` (string[]): optional list of internal anchors or page links

### NavigationLink
Represents a site navigation item.

Fields:
- `id` (string): unique identifier for the link
- `label` (string): display text (e.g., "Menu", "FAQ")
- `href` (string): destination path (e.g., "/menu", "/faq")

## Relationships

- `NavigationLink` is referenced from the site header/footer and connects to pages built from static routes.
- `Beverage` entries are rendered on the Menu page.
- `FAQItem` entries are rendered on the FAQ page.

## Validation Rules

- `Beverage.name` must be present and non-empty.
- `Beverage.description` must be present and non-empty.
- `FAQItem.question` and `FAQItem.answer` must be present and non-empty.
- `NavigationLink.href` must reference a valid static route within the site.

## Storage Model

- Data is stored as embedded static content in Next.js page props or local modules.
- No runtime database or API storage is used.
- Build-time data generation ensures static output.
