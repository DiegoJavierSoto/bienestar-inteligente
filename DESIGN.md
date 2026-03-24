# Design System Document: Bienestar Inteligente by Generación +

## 1. Overview & Creative North Star

### Creative North Star: "The Editorial Sanctuary"
The design system for 'Bienestar Inteligente' is not a typical utility-first interface; it is a digital sanctuary. We move beyond "Modern" into a space of **Editorial Mindfulness**. This system prioritizes the user's mental state by utilizing a "High-End Editorial" aesthetic—characterized by bold, authoritative serif typography, an expansive sense of air (white space), and a sophisticated layering of organic tones.

To break the "template" look, we employ **Intentional Asymmetry**. Do not center-align every hero; instead, use the `24` (8.5rem) spacing token to create wide, off-balance margins that guide the eye through content like a luxury wellness magazine. We use overlapping elements—such as a `surface-container-lowest` card bleeding over a `primary-container` background—to create a sense of tactile depth and human touch.

---

## 2. Colors

Our palette transitions from the calming groundedness of deep forest greens to the energizing vitality of soft lime and warm neutrals.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited for sectioning.** To define boundaries, you must use shifts in background tokens. For example, a content block using `surface-container-low` (#f2f4f2) should sit directly against a `surface` (#f8faf8) background. The eye should perceive the change in "weight" rather than a hard edge.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine papers.
*   **Base:** `surface` (#f8faf8).
*   **Secondary Sections:** `surface-container-low` (#f2f4f2).
*   **Elevated Content/Cards:** `surface-container-lowest` (#ffffff).
*   **Interactive Callouts:** `tertiary-fixed` (#d2e8d8).

### The "Glass & Gradient" Rule
To add "soul" to the digital experience, use **Glassmorphism** for floating navigation or overlay modals. Use a semi-transparent `surface` color with a `backdrop-filter: blur(20px)`. 
For Hero CTAs, utilize a subtle linear gradient (135°) from `primary` (#426604) to `primary-container` (#5a8021). This creates a "glow" effect that feels alive and premium.

---

## 3. Typography

The typography strategy is a dialogue between **Wisdom (Noto Serif)** and **Clarity (Work Sans)**.

*   **Display & Headlines (Noto Serif):** Use these to convey the authority of a coaching program. High-contrast sizing (e.g., `display-lg` vs. `body-md`) is encouraged to create a rhythmic, editorial flow.
*   **Body & Titles (Work Sans):** Chosen for its modern, approachable geometry. It ensures that complex wellbeing advice remains accessible and easy to digest.
*   **Labels (Inter):** Reserved for functional metadata and micro-copy, providing a "technical" counterpoint to the organic serif headings.

---

## 4. Elevation & Depth

We reject traditional shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container` background creates a soft, natural lift.
*   **Ambient Shadows:** If a floating element (like a FAB or Popover) requires a shadow, use a large blur (`32px`+) with a low-opacity tint of `on-surface` (e.g., `rgba(25, 28, 27, 0.06)`). Never use pure black shadows; they feel "dirty" in a wellness context.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use the `outline-variant` (#c4c9b6) at **15% opacity**. It should be felt, not seen.
*   **Roundedness:** Lean into the `xl` (1.5rem) scale for large containers and `full` (9999px) for buttons. This removes "aggression" from the UI, making it feel safe and welcoming.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` (#426604) with `on-primary` (#ffffff) text. Use `full` rounding. Padding: `spacing-3` (top/bottom) and `spacing-6` (left/right).
*   **Secondary:** `primary-fixed-dim` (#a9d46c) with `on-primary-fixed` (#111f00). No border.
*   **Tertiary:** Text-only using `primary` (#426604) with a `spacing-0.5` underline that appears on hover.

### Cards & Content Lists
**Forbid the use of divider lines.** To separate list items, use `spacing-4` (1.4rem) of vertical white space or alternate background tones between `surface-container-low` and `surface`. 

### Input Fields
Avoid the "boxed" look. Use `surface-container-high` as the background fill with a `rounded-md` (0.75rem) corner. The label should be in `label-md` using `on-surface-variant`. Error states use `error` (#ba1a1a) for the text and a `ghost-border` of the same color.

### Additional Signature Components
*   **The "Moment of Reflection" Card:** A large, `surface-container-lowest` container with `xl` rounding, featuring a `display-sm` quote in Noto Serif and heavy `spacing-12` padding.
*   **The Vitality Progress Bar:** Using a gradient from `secondary` (#576400) to `primary` (#426604) to visualize growth and energy levels.

---

## 6. Do’s and Don’ts

### Do:
*   **DO** use whitespace as a functional element. If a section feels "crowded," double the spacing token (e.g., move from `8` to `16`).
*   **DO** use high-quality, authentic imagery. Photos should feature natural light, organic textures (linen, wood, leaves), and genuine human emotion.
*   **DO** use `tertiary-fixed` (#d2e8d8) for success messages or "calm" notifications.

### Don’t:
*   **DON’T** use 100% black typography. Always use `on-surface` (#191c1b) for readability and softness.
*   **DON’T** use sharp 90-degree corners. Everything must feel "honed" and "smooth" to the touch.
*   **DON’T** use standard grid layouts for everything. Occasionally break the alignment of an image to the right or left to create an editorial, boutique feel.
*   **DON’T** use heavy, saturated blue for primary actions. Stick to the `primary` green tokens to maintain brand alignment with 'Generación +'.