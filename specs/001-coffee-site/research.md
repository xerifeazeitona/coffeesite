# Research: Modern Coffee Shop Website

## Decision: Use Next.js with Static Site Generation

### Why chosen
Next.js is a modern React-based framework that supports static site generation with `next export` and `getStaticProps`. It fits the project requirement for a static website while enabling responsive layouts, reusable UI components, and mocked content embedded directly in the site.

### Rationale
- Aligns with the constitution's Static-First Architecture principle.
- Allows modern styling and component-driven UX without introducing a backend.
- Supports optimized asset delivery, incremental static generation patterns, and familiar developer ergonomics.

### Alternatives considered
- Hugo/Jekyll: Good for pure static sites, but less flexible for modern interactive UI and React-based design patterns.
- Vite with vanilla HTML/CSS/JS: Simple, but would require more custom scaffolding for content structure and static routing.
- Gatsby: Also viable, but adds more build-time complexity than needed for a small site.

## Decision: Use embedded mock data in content for menu and FAQ

### Why chosen
The feature explicitly calls for mocked coffee beverage data. Embedding the data in local content files or constants eliminates external dependencies and keeps the build static.

### Rationale
- No database or external API is required.
- Keeps the site self-contained and aligns with the requirement for static content.
- Makes it easy to update menu and FAQ entries in source control.

### Alternatives considered
- JSON file loaded at build time: valid, but equivalent to embedded constants for this scale.
- CMS or remote data source: rejected because it violates the static/no-backend requirement.

## Decision: Responsive mobile-first design

### Why chosen
Mobile support is explicitly required. A mobile-first responsive layout ensures strong UX on phones and scales gracefully to desktop.

### Rationale
- Ensures performance on smaller screens and lower bandwidth.
- Aligns with the constitution's performance and accessibility standards.
- Easier to validate with standard breakpoints and responsive components.

### Alternatives considered
- Desktop-first design: rejected due to mobile requirement.
- Fully adaptive design with separate templates: overkill for this scope.
