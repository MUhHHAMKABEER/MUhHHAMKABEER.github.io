# Design System: Muhammad Kabeer portfolio

Written from the live site (index.html) on 24 Nov 2026. This file is the rule book.
If a skill, a detector or a habit disagrees with this file, this file wins.

## Overview

One-page portfolio for a software and AI automation engineer, aimed at small business
owners in the US, UK and Australia who arrive from a cold email. Mode: Persuade.
Editorial and confident: huge condensed uppercase display type, a soft italic serif
voice, a 3-colour dark green palette, and one product-mockup hero.

Fixed decisions (do not change without Kabeer saying so):
- Palette is dark green: #051F20, #235347 and white. Other values are tints of these.
- Hero headline: "Software & AI automation engineer".
- Never position the work as an auction business. The marketplace project is described
  as an online marketplace for vehicles and boats. No "auction", "bid" or "bidding"
  in copy, alt text or visible in screenshots.
- The marketplace client stays anonymous. No client name or logo in copy or screenshots.
- Only true facts. No invented numbers, clients, results or testimonials.
- Contact is through LinkedIn for now.

## Colors

### Primary
- `--ink` / `--dark` #051F20: text on light, dark sections (trust bar, work, contact).
- `--accent` / `--muted` / `--photo` #235347: secondary text, accent shapes, AI nodes.

### Neutral
- `--bg` #FFFFFF, `--bg-2` #F3F5F5 (tiles, about band), `--line` #E2E7E7.
- On dark: `--on-dark` #FFFFFF, `--on-dark-muted` white at 70%, `--dark-line` white at 14%.

### Named rules
- **Three colours only.** No new hues. Status, hover and focus come from these three.
- **Contrast floor.** Body text 4.5:1, large text 3:1. Never put text in the same colour
  as its background (placeholders included).

## Typography

- Display: **Anton**, uppercase, line-height .98. Headlines, labels, numbers, buttons.
- Voice: **Instrument Serif**, italic for the emphasised word inside a display headline
  (`em.serif-i`), roman for leads and short descriptions.
- Body/UI: **Inter** 400/500/600.

### Hierarchy (desktop / ≤900px)
- h1 hero 92px / 56px (italic line 72px / 56px)
- h2 section 72px / 56px; contact h2 150px / 72px
- h3 case 44px / 28px; tile 28px; step/card 44px / 28px
- Lead 24px serif; body 16–18px Inter, line-height 1.55–1.65
- One h1. Headings go in order (h1 → h2 → h3), no skipped levels.

## Layout

- `.wrap` max 1440px, side padding 72px, 16px at ≤900px.
- Sections: 110px vertical padding, 72px at ≤900px.
- Breakpoints: 1200px (hero stacks), 900px (mobile layout), 600px (hero art simplified).
- Must work at 1440px and 375px with no horizontal scroll.

## Elevation & Depth

- `--shadow-1` 0 12px 28px rgba(5,31,32,.14): hover lift, chips, stacked cards.
- `--shadow-2` 0 40px 80px -20px rgba(5,31,32,.45): floating hero window, phone, flow card.
- A soft blurred ellipse under floating objects. Film grain overlay at 7%.

## Shapes

- Radius: 10px small, 20px cards and windows, 999px pills, 240px arches (hero, about photo).
- Brand motif: the interlocking corner bracket (top + left border), used in eyebrows,
  the loader mark and the Work reveal.

## Components

### Buttons
- Primary `.btn`: ink pill, Anton 16px, white circle with arrow on the right. Hover lifts 2px,
  arrow moves 4px. `.btn.light` is the inverse on dark.
- Secondary `.btn-2`: 54px outline pill, fills ink on hover.

### Navigation
- Sticky glass top bar (white 72% + 14px blur), MK monogram left, 5 anchor links right.
- At ≤900px a menu button opens the same 5 links; a Contact pill stays visible.

### Cards / containers
- Bento tiles (`.tile`) on `--bg-2`; stacked sticky process cards (`.card`) in 4 tones.
- Work case study: text left, browser-frame screenshots right.

### FAQ
- Native `details/summary`, Anton 24px, +/– marker.

## Motion

- Intro: short loader (brand mark locks together, panels lift), then the headline words rise
  from behind a mask. Whole intro under ~1.5s.
- Scroll: sections fade and rise in once; Work opens from the logo's centre square.
- Marquee of the tech stack.
- `prefers-reduced-motion: reduce` turns off the loader, marquee, reveals, word rise and
  smooth scrolling. Content is fully visible with no motion.

## Do's and Don'ts

### Do
- Keep real, checked facts only (10 months at Hexafume, one live marketplace, you own the code).
- Label illustrations as illustrations, and keep that label visible.
- Test at 1440px and 375px with Playwright before calling anything done.

### Don't
- Don't add colours, fonts or claims that are not here.
- Don't show "auction", "bid" or the client's name or logo anywhere.
- Don't hide content behind a long loader.
- Don't ship requests for files that don't exist (404s).
