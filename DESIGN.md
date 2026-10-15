---
name: Tim's Window Cleaning
description: Pure-water window cleaning from Newmarket to Cambridge, in clear premium blues.
colors:
  harbour-navy-950: "#071A2E"
  harbour-navy-900: "#0B2340"
  harbour-navy-800: "#0E2A47"
  harbour-navy-700: "#163A60"
  window-blue: "#1F5FA8"
  window-blue-deep: "#174C88"
  bright-blue: "#3C8AD8"
  sky: "#8FC5EE"
  sky-pale: "#D6E9F8"
  mist: "#F3F8FC"
  white: "#FFFFFF"
  text: "#0E2238"
  muted: "#4A5E74"
  on-dark: "#E8F1FA"
  on-dark-muted: "#AFC4D9"
  line: "#DCE6EF"
  error: "#B42318"
typography:
  display:
    fontFamily: "Manrope, system-ui, sans-serif"
    fontSize: "clamp(2.9rem, 6vw, 5rem)"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Manrope, system-ui, sans-serif"
    fontSize: "clamp(2.2rem, 4.4vw, 3.4rem)"
    fontWeight: 800
    lineHeight: 1.06
    letterSpacing: "-0.03em"
  title:
    fontFamily: "Manrope, system-ui, sans-serif"
    fontSize: "1.22rem"
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Manrope, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "Manrope, system-ui, sans-serif"
    fontSize: "0.97rem"
    fontWeight: 700
rounded:
  sm: "10px"
  md: "16px"
  lg: "20px"
  pill: "999px"
spacing:
  gutter: "clamp(1rem, 4vw, 2.5rem)"
  section: "clamp(4.5rem, 9vw, 7.5rem)"
  wrap: "1200px"
components:
  button-primary:
    backgroundColor: "{colors.window-blue}"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
    padding: "13px 24px"
  button-primary-hover:
    backgroundColor: "{colors.window-blue-deep}"
  button-primary-on-dark:
    backgroundColor: "{colors.white}"
    textColor: "{colors.harbour-navy-900}"
    rounded: "{rounded.pill}"
  button-outline:
    textColor: "{colors.harbour-navy-800}"
    rounded: "{rounded.pill}"
  input:
    backgroundColor: "{colors.mist}"
    textColor: "{colors.text}"
    rounded: "{rounded.sm}"
    height: "52px"
  chip-selected:
    backgroundColor: "{colors.window-blue}"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
  card:
    backgroundColor: "{colors.white}"
    rounded: "{rounded.md}"
---

# Design System: Tim's Window Cleaning

## Overview

**Creative North Star: "Clear Glass, Deep Water"**

The site looks like what a customer expects a good window cleaner to look like, executed with more care than any of the competitors: deep harbour-navy grounds, one clear window blue for every action, sky-blue highlights, and lots of white space. It is the category standard on purpose. The owner tried and rejected a bold concept look (an Ordnance Survey map with orange and magenta) as too bright and garish. Polish, not novelty, earns trust here.

The one memorable thing is the hero window: a dirty Georgian sash the visitor wipes clean (or lets Tim squeegee), followed by a rinse of pure water running down the glass. Everything else stays calm so that moment carries the page.

**Key Characteristics:**
- Navy sections (hero, pure water, quote) alternate with white and mist sections.
- One action colour: window blue on light, white on navy.
- Manrope at 800 with tight tracking for headings; 400 to 500 for reading.
- Soft rounded cards with layered, blue-tinted shadows; pill buttons and chips.
- No fake proof: no stock photos, reviews or badges until real ones exist.

## Colors

A single blue family from almost-black navy to pale sky, plus white.

### Primary
- **Window Blue** (#1F5FA8): primary buttons, selected chips and "On my quote" toggles, links on light grounds, the Newmarket marker, icon strokes.
- **Window Blue Deep** (#174C88): primary hover.

### Secondary
- **Sky** (#8FC5EE): highlights on navy (callout rings, contact icons, the postcode tick), step-line start, diagram water.
- **Sky Pale** (#D6E9F8): icon chips, FAQ toggles, text selection.
- **Bright Blue** (#3C8AD8): focus rings only.

### Neutral
- **Harbour Navy 800/900** (#0E2A47 / #0B2340): hero, pure-water and quote grounds (with soft radial sky glows).
- **Harbour Navy 950** (#071A2E): footer.
- **Mist** (#F3F8FC): alternate light sections and input fills.
- **Ink Text** (#0E2238) and **Slate Muted** (#4A5E74): body copy on light grounds.
- **On-dark** (#E8F1FA) and **On-dark Muted** (#AFC4D9): copy on navy.
- **Line** (#DCE6EF): hairline dividers.

**The One Action Colour Rule.** Window Blue is the only colour that means "do this" or "selected". On navy grounds the primary becomes white instead. No second accent.

## Typography

**Display and Body Font:** Manrope (self-hosted, 400 to 800), fallback system-ui.

**Character:** a clean, slightly geometric sans. Heavy and tightly tracked in headings, open and calm in text.

### Hierarchy
- **Display** (800, clamp(2.9rem, 6vw, 5rem), 1.02, -0.03em): hero headline only.
- **Headline** (800, clamp(2.2rem, 4.4vw, 3.4rem), 1.06): section titles.
- **Title** (700, 1.22rem, 1.3): service names, step titles, FAQ questions (1.12rem).
- **Body** (400, 1.0625rem, 1.65): copy at 34 to 42em max width; ledes 1.12 to 1.2rem; 500 weight on navy.
- **Label** (700, 0.97rem): form labels, buttons.

## Layout

Single page. 1200px container with clamp gutters; sections at clamp(4.5rem, 9vw, 7.5rem) vertical padding. Two-column intro and content splits collapse to one column at 900 to 960px. The services list runs as two columns inside one card and becomes one column at 820px. Steps run as four columns on a horizontal line, and become a vertical timeline at 900px. A sticky white header sits on top; under 900px it gains a menu toggle and a fixed navy quick-contact bar at the bottom.

## Elevation & Depth

Depth comes from tonal grounds (navy against mist and white) and soft layered shadows tinted with navy.

### Shadow Vocabulary
- **Card** (`0 1px 2px rgba(11,35,64,.06), 0 12px 32px -8px rgba(11,35,64,.14)`): the services card and the area-map card.
- **Quote card on navy** (`0 40px 80px -24px rgba(2,10,22,.6)`): the form card.
- **Primary button** (`0 6px 16px -6px rgba(31,95,168,.55)`): blue buttons on light grounds.
- **Window** (`drop-shadow(0 30px 40px rgba(2,10,22,.5))`) with a radial sky glow behind it.

## Shapes

Generous rounding: 10px inputs, 12px icon chips, 16px cards, 20px quote card. All buttons, chips and toggles are pills. Circles for step markers, callouts and FAQ toggles.

## Components

### Buttons
- **Shape:** pill (999px).
- **Primary:** Window Blue with white text, 50 to 56px tall. On navy it is white with navy text.
- **Outline:** transparent with a 1.5px navy border at 28% opacity (white at 40% on navy).
- **Hover / Focus:** a darker blue or pale-sky fill; a 3px Bright Blue focus ring with a 3px offset.

### Service toggle ("Add to my quote")
- A pill with a circular tick box. Selected: Window Blue fill, white text, white circle with a blue tick. It stays in sync with the form checkboxes.

### Chips (form)
- White pills with a #CBD8E5 border. Selected: Window Blue fill with a white box and blue tick (radio: inset ring).

### Cards / Containers
- White, 16px radius, card shadow, hairline internal dividers. The lead service row is a navy gradient band inside the card.

### Inputs
- Mist fill, 1.5px #CBD8E5 border, 10px radius, 52px tall. Focus: white fill, blue border, 4px soft blue ring. Error: red border on pale red.

### Hero window (signature)
- An inline SVG sash window (white frame, sky and Heath view) with a grime canvas the visitor wipes, a squeegee, and a water canvas for the rinse drips. Respects reduced motion.

## Do's and Don'ts

### Do:
- **Do** keep every action and selected state in Window Blue (#1F5FA8), or white on navy.
- **Do** alternate navy and light sections to pace the page.
- **Do** keep copy plain, British and short, and keep claims to what Tim has confirmed.

### Don't:
- **Don't** introduce bright or warm accents (orange, magenta, gold). The owner rejected them as garish.
- **Don't** bring back the map/Ordnance Survey concept or any other themed "world".
- **Don't** add stock photos, invented reviews, ratings or trust badges.
- **Don't** use gradient text or glassy blur panels.
