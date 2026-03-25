# Design System Specification: Editorial Authority & Empathetic Precision

## 1. Overview & Creative North Star: "The Modern Archivist"
This design system is anchored by the **Creative North Star: The Modern Archivist.** It rejects the "disposable" feel of generic SaaS interfaces in favor of a high-end, editorial aesthetic that feels both permanent and human. 

The system balances the **authoritative weight** of Japanese typography with the **empathetic warmth** of an off-white, paper-like surface. We move beyond the "template" look by using rigid, brutalist grid alignments juxtaposed against sophisticated tonal layering. This is a system of "Quiet Power"—where the absence of traditional borders creates a more expansive, intentional user journey.

---

## 2. Color & Surface Architecture
We utilize a palette that mimics physical materials: ink-heavy navies, oxblood accents, and parchment surfaces.

### The "No-Line" Rule
To achieve a premium, custom feel, **1px solid borders are prohibited for sectioning.** Boundaries must be defined through background color shifts or the "Ghost Border" principle. 
- Use `surface-container-low` (#f7f3ee) for large secondary sections.
- Use `surface-container-high` (#ebe8e3) to draw focus to utility panels.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked fine papers. 
- **Base Layer:** `surface` (#fdf9f4).
- **Embedded Content:** Place a `surface-container-lowest` (#ffffff) card on a `surface-container-low` (#f7f3ee) section to create a soft, natural lift without a shadow.

### Signature Textures & Glass
- **Subtle Gradients:** For primary CTAs, use a linear gradient from `primary` (#00000b) to `primary-container` (#1a1a2e). This provides a "lacquered" depth that feels high-end.
- **The Glass Rule:** For floating navigation or modal overlays, use `surface` (#fdf9f4) at 85% opacity with a `24px` backdrop-blur. This softens the interface and prevents it from feeling "pasted on."

---

## 3. Typography: The Editorial Voice
Typography is the primary vehicle for the brand’s authority.

| Level | Token | Font Family | Size | Character Spacing |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | Noto Serif JP (900) | 3.5rem | -0.02em |
| **Headline** | `headline-md` | Noto Serif JP (700) | 1.75rem | 0 |
| **Title** | `title-lg` | Public Sans (600) | 1.375rem | 0 |
| **Body** | `body-md` | Public Sans (400) | 0.875rem | 0.01em |
| **Metadata** | `label-md` | Public Sans (700) | 0.75rem | **0.15em (Uppercase)** |

**The Typographic Tension:** Pair the heavy, serif `display-lg` headings with wide-tracked, uppercase `label-md` metadata. This high-contrast pairing (Traditional Serif vs. Technical Sans) is the hallmark of this system's sophisticated identity.

---

## 4. Elevation & Depth
In this system, depth is felt, not seen. We avoid the "floating card" clichés of the early 2010s.

*   **Tonal Layering:** Always default to color shifts over shadows. Use `surface-dim` (#ddd9d5) to create a sense of recession for background utility areas.
*   **Ambient Shadows:** If a floating element is required (e.g., a dropdown), use a shadow tinted with `on-surface` (#1c1c19) at 5% opacity with a `32px` blur. It should look like a soft shadow cast on paper, not a digital glow.
*   **The "Ghost Border":** For input fields or cards where separation is critical for accessibility, use `outline-variant` (#c8c5cd) at **15% opacity**. This creates a "suggestion" of a boundary that maintains the minimalist ethos.

---

## 5. Component Strategy
All components follow a **0px Border Radius** (Strict Square) policy to maintain an authoritative, architectural feel.

*   **Buttons:**
    *   **Primary:** `primary` background with `on-primary` text. Use the "Lacquered Gradient" (Primary to Primary-Container) on hover.
    *   **Secondary:** `secondary` (#b02d21) background. Reserve this strictly for high-priority conversion or "New" actions.
*   **Cards & Lists:** Prohibit divider lines. Use `spacing-8` (1.75rem) of vertical white space to separate list items. Use a `surface-container-low` background on hover to indicate interactivity.
*   **Input Fields:** Use a "Bottom-Line Only" approach or a very faint "Ghost Border." Labels must use `label-sm` in uppercase with wide tracking to look like an architectural drawing.
*   **Coming Soon (Tertiary):** Elements using `tertiary` (#2d7a4f) should be styled with a subtle SVG dot-matrix pattern to indicate their "under construction" status, adding a tactile texture to the minimalist grid.

---

## 6. Do’s and Don'ts

### Do:
*   **Embrace Asymmetry:** Align text to a strict left-hand grid while leaving significant "white space" on the right to allow the layout to breathe.
*   **Use Vertical Text:** For metadata labels or section sidebars, occasionally use vertical text orientations to lean into the Japanese editorial influence.
*   **Strict Grid Alignment:** Ensure every element snaps to the `spacing-px` grid. In a minimalist system, a 1px misalignment is an eyesore.

### Don't:
*   **No Rounded Corners:** Never use `border-radius`. Everything is a sharp, intentional 90-degree angle.
*   **No Default Shadows:** Avoid the standard "Material Design" shadow levels. If it doesn't look like natural light hitting paper, don't use it.
*   **No Pure Black:** Use `primary` (#00000b) or `on-surface` (#1c1c19) for text to maintain a premium, ink-like softness. Pure #000000 is too digital and harsh for this system.