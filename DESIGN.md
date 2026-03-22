# Design System Document: IBRACI Digital Identity

## 1. Overview & Creative North Star: "The Urban Architect"
The design system for IBRACI is built upon the **"Urban Architect"** Creative North Star. It rejects the "flat" web in favor of a layered, multi-dimensional experience that mimics the complexity and interconnectedness of a modern Smart City. 

The system moves beyond generic administration templates by utilizing **Editorial Sophistication**. We achieve this through:
*   **Intentional Asymmetry:** Shifting text blocks and using generous, uneven white space to guide the eye dynamically.
*   **Atmospheric Layering:** Using background color shifts instead of lines to create a sense of physical environment.
*   **Human-Centric Data:** Balancing hard technical data with warm, oversized typography and soft organic shapes.

This is a system that feels authoritative yet accessible—professional enough for government officials, yet modern enough for citizens and tech innovators.

---

## 2. Colors: Tonal Architecture
Color is used to define space rather than just decorate it. We employ a rigorous "No-Line" strategy to ensure the UI feels expansive and premium.

### The Palette
*   **Primary (The Foundation):** `primary` (#002a3c) and `primary_container` (#00415a). These deep teals represent institutional trust and deep-sea stability.
*   **Secondary (The Pulse):** `secondary` (#00658d) and `secondary_container` (#41befd). Used for technology-driven accents, highlights, and interactive elements.
*   **Tertiary (The Vitality):** `tertiary` (#192b16) and `tertiary_container` (#2e412a). A sophisticated sage-derived dark green representing sustainability and urban greening.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to separate sections. Boundaries must be defined through:
1.  **Background Shifts:** Placing a `surface_container_low` section directly against a `surface` background.
2.  **Tonal Transitions:** Using subtle gradients between `primary` and `primary_container` for hero regions.

### Glass & Gradient Strategy
To evoke "Smart Cities," use **Glassmorphism** for floating cards and navigation bars.
*   **Recipe:** Use a semi-transparent `surface_container_lowest` (approx. 80% opacity) with a `backdrop-blur` of 20px. 
*   **Signature Texture:** Main CTAs should utilize a 45-degree linear gradient from `secondary` to `secondary_container` to create a "glowing" tech-forward energy.

---

## 3. Typography: Editorial Authority
We pair the technical precision of **Inter** with the architectural character of **Manrope**.

*   **Display Scale (Manrope):** Use `display-lg` (3.5rem) and `display-md` (2.75rem) for hero statements. These should be set with tight letter-spacing (-0.02em) to feel solid and intentional.
*   **Headline Scale (Manrope):** Use `headline-lg` (2rem) for section titles. This font conveys the "Smart City" structural feel.
*   **Body & Labels (Inter):** Use `body-lg` (1rem) for general reading. Inter’s high x-height ensures readability in data-heavy contexts.
*   **Visual Hierarchy:** Pair a large `display-md` headline with a `label-md` in all-caps (using `primary_container`) to create an editorial, magazine-style contrast.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are a last resort. Depth in this design system is achieved through physical "stacking."

*   **The Layering Principle:** 
    *   Level 0: `surface` (Base)
    *   Level 1: `surface_container_low` (Section backgrounds)
    *   Level 2: `surface_container_lowest` (White cards/content blocks)
    *   This "white-on-grey" stacking creates a natural lift without visual clutter.

*   **Ambient Shadows:** When a float is required (e.g., a primary CTA or a Modal), use the following shadow:
    *   `box-shadow: 0 12px 32px -4px rgba(0, 30, 44, 0.08);`
    *   Notice the shadow is tinted with a dark teal (`on_primary_fixed`) rather than black, making the shadow feel like it belongs to the environment.

*   **The "Ghost Border" Fallback:** If a container must be defined against a similar background, use `outline_variant` at 15% opacity. Never use 100% opaque outlines.

---

## 5. Components: Precision Primitives

### Buttons
*   **Primary:** High-pill shape (`rounded-full`). Gradient from `secondary` to `secondary_container`. White text.
*   **Secondary:** `surface_container_highest` background with `on_surface` text. No border.
*   **Tertiary (Ghost):** No background. `secondary` text color with a heavy weight (Semi-bold).

### Cards & Data Lists
*   **Rule:** Forbid divider lines. 
*   **Cards:** Use `rounded-xl` (1.5rem) and `surface_container_lowest`. Separate content within the card using the Spacing Scale (e.g., `spacing-8` between header and body).
*   **Lists:** Separate list items by alternating between `surface` and `surface_container_low` background fills.

### Input Fields
*   **Style:** `surface_container_high` backgrounds with `rounded-md` corners. 
*   **State:** On focus, the background shifts to `surface_container_lowest` and gains a 2px "Ghost Border" of `secondary`.

### Interactive Chips
*   **Selection:** Use `primary_fixed` with `on_primary_fixed` text for active states to ensure high contrast and a "tech-chip" aesthetic.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use overlapping elements (e.g., an image bleeding 20px into the section below) to break the "grid-box" feel.
*   **Do** use `tertiary_fixed` (sage green) as a background for sustainability-focused modules to signal a tonal shift from "tech" to "human/nature."
*   **Do** prioritize `spacing-24` (6rem) between major sections to allow the "Smart City" concepts room to breathe.

### Don’t:
*   **Don’t** use pure black (#000000) for text. Use `on_surface` (#171c1f) for better optical comfort.
*   **Don’t** use hard shadows. If you can clearly see where the shadow starts and ends, it is too heavy.
*   **Don’t** use standard 4px "web-default" border radii. Adhere strictly to the `rounded-lg` (1rem) and `rounded-xl` (1.5rem) scale to maintain the "friendly" human-centric touch requested.