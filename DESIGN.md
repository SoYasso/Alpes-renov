```markdown
# Design System Specification: Industrial Excellence

## 1. Overview & Creative North Star

### Creative North Star: "The Architectural Monolith"
This design system moves away from the cluttered, "loud" aesthetics typical of the construction industry. Instead, it adopts the persona of an architectural firm—stable, precise, and premium. We lean into the concept of **Architectural Brutalism meets High-End Editorial**. 

The design breaks the standard grid through intentional asymmetry, mimicking the structural complexity of scaffolding. We prioritize massive, authoritative typography and deep, layered tonal shifts to communicate safety and institutional trust. Elements should feel like they have been "engineered" rather than just placed.

## 2. Colors

The palette is rooted in a deep, midnight foundation (`background: #121416`) contrasted by a high-visibility structural amber (`primary: #fdbb24`).

### The "No-Line" Rule
To achieve a high-end feel, **1px solid borders are strictly prohibited for sectioning.** We do not use lines to separate content. Boundaries must be defined through background color shifts. For example, a card utilizing `surface-container-high` should sit on a section using `surface` or `surface-container-low`. The change in hex value is the only divider needed.

### Surface Hierarchy & Nesting
Think of the UI as a physical site with different elevations:
- **Foundation:** `surface` (#121416) – Use for main page backgrounds.
- **Sub-structure:** `surface-container-low` (#1a1c1e) – Use for secondary content areas.
- **Elevated Platforms:** `surface-container-high` (#282a2c) – Use for interactive cards or floating panels.
- **Top-Tier:** `surface-bright` (#37393b) – Use for hover states or high-focus micro-containers.

### Signature Textures & Glassmorphism
To avoid a "flat" industrial look, apply a subtle linear gradient to primary CTAs transitioning from `primary` (#fdbb24) to `on_primary_container` (#a87900) at a 135-degree angle. For floating navigation or overlays, use a semi-transparent `surface` color with a `20px` backdrop-blur to create a "Smoked Glass" effect.

## 3. Typography

The system utilizes a dual-font strategy: **Manrope** for structural impact (Display/Headlines) and **Inter** for technical precision (Body/Labels).

*   **Display (Manrope):** Large-scale, heavy weights. Use `display-lg` (3.5rem) for hero statements. This font represents the "Facade"—bold, clean, and impressive.
*   **Body (Inter):** High readability, medium tracking. Use `body-md` (0.875rem) for technical descriptions. This represents the "Safety Manual"—clear, objective, and functional.

**Hierarchy as Identity:** Use `primary` (#fdbb24) sparingly in typography—only for high-impact keywords or active states. The majority of headlines should be `on_surface` (#e2e2e5) to maintain a professional, dark-mode sophistication.

## 4. Elevation & Depth

### The Layering Principle
Depth is achieved by stacking tonal tiers. To lift a card, do not reach for a shadow first; reach for a higher surface token. A `surface-container-highest` card placed on a `surface` background creates a natural, "physical" lift.

### Ambient Shadows
When absolute separation is required (e.g., a floating quote or a modal), use an **Ambient Shadow**:
- **Color:** Hex `0c0e10` (Surface Container Lowest) at 40% opacity.
- **Blur:** 40px - 60px.
- **Spread:** -10px (to keep the shadow "tucked" under the element).

### The "Ghost Border" Fallback
If an element lacks contrast against a background, use a **Ghost Border**: `outline-variant` (#44474b) at 15% opacity. This provides a structural hint without creating a visual "hard stop."

## 5. Components

### Buttons
*   **Primary:** Solid `primary` (#fdbb24) with `on_primary` (#412d00) text. Border radius: `DEFAULT` (0.25rem) to maintain a sharp, industrial edge. No rounded pills.
*   **Secondary:** Glassmorphism style. Background: `surface-variant` at 20% opacity with a `20px` backdrop blur. 
*   **Tertiary:** Text-only with an underline that appears on hover using the `primary` color.

### Input Fields
*   **Default State:** Background: `surface-container-highest`. No border.
*   **Focus State:** A 2px bottom-border using `primary`. The rest of the container remains borderless. This mimics architectural drafting lines.

### Cards & Lists
*   **Strict Rule:** No dividers. Use `spacing-8` (2rem) or `spacing-12` (3rem) to let content breathe.
*   **Structural Grid:** Use the `roundedness-sm` (0.125rem) for small image containers and `roundedness-DEFAULT` (0.25rem) for larger cards to maintain a "machined" look.

### Additional Industrial Components
*   **The "Safety Badge":** Small, high-contrast labels using `label-sm` in all-caps, with a `0.1em` letter spacing. Used for certifications (e.g., "ISO 9001").
*   **Status Indicator:** Use a small circular dot of `primary` next to text to indicate "Active Project" or "Available Equipment."

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts. Let images of scaffolding bleed off the edge of the screen to suggest scale.
*   **Do** use `primary` (#fdbb24) as a precision tool. It should feel like a laser level—thin lines, small icons, or specific callouts.
*   **Do** embrace negative space. Industrial design is about efficiency; your UI should not feel "crowded."

### Don't
*   **Don't** use standard 1px borders. It cheapens the "Architectural" feel.
*   **Don't** use pure white (#ffffff) for large text. Use `on_surface` (#e2e2e5) to reduce eye strain in dark environments.
*   **Don't** use rounded "pill" shapes (9999px). They are too soft for a scaffolding and facade brand. Stick to `DEFAULT` (4px) or `sm` (2px) corners.
*   **Don't** use generic stock photography. Use high-contrast, wide-angle shots of steel, glass, and geometric construction patterns.```