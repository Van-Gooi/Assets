# Van Gooi -- Copilot UI Style Guide

Version 2.0 -- Extended Digital & Product Guidelines

------------------------------------------------------------------------

# 1. Brand Foundation

## Brand Positioning

**Technically Ingenious**

Van Gooi builds engineered solutions. Interfaces must reflect
reliability, structure, and technical intelligence.

## Core Brand Traits → UI Translation

  Brand Trait   UI Translation
  ------------- ---------------------------------------
  Structured    Clear grid, predictable layouts
  Specialist    Strong hierarchy, precise spacing
  Direct        Clear language, high contrast
  Innovative    Controlled gradient use
  Pragmatic     Functional components over decoration

------------------------------------------------------------------------

# 2. Design Principles

1.  Engineer before decorating\
2.  Prioritize clarity over creativity\
3.  Maintain strict visual hierarchy\
4.  Reduce cognitive load\
5.  Use color with intent, never decoration

------------------------------------------------------------------------

# 3. Color System

## 3.1 Primary Colors

  Name           HEX       Usage
  -------------- --------- --------------------------------
  Black          #1C1C1C   Primary text, dark backgrounds
  Light Grey     #EDEDED   Backgrounds, surfaces
  Primary Blue   #372DFF   Primary actions, links
  Violet Blue    #3B4294   Secondary actions, depth

## 3.2 Secondary Colors

  Name          HEX       Usage
  ------------- --------- ---------------------
  Neon Green    #A6F205   Highlights, signals
  Apple Green   #52C200   Success states

## 3.3 Gradient

Primary Brand Gradient:\
#3B4294 → #372DFF

Use for: - Hero sections - CTA backgrounds - Highlight panels

Avoid overuse in dense UI environments.

## 3.4 Accessibility

-   Maintain WCAG AA contrast minimum
-   Never use neon green for body text
-   Ensure interactive states have visible contrast shift

------------------------------------------------------------------------

# 4. Typography

## 4.1 Primary Typeface

**Semplicita Pro** - Light - Bold

Used for: Headings, UI labels, navigation, buttons

## 4.2 Secondary Typeface

**Aptos** Used for formal documents and fallback system use

## 4.3 Type Scale

  Role    Size       Weight
  ------- ---------- --------
  H1      80px       Bold
  H2      52px       Bold
  H3      34px       Bold
  Body    18px       Light
  Small   14--16px   Light

## 4.4 Typography Rules

-   Maximum 2 weights per component
-   Avoid decorative italic usage
-   Maintain consistent line height (130--150%)
-   Prefer sentence case

------------------------------------------------------------------------

# 5. Layout & Spacing

## Grid System

Base grid: 10px modular system

Spacing scale: - 10px - 20px - 30px - 50px - 80px

## Layout Rules

-   Generous whitespace
-   Clear section separation
-   Avoid visual clutter
-   Use consistent vertical rhythm

------------------------------------------------------------------------

# 6. Component Guidelines

## 6.1 Buttons

### Primary Button

-   Background: #372DFF
-   Text: White
-   Font: Bold

Hover: Slight darkening or gradient shift\
Active: Slight inset effect

### Secondary Button

-   Border: #372DFF
-   Text: #372DFF
-   Background: Transparent

### Success State

-   Background: #52C200

### Disabled State

-   Background: #EDEDED
-   Reduced opacity

------------------------------------------------------------------------

## 6.2 Forms

-   Labels always visible
-   Clear error messages
-   Error color: subtle red (system defined)
-   Focus state: Blue highlight (#372DFF)

------------------------------------------------------------------------

## 6.3 Cards & Containers

-   Subtle elevation or border
-   Border radius: 6px or 12px
-   Avoid heavy shadows

------------------------------------------------------------------------

## 6.4 Icons

-   Line-based
-   Geometric
-   Consistent stroke width
-   No playful illustrations

------------------------------------------------------------------------

# 7. Interaction Design

-   Motion should be purposeful
-   Keep transitions under 200ms
-   Avoid elastic or playful animations
-   Feedback must be immediate and clear

------------------------------------------------------------------------

# 8. Tone of Voice (UI Microcopy)

## Characteristics

-   Direct
-   Honest
-   Technical
-   Action-oriented

## Examples

Instead of: "We are excited to get started!"

Use: "Start configuration."

Instead of: "Oops! Something went wrong!"

Use: "Configuration failed. Check connection."

------------------------------------------------------------------------

# 9. Do's & Don'ts

## Do

-   Use strong hierarchy
-   Apply blue as primary accent
-   Keep layouts structured
-   Maintain consistent spacing

## Don't

-   Overuse gradients
-   Add decorative shapes
-   Use playful language
-   Mix too many accent colors

------------------------------------------------------------------------

# 10. UI Identity Summary

Van Gooi interfaces must feel:

-   Engineered
-   Reliable
-   Structured
-   Confident
-   Technically intelligent

Not:

-   Playful
-   Experimental
-   Decorative
-   Trend-driven

------------------------------------------------------------------------

# Engineering-Led UI/UX & Accessibility Guidelines

## 1. Color & Contrast (WCAG 2.1 AA Standards)
- **Standard Text:** Maintain a minimum contrast ratio of 4.5:1 for normal text (under 18pt/24px).
- **Large Text:** Maintain a minimum contrast ratio of 3:1 for text at or above 18pt/24px.
- **UI Components:** Graphical objects and user interface components (borders, icons, focused states) must have a contrast ratio of at least 3:1.
- **Non-Color Indicators:** Do not use color as the only visual means of conveying information (e.g., use icons or underlines in addition to color for error states or links).

## 2. Layout, Spacing & Sizing
- **Touch Targets:** All interactive elements (buttons, links, inputs) must have a minimum hit area of 44x44px.
- **Spacing System:** Follow a strict 8px (0.5rem) linear scale for all padding, margins, and gaps. Avoid "magic numbers" (e.g., 7px, 13px).
- **Responsive Units:** Use `rem` or `em` for font sizes and spacing to ensure layouts scale with user browser settings. Do not hardcode `px` for typography.
- **Grid:** Use CSS Grid or Flexbox with `gap` properties rather than manual margin-right calculations to ensure layout consistency.

## 3. Semantic HTML & ARIA
- **Heading Hierarchy:** Use `<h1>` through `<h6>` in a strict sequential order. Do not skip levels (e.g., do not go from `<h2>` to `<h4>`).
- **Interactive Elements:** Use `<button>` for actions and `<a>` for navigation. Do not attach click handlers to `<div>` or `<span>` without providing `role="button"` and `tabindex="0"`.
- **Form Labels:** Every `<input>`, `<select>`, and `<textarea>` must have a programmatically associated `<label>` via the `for`/`id` attributes.
- **Images:** All `<img>` tags must include an `alt` attribute. Use descriptive text for functional images and `alt=""` (empty) for purely decorative images.

## 4. State & Feedback
- **Focus States:** Never remove default focus outlines (`outline: none`) without providing a high-contrast CSS `:focus-visible` alternative.
- **Loading States:** Provide `aria-busy="true"` and `aria-live` regions for dynamic content updates.
- **Error Handling:** Form errors must be linked to their respective inputs using `aria-describedby`.

End of Document
