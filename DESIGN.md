# Design System Strategy: The Cinematic Monolith

## 1. Overview & Creative North Star
The "Creative North Star" for this design system is **The Cinematic Monolith**. 

This system moves away from the cluttered, "dashboard-style" density of typical SaaS products. Instead, it treats every screen as a premium editorial layout. It is defined by the tension between absolute darkness (#000000) and laser-precise structural lines. We reject "safe" padding and standard grids in favor of extreme whitespace and intentional asymmetry. By utilizing a "Massive" typographic scale against a void-like background, we create a sense of authority and AI-native sophistication. The UI doesn't just display information; it "curates" it.

## 2. Colors
The palette is rooted in the "Dark Mode Luxury" aesthetic. It utilizes pure black as the foundation to allow high-end imagery and massive typography to emerge from the background.

*   **Primary Background (`surface-container-lowest`):** #000000. This is the bedrock.
*   **Surface Hierarchy (`surface` to `surface-bright`):** Use #0e0e0e and #131313 for sectioning. 
*   **The "No-Line" Rule for Depth:** While the global layout uses structural grid lines, internal components must prohibit 1px solid borders for sectioning content. Instead, boundaries are defined by shifting from `surface` (#0e0e0e) to `surface-container-low` (#131313). This creates a "soft" edge that feels more organic and premium.
*   **The "Glass & Gradient" Rule:** To provide "soul" to the AI-native experience, floating elements (like the navigation bar or specific CTAs) must utilize Glassmorphism. Apply `surface-container-high` at 60% opacity with a 20px backdrop-blur. 
*   **Signature Textures:** For primary CTAs, do not use flat colors. Use a subtle linear gradient transitioning from `primary` (#c6c6c7) to `primary-container` (#454747) at a 45-degree angle to provide a metallic, high-end finish.

## 3. Typography
Typography is the primary vehicle for the brand’s voice. We use **DM Sans** to achieve a modern, geometric, yet approachable feel.

*   **Display-Massive (H1):** 120px / 1.1 Leading / -0.04em Tracking. Used for singular, impactful statements. It should feel "too big" for the screen, forcing the user to acknowledge the scale.
*   **Display-Large (H2):** 72px / 1.2 Leading / -0.02em Tracking. Used for primary section headers.
*   **Body-Editorial:** 20px–28px. Unlike standard web text (16px), our body text is intentionally oversized to maintain the "Editorial" feel. Use `on-surface-variant` (#8A8F9A) for secondary body copy to maintain a sophisticated hierarchy.
*   **Label-Caps:** 12px / 0.1em Tracking / All Caps. Used for "AI-Native" metadata or small eyebrow tags.

## 4. Elevation & Depth
In a pure black environment, traditional shadows often fail. We achieve depth through **Tonal Layering** and **Structural Scaffolding**.

*   **The Layering Principle:** Depth is achieved by "stacking" surface tiers. An active card should not have a shadow; it should simply be one tier lighter than the background it sits on (e.g., a `surface-container-high` card on a `surface` background).
*   **The Grid Scaffold:** Use the `outline-variant` (#626B7A) for thin, 1px horizontal and vertical lines that run to the edges of the viewport. This creates a "blueprint" look that feels engineered and precise.
*   **Ambient Glow:** When a floating effect is required (e.g., a modal), use a shadow with a 100px blur and 4% opacity, tinted with `primary` (#c6c6c7) to mimic the subtle light bleed of a high-end display.
*   **The "Ghost Border":** If a border is required for input fields or buttons, use the `outline` token at 20% opacity. Never use 100% opaque borders for interior elements; they break the cinematic flow.

## 5. Components

### Buttons
*   **Primary:** Capsule shape (Full Roundedness). Background: Linear gradient (Primary to Primary-Container). Text: #000000. 
*   **Secondary:** Ghost style. 1px border using `outline` at 30% opacity. Text: #FFFFFF.
*   **Tertiary:** Text-only with a "trailing-arrow" icon. On hover, the arrow should slide 4px to the right.

### Cards & Lists
*   **Strict Rule:** No divider lines between list items. Use 48px–64px of vertical whitespace (Spacing Scale) to separate items.
*   **Grid Cards:** Anchored to the 1px structural grid. On hover, the background shifts from `surface` to `surface-bright`.

### Input Fields
*   **Minimalist State:** No background. 1px bottom-border only (#626B7A). 
*   **Active State:** The bottom border transforms into a `primary` (#c6c6c7) glow. Label text (DM Sans 14px) floats above in `on-surface-variant`.

### Selection Chips
*   **AI-Native Chips:** Small, fully rounded, using `surface-container-highest`. Use for category tags or AI-generated keywords. Text should be `label-sm` in `primary` color.

## 6. Do's and Don'ts

### Do:
*   **Embrace the Void:** Leave large areas of #000000 untouched. Whitespace is a luxury.
*   **Align to the Grid:** Ensure every element, especially massive typography, is snapped to the 1px structural lines.
*   **Use High-Contrast Images:** Use photography with deep blacks and singular light sources to match the UI.

### Don't:
*   **Don't use standard grey backgrounds:** Avoid #333333 or #222222. Stick to the specified `surface` tokens to maintain the "Pure Black" luxury.
*   **Don't use 16px body text:** It will look lost and "cheap" next to the 120px headers. Stick to the 20px-28px range.
*   **Don't use rounded corners over 8px (except for buttons):** This system is architectural. Use `DEFAULT` (4px) or `none` (0px) for cards to maintain a sharp, engineered edge.