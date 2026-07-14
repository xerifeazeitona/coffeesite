# Quickstart: Modern Coffee Shop Website

## Prerequisites

- Node.js 18+ installed
- Yarn or npm installed
- Git repository checked out at `/home/korporal/Documents/demo/coffeesite`

## Setup

1. Open the repository in your terminal.
2. Install dependencies:
   - `npm install`
   - or `yarn install`

## Local development

1. Start the Next.js development server:
   - `npm run dev`
   - or `yarn dev`
2. Open the site in your browser at `http://localhost:3000`.
3. Verify the following pages render correctly:
   - `/` → Landing page
   - `/menu` → Menu page
   - `/faq` → FAQ page

## Static build validation

Run the production build for static export:
- `npm run build`
- `npm run export`

Expected outcomes:
- Build completes without errors
- The `out/` directory contains static HTML/CSS/JS files
- `/out/index.html`, `/out/menu.html`, and `/out/faq.html` are present

## Performance and accessibility checks

1. Run Lighthouse audit in Chrome DevTools or automated CLI tool.
2. Verify:
   - Performance score ≥ 85 on desktop
   - Performance score ≥ 75 on mobile
   - Accessibility score ≥ 90
3. Confirm all images are optimized and file sizes are reasonable.

## Expected results

- Landing page loads cleanly with responsive design and modern styling.
- Menu page displays at least 3 mocked beverages.
- FAQ page shows at least 10 questions with readable answers.
- Navigation links work between `/`, `/menu`, and `/faq`.

## Notes

- Menu and FAQ data is mocked in static content.
- No external API or database is required.
- If using `next export`, ensure all pages are static and all routes are included.
