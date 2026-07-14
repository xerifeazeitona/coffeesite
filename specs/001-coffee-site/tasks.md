# Tasks: Modern Coffee Shop Website

**Input**: Design documents from `/specs/001-coffee-site/`

**Prerequisites**: `spec.md`, `plan.md`, `research.md`, `data-model.md`, `contracts/`, `quickstart.md`

## Phase 1: Setup (Shared Infrastructure)

**Purpose**: Initialize the static Next.js application and create shared data/configuration.

- [x] T001 Create the Next.js static app scaffold in `frontend/` with `frontend/next.config.mjs`
- [x] T002 Create static menu data in `frontend/data/beverages.ts` and static FAQ data in `frontend/data/faqs.ts` [P]
- [x] T003 Create shared site layout files in `frontend/app/layout.tsx` and `frontend/app/globals.css` [P]
- [x] T004 Create navigation and footer components in `frontend/components/Header.tsx` and `frontend/components/Footer.tsx` [P]
- [x] T005 Configure static export settings and build scripts in `frontend/package.json` and `frontend/next.config.mjs`

---

## Phase 2: Foundational (Blocking Prerequisites)

**Purpose**: Implement reusable UI components and responsive styling that all pages depend on.

- [x] T006 Implement the responsive page wrapper and site metadata in `frontend/app/layout.tsx`
- [x] T007 Add global responsive design and accessibility styles in `frontend/app/globals.css`
- [x] T008 Create reusable page sections in `frontend/components/Section.tsx` and `frontend/components/Container.tsx` [P]
- [x] T009 Add navigation accessibility support and keyboard focus styles in `frontend/components/Header.tsx`

---

## Phase 3: User Story 1 - Landing Page First Impression (Priority: P1)

**Goal**: Deliver a sleek landing page that establishes brand identity and routes visitors to Menu and FAQ.

- [x] T010 [US1] Create the landing page shell in `frontend/app/page.tsx`
- [x] T011 [P] [US1] Add hero section content, branding, and navigation CTA buttons in `frontend/app/page.tsx`
- [x] T012 [P] [US1] Add landing page responsive styling and visual polish in `frontend/app/globals.css`
- [ ] T013 [US1] Ensure the landing page is mobile-responsive and loads within 3 seconds using static assets only

---

## Phase 4: User Story 2 - Browse Coffee Menu (Priority: P1)

**Goal**: Deliver the Menu page with mocked coffee beverages and polished presentation.

- [x] T014 [US2] Create the Menu page in `frontend/app/menu/page.tsx`
- [x] T015 [P] [US2] Create the reusable beverage card component in `frontend/components/BeverageCard.tsx`
- [x] T016 [P] [US2] Render mocked beverage entries from `frontend/data/beverages.ts` on the Menu page
- [x] T017 [P] [US2] Add responsive menu grid styling in `frontend/app/globals.css`
- [x] T018 [US2] Verify the Menu page displays at least three beverages and navigation from landing/FAQ

---

## Phase 5: User Story 3 - Find Answers to Common Questions (Priority: P2)

**Goal**: Deliver a helpful FAQ page with mocked questions and easy browsing.

- [x] T019 [US3] Create the FAQ page in `frontend/app/faq/page.tsx`
- [x] T020 [P] [US3] Create the FAQ section component in `frontend/components/FAQSection.tsx`
- [x] T021 [P] [US3] Render mocked FAQ entries from `frontend/data/faqs.ts` on the FAQ page
- [x] T022 [P] [US3] Add responsive FAQ page styling in `frontend/app/globals.css`
- [x] T023 [US3] Verify the FAQ page includes at least ten questions and accessible navigation

---

## Phase 6: Polish & Cross-Cutting Concerns

**Purpose**: Finalize quality, accessibility, performance, and static export.

- [x] T024 [P] Add `alt` text for all images and verify accessible labels in `frontend/components/*`
- [x] T025 [P] Optimize static asset sizes and confirm image compression in `public/images/`
- [ ] T026 [P] Validate WCAG 2.1 AA accessibility and keyboard navigation across landing, menu, and FAQ pages
- [ ] T027 Configure static export verification and test output existence for `frontend/app/page.tsx`, `frontend/app/menu/page.tsx`, and `frontend/app/faq/page.tsx`

---

## Dependencies

- Phase 1 must complete before Phase 2.
- Phase 2 must complete before Phase 3, Phase 4, and Phase 5.
- Phase 3, Phase 4, and Phase 5 can progress in parallel after Phase 2 is complete.
- Phase 6 is the final polish phase and depends on all prior phases.

## Parallel Opportunities

- `frontend/data/beverages.ts` and `frontend/data/faqs.ts` can be created in parallel with shared component setup.
- Page-specific components and styles for landing, menu, and FAQ can be developed in parallel after the shared layout is ready.
- Accessibility and asset optimization work in Phase 6 can occur alongside final content review.

## Implementation Strategy

- Deliver the static Next.js app scaffold first, including core layout and navigation.
- Build the landing page and menu page next as the MVP slice, because they represent the highest-priority user journeys.
- Add the FAQ page after the primary menu experience is working.
- Finish with performance and accessibility polish, then verify the static export output.
