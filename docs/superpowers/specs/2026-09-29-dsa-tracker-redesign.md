# Technical Design Specification: DSA Pattern Tracker Modern Rebuild

**Date:** 2026-09-29  
**Status:** Approved for Implementation  
**Target:** `index.html` (Complete Redesign from Scratch)

---

## 1. Overview & Objectives

The goal is to replace the current cramped, basic single-column layout of the DSA Pattern Tracker (`index.html`) with a modern, high-aesthetic, and accessible dashboard web application. 

### Core Objectives:
1. **Modern Dashboard Architecture:** Implement a responsive two-column application layout featuring a persistent, collapsible sidebar for navigation and high-level progress tracking alongside a spacious, readable main workspace.
2. **Accessible by Design (WCAG AA):** Guarantee high contrast ratios, visible focus indicators, screen-reader landmark semantics (`<aside>`, `<main>`, `<nav>`, `<header>`), skip-to-content functionality, and full keyboard navigation.
3. **Clean Neutral Aesthetic:** A polished, airy light-mode interface with crisp slate borders, subtle shadows, and distinct difficulty accents (Emerald for Easy, Amber for Medium, Crimson for Hard), accompanied by a persistent dark-mode toggle.
4. **Seamless Data Continuity & Zero Dependencies:** Preserve the complete 133-problem / 28-phase DSA curriculum, ensure 100% backwards compatibility with existing `localStorage` solved keys (`lc_tracker_solved_v1`), and maintain zero external build dependencies (pure HTML5, CSS3, and Vanilla JavaScript).

---

## 2. Visual Design System

### 2.1 Color Palette
* **Light Mode (Default Theme):**
  * Canvas Background: `#F8FAFC` (Slate-50)
  * Surface / Cards: `#FFFFFF` (Pure white)
  * Surface Secondary / Hovers: `#F1F5F9` (Slate-100)
  * Hairline Borders: `#E2E8F0` (Slate-200)
  * Primary Text: `#0F172A` (Slate-900, 15:1 contrast against white)
  * Secondary Text: `#475569` (Slate-600)
  * Muted / Metadata Text: `#64748B` (Slate-500)
  * Primary Accent: `#2563EB` (Blue-600) / `#0284C7` (Sky-600)
* **Dark Mode (Toggleable & Persistent):**
  * Canvas Background: `#0B0F17` (Deep Obsidian)
  * Surface / Cards: `#131924` (Dark Slate)
  * Surface Secondary / Hovers: `#1E2536`
  * Hairline Borders: `#263044`
  * Primary Text: `#F8FAFC`
  * Secondary Text: `#94A3B8`
  * Muted / Metadata Text: `#64748B`
  * Primary Accent: `#38BDF8` (Sky-400)
* **Difficulty Accents (WCAG AA Compliant):**
  * **Easy (E):** Text `#059669` (Emerald-600), Background `#ECFDF5`, Border `#A7F3D0` (Dark mode: Text `#34D399`, Bg `#064E3B40`)
  * **Medium (M):** Text `#D97706` (Amber-600), Background `#FFFBEB`, Border `#FDE68A` (Dark mode: Text `#FBBF24`, Bg `#78350F40`)
  * **Hard (H):** Text `#DC2626` (Red-600), Background `#FEF2F2`, Border `#FECACA` (Dark mode: Text `#F87171`, Bg `#7F1D1D40`)

### 2.2 Typography & Shadows
* **Font Stacks:**
  * UI Sans: `'Inter'`, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif
  * Monospace: `'JetBrains Mono'`, ui-monospace, SFMono-Regular, monospace (for numbers, badges, hotkeys, stats)
* **Elevation & Layering:**
  * Card Shadow: `0 1px 3px 0 rgba(0, 0, 0, 0.05), 0 1px 2px -1px rgba(0, 0, 0, 0.03)`
  * Elevated / Hover: `0 4px 6px -1px rgba(0, 0, 0, 0.07), 0 2px 4px -2px rgba(0, 0, 0, 0.05)`
  * Modal / Drawer Shadow: `0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.08)`

---

## 3. Layout Architecture & Component Structure

### 3.1 Layout Grid
* **App Container:** CSS Grid / Flexbox layout with two primary zones:
  1. **Sidebar (`<aside id="app-sidebar">`):**
     * Desktop: `280px` fixed width, sticky `100vh`, dedicated scroll container.
     * Mobile (< 768px): Collapsible off-canvas drawer with backdrop overlay (`#sidebar-backdrop`) triggered by a mobile hamburger button.
  2. **Main Workspace (`<main id="main-content">`):**
     * Fluid width with `max-width: 1140px` centered with responsive padding (`16px` mobile, `32px` desktop).

### 3.2 Component Breakdown

#### A. Sidebar (`<aside>`)
* **Header / Branding:** App title ("DSA Pattern Tracker"), subtitle ("133 Curated LeetCode Problems"), and theme toggle button (Sun/Moon icon).
* **Overall Progress Widget:**
  * Solved ratio (`XX / 110 unique solved`) and percentage ring or fill bar.
  * Difficulty breakdown pills:
    * `Easy: X / 23`
    * `Medium: Y / 62`
    * `Hard: Z / 25`
* **Navigation Tree (`<nav>`):**
  * Direct links to the 3 Pattern sections:
    1. *Two Pointers & Sliding Window* (9 phases, 55 entries)
    2. *Prefix Sum* (11 phases, 49 entries)
    3. *Merge Intervals* (8 phases, 29 entries)
  * Each pattern item displays its current completion ratio (e.g. `12/55`) and an expandable list of quick-jump phase anchors.
* **Quick Status Filters:**
  * Radio/chip group: All (Default), Solved Only, Unsolved Only.
  * Checkbox toggle: High Priority (★ Only).
* **Footer Actions:**
  * Reset progress (with confirmation modal), Export data (download JSON), Import data (upload JSON).

#### B. Main Workspace Header & Control Bar (`<header>`)
* **Mobile Top Bar:** App brand + hamburger toggle for mobile devices.
* **Sticky Control Bar:**
  * Search Bar: `<input type="search">` with magnifying glass icon and keyboard shortcut prompt (`/`). Filters by problem name or number `#`.
  * Difficulty Filter Chips: All, Easy, Medium, Hard.
  * Action Buttons: "Expand All" and "Collapse All" phase cards.

#### C. Pattern Sections (`<section class="pattern-section">`)
* **Pattern Header Banner:**
  * Pattern title (`<h2>`), descriptive subtitle, total problem count, and overall pattern progress bar.
* **Phase Cards (`<article class="phase-card">`):**
  * Card Header (`<button class="phase-header" aria-expanded="true">`):
    * Phase Title (`<h3>`) and phase status indicator (chevron icon rotating on toggle).
    * Phase Meta: Solved count (e.g. `4 / 8`), progress bar fill.
  * Card Body (`<div class="phase-body">`):
    * Container for problem rows.

#### D. Problem Rows (`<div class="problem-row">`)
* **Checkbox:** Custom accessible checkbox `<input type="checkbox" class="problem-cb">` with custom checkmark icon, labeled by problem title.
* **Problem Number & Difficulty:**
  * `#XYZ` in JetBrains Mono.
  * Difficulty Pill (`Easy`, `Medium`, `Hard`) with dedicated WCAG AA colors.
* **Problem Link:**
  * Clean, readable title linking to `https://leetcode.com/problems/{slug}/` (opens in new tab with `target="_blank" rel="noopener noreferrer"`).
* **Metadata & Tags:**
  * Algorithmic tags (e.g., `Two Pointers`, `Hash Table`, `Dynamic Programming`).
  * Priority rating: High-priority star badges (`★ ★ ★ ★ ★`).
  * Repetition badge: `🔁 Review` indicating problems revisited in capstone/review phases.

---

## 4. Accessibility & Keyboard Navigation (a11y)

1. **Skip to Main Content:** Accessible link `<a href="#main-content" class="skip-link">Skip to problem list</a>` positioned at top of DOM.
2. **Keyboard Shortcuts:**
   * `/` or `s` : Focus search input directly.
   * `Escape` : Clear search input and blur.
   * `Space` / `Enter` on phase header : Expand or collapse phase card.
   * `Space` on checkbox : Toggle solved status.
3. **ARIA Landmark & State Roles:**
   * `aria-expanded="true|false"` on phase cards and mobile drawer toggle.
   * `aria-controls` referencing controlled panel IDs.
   * `aria-label` on all icon-only buttons (theme toggle, mobile menu, clear search).
   * `aria-live="polite"` on the solved progress counter for screen reader announcement.
4. **Focus Rings:** Non-negotiable `2px solid var(--accent)` outline with `2px offset` on all `:focus-visible` elements.

---

## 5. Data Flow & State Management

1. **Problem Database:**
   * Stored in-document as valid JSON in `<script id="lc-data" type="application/json">` maintaining the complete 133 entries across 3 patterns and 28 phases.
2. **State Store (`localStorage`):**
   * Key: `'lc_tracker_solved_v1'` containing an array of solved problem numbers `[n1, n2, ...]`.
   * Theme Key: `'lc_tracker_theme'` storing `'light'` or `'dark'`.
3. **Filtering Pipeline:**
   * Filters run reactively on any change:
     $$\text{visible} = \text{matchesSearch} \land \text{matchesDifficulty} \land \text{matchesStatus} \land \text{matchesPriority}$$
   * If a phase has visible matching problems during a search/filter, it automatically expands to reveal them.
   * Empty phases during filtering are hidden smoothly.
4. **Progress Recalculation:**
   * Dynamic recalculation of:
     * Overall unique solved count & percentage ($N \le 110$).
     * Easy / Medium / Hard solved counts.
     * Pattern-specific solved counts ($X / \text{total}$).
     * Phase-specific solved counts.

---

## 6. Verification & Quality Acceptance Criteria

1. **Visual Appeal & Polish:** Crisp styling, balanced spacing, clean neutral colors, no awkward wrapping or overflow issues.
2. **Responsiveness:** Flawless display on mobile screens (375px+), tablets (768px+), and wide desktop displays (1440px+).
3. **Keyboard Accessibility:** Complete workflow operable via keyboard alone.
4. **State Persistence:** Toggling problems, changing themes, and reloading preserves all user progress.
5. **No Regressions:** All 133 problem links, tags, and numbers remain intact and accurate.
