# DSA Pattern Tracker Modern Rebuild Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Completely rebuild `index.html` from scratch into a modern, accessible, two-column dashboard with a collapsible sidebar, clean neutral light theme, interactive phase cards, keyboard shortcuts, and full progress tracking.

**Architecture:** A zero-dependency client-side web application built with semantic HTML5, modern CSS3 variables/grid, and modular Vanilla JS. The sidebar houses navigation, overall metrics, and status filters, while the main workspace renders sticky search controls, pattern banners, and collapsible phase accordion cards with problem rows. Solved state persists to `localStorage` under key `lc_tracker_solved_v1`.

**Tech Stack:** HTML5, CSS3 (Custom properties, Flexbox, Grid), Vanilla JavaScript (ES6+), Google Fonts (Inter, JetBrains Mono).

**Spec:** [docs/superpowers/specs/2026-09-29-dsa-tracker-redesign.md](file:///mnt/win-newvol/Projects/GitHub/leetcode-question/docs/superpowers/specs/2026-09-29-dsa-tracker-redesign.md)

## Global Constraints

- Must preserve the exact 133-problem / 28-phase curriculum and data structure in `#lc-data`.
- Must maintain 100% backwards compatibility with existing user progress stored in `localStorage` under `'lc_tracker_solved_v1'`.
- Must remain a single-file, zero-build-step application in `index.html` compatible with GitHub Pages hosting.
- Clean Neutral Light Mode must be the default theme, with a persistent Dark Mode switch.
- All interactive elements must have visible `:focus-visible` focus rings and valid ARIA attributes.
- Keyboard shortcuts: `/` to focus search, `Escape` to clear search, `Space`/`Enter` to toggle accordions.

## Review Focus

1. **Local storage corruption or empty state:** App must handle empty or corrupted `localStorage` without throwing errors or breaking the UI.
2. **Mobile sidebar behavior:** On screens < 768px, sidebar must render as an off-canvas drawer that properly traps or resets focus and closes on backdrop click.
3. **Search auto-expand & empty states:** Searching must auto-expand phases containing visible matches and display a clear "No matching problems found" empty state if no rows match.
4. **Repeated problems consistency:** Toggling a problem that appears in multiple phases (e.g. #30, #76, #239) must keep all instances in sync across all phases.
5. **Keyboard focus trap/navigation:** Tabbing must follow a logical flow starting from the skip-to-content link, through sidebar, to main search, and down problem rows.

---

### Task 1: Design System, CSS Variables & Layout Foundation

**Files:**
- Modify: `index.html` (CSS styling section)

**Interfaces:**
- Produces: CSS custom properties (`--bg`, `--surface`, `--surface-hover`, `--border`, `--text-primary`, `--text-secondary`, `--text-muted`, `--accent`, `--easy`, `--med`, `--hard`), layout grid classes (`.app-shell`, `.sidebar`, `.main-workspace`, `.mobile-topbar`).

- [ ] **Step 1: Write automated layout and theme token verification script**

Create a temporary verification script `tests/verify-css.cjs` using Node.js to verify that all necessary color tokens, responsive breakpoints (`@media (max-width: 768px)`), `:focus-visible` states, and dark mode rules exist in `index.html`.

- [ ] **Step 2: Run verification script to confirm it fails**

Run: `node tests/verify-css.cjs`
Expected: FAIL (missing new tokens and app-shell classes).

- [ ] **Step 3: Implement Design System & App Shell CSS in `index.html`**

Implement:
1. CSS custom properties for light theme (default) and `[data-theme="dark"]`.
2. Skip-to-content link styles (`.skip-link`).
3. App layout grid: `.app-shell` with desktop 280px sidebar, mobile off-canvas drawer with backdrop, and fluid main container (`max-width: 1140px`).
4. Typography rules using Inter and JetBrains Mono.
5. Focus visible rings (`outline: 2px solid var(--accent); outline-offset: 2px`).

- [ ] **Step 4: Run verification script to confirm it passes**

Run: `node tests/verify-css.cjs`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "style: implement modern design system and responsive app shell layout"
```

---

### Task 2: Responsive DOM Structure & Semantic Layout Shell

**Files:**
- Modify: `index.html` (HTML structure)

**Interfaces:**
- Consumes: Layout CSS classes from Task 1.
- Produces: Semantic DOM landmarks (`<a class="skip-link">`, `<aside id="app-sidebar">`, `<main id="main-content">`, `<header class="app-header">`), search input `#search`, filter chips, and placeholder containers `#patternNav`, `#statWidgets`, `#curriculumContainer`.

- [ ] **Step 1: Write DOM structure verification test**

Create `tests/verify-dom.cjs` using Node.js to assert presence of:
- `<a href="#main-content" class="skip-link">`
- `<aside id="app-sidebar">` with `aria-label="Navigation and statistics"`
- Mobile menu toggle button with `aria-expanded` and `aria-controls="app-sidebar"`
- `<main id="main-content">` with `#search` input and `aria-label="Search problems"`
- Filter controls for difficulty and status
- Persistent JSON script `#lc-data`

- [ ] **Step 2: Run verification test to confirm it fails**

Run: `node tests/verify-dom.cjs`
Expected: FAIL (missing new landmarks).

- [ ] **Step 3: Implement semantic DOM structure in `index.html`**

Rebuild the body HTML in `index.html` with:
1. Skip link.
2. Mobile top navigation bar (title, hamburger button, quick solved badge).
3. Sidebar: Brand header, overall progress widget, difficulty counters, pattern nav list `#patternNav`, status filters (All/Solved/Unsolved/Priority), theme toggle, data actions (Export/Import/Reset).
4. Main content area: Sticky control bar with search input (prompting `/`), difficulty chips (All, Easy, Medium, Hard), Expand/Collapse All buttons, and `#curriculumContainer`.
5. Preserved `#lc-data` JSON script element.

- [ ] **Step 4: Run verification test to confirm it passes**

Run: `node tests/verify-dom.cjs`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "feat: implement accessible semantic DOM structure and dashboard shell"
```

---

### Task 3: Pattern Sections, Phase Cards & Problem Rows Rendering

**Files:**
- Modify: `index.html` (JS rendering logic and card CSS)

**Interfaces:**
- Consumes: `#lc-data` JSON array and `#curriculumContainer`.
- Produces: `renderCurriculum(data, solvedSet)` generating Pattern header banners, Phase accordion cards with progress bars, and Problem rows with checkboxes, difficulty tags, links, and stars.

- [ ] **Step 1: Write rendering verification test**

Create `tests/verify-render.cjs` to assert:
- All 3 Patterns are generated with correct titles.
- Exactly 28 Phase cards are created with accessible headers (`<button class="phase-header" aria-expanded="true">`).
- All 133 Problem rows are generated with checkboxes, `#` numbers, and LeetCode links.
- Repeated problems carry the `🔁 Review` marker.

- [ ] **Step 2: Run verification test to confirm it fails**

Run: `node tests/verify-render.cjs`
Expected: FAIL

- [ ] **Step 3: Implement curriculum rendering engine in `index.html`**

Implement:
1. Card & row CSS styling: Phase accordion styling, chevron rotation, difficulty pill colors, problem row hover states, strikethrough on completed items.
2. JavaScript rendering functions:
   - `buildPatternSection(pattern)`
   - `buildPhaseCard(phase, patternId)`
   - `buildProblemRow(row, isDone)`
   - `buildSidebarNav(data)`
3. Initial render invocation on page load.

- [ ] **Step 4: Run verification test to confirm it passes**

Run: `node tests/verify-render.cjs`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "feat: render pattern sections, phase accordion cards, and problem rows"
```

---

### Task 4: Interactive Logic, State Management, Filtering & a11y Shortcuts

**Files:**
- Modify: `index.html` (Application controller script)

**Interfaces:**
- Consumes: DOM elements (`#search`, `.diff-chip`, `.status-filter`, `.problem-cb`, `#themeToggle`, `#exportBtn`, `#importInput`).
- Produces: Reactive filtering, progress recalculation, `localStorage` persistence, keyboard shortcuts, and theme switching.

- [ ] **Step 1: Write state and interaction verification test**

Create `tests/verify-state.cjs` to test:
- Toggling problem checkbox updates `solved` set, syncs duplicate entries, and saves to `localStorage`.
- Search filters rows by name and number, auto-expanding phases with matches.
- Difficulty chips filter correctly.
- Status filter (Solved / Unsolved / Starred) filters correctly.
- Keyboard shortcuts (`/` focuses search, `Escape` clears search).
- Theme toggle flips `data-theme` attribute and updates `localStorage`.

- [ ] **Step 2: Run verification test to confirm it fails**

Run: `node tests/verify-state.cjs`
Expected: FAIL

- [ ] **Step 3: Implement application logic & interactions in `index.html`**

Implement:
1. `State` store: `solved` (Set of problem numbers), `searchQuery`, `activeDiff`, `statusFilter`, `priorityOnly`, `theme`.
2. Checkbox change handler: updates Set, syncs across all instances of the same problem number, calls `persist()` and `updateAllMetrics()`.
3. Filter engine: computes row visibility based on combined search, difficulty, status, and priority filters.
4. Auto-expand matching phases during search; display empty state if no problems match.
5. Theme manager: toggle and persist theme, sync icon.
6. Mobile drawer toggle: open/close drawer on hamburger click, close on backdrop click or navigation link click.
7. Keyboard shortcuts: `/` key event listener, `Escape` handler, Enter/Space for phase accordions.
8. Data backup: JSON export and file import with format validation.

- [ ] **Step 4: Run verification test to confirm it passes**

Run: `node tests/verify-state.cjs`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "feat: add interactive filtering, state persistence, keyboard shortcuts, and theme switcher"
```

---

### Task 5: End-to-End Verification & Polish

**Files:**
- Modify: `index.html` (visual adjustments and refinements)
- Delete: temporary test scripts in `tests/`

- [ ] **Step 1: Run comprehensive headless verification**

Verify all features, accessibility attributes, and visual layout using Puppeteer or simulated DOM.

- [ ] **Step 2: Clean up temporary test files**

Remove `tests/` directory and ensure git status is clean.

- [ ] **Step 3: Final Commit**

```bash
git add index.html
git commit -m "chore: finalize modern dsa tracker rebuild and clean up tests"
```
