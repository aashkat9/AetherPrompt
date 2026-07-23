# AetherPrompt Data Architecture

Below is the pure data structure and logic mapping that powers AetherPrompt. This outlines the application state, available parameters, and the literal strings injected into the final LLM prompt.

## 1. Application State Object

The core data model holding the user's current selections.

```json
{
  "step": 1,
  "config": {
    "framework": "html-css",
    "audience": "creatives",
    "archetype": "high-tech",
    "flavor": "corporate",
    "emotion": "calm",
    "typography": "sans",
    "primaryHex": "#9141AC",
    "secondaryHex": "#06B6D4",
    "harmony": "monochromatic",
    "neutrals": "slate",
    "contrast": "aa",
    "semantics": "pastels",
    "surfaceBase": "zinc",
    "surfaceMaterial": "acrylic",
    "elevation": "flat",
    "borders": "hairline",
    "navigation": "dock",
    "grid": "center"
  }
}

```

---

## 2. Parameter Mappings & Descriptions

### Step 1: Core Stack & Audience

* **Framework (`framework`)**
* `react` -> React 19 (TSX, Functional Hooks)
* `svelte` -> SvelteKit 2.0 (Svelte 5 Runes)
* `vue` -> Vue 3 (Composition API)
* `html-css` -> Pure Semantic HTML5 + Custom CSS


* **Target Audience (`audience`)**
* `developers` -> Developers & Engineers (Prioritizes extreme data density and keyboard-centric navigation)
* `enterprise` -> Enterprise Executives (Prioritizes high-level KPI summaries and clean charts)
* `gen-z` -> General Consumers / Gen-Z (Prioritizes mobile-first thumb zones and gamification)
* `creatives` -> Creatives & Designers (Prioritizes pixel-perfect alignment and experimental layouts)



### Step 2: Identity & Vibe Engine

* **Base Archetype (`archetype`)**
* `high-tech` -> High-Tech & Developer-First interface. Draw inspiration from tiling window managers, IDEs, and CLI environments. Utilize strict grid alignments, exposed structural borders, and dense monospaced telemetry data. Prioritize function, keyboard-navigability, and raw utility over decorative flourishes. The visual language should feel like a native, high-performance developer tool with visible state indicators and highly structured data panes.
* `corporate` -> Corporate Clean interface. Establish absolute user trust through conventional, highly predictable UX patterns. Utilize balanced, symmetrical layouts, clear visual hierarchies, and stark contrast. Components should feel robust, fully accessible, and modular. The design language must echo enterprise-grade dashboards—prioritizing clarity, compliance, and frictionless user flows over experimental aesthetics.
* `luxury` -> Ultra-Premium & Luxury interface. Embrace vast negative space and deliberate, editorial pacing. Use delicate hairline dividers, slow cinematic transitions, and precise, highly intentional typographic scales. The UI should feel curated, bespoke, and quiet, requiring the user to slow down and appreciate the content. Avoid overwhelming data density in favor of high-impact, singular focal points.
* `web3` -> Web3 & Crypto Avant-Garde interface. Push modern browser capabilities with dark-mode native aesthetics. Incorporate hardware-accelerated floating elements, deeply saturated neon glows against pitch-black canvases, and frosted glass panels. The layout should feel decentralized, cutting-edge, and highly spatial, blending complex financial data visualization with immersive, high-tech branding.
* `playful` -> Playful, Quirky & Approachable interface. Break the rigidity of standard grids with organic shapes, bouncy micro-interactions, and asymmetric layouts. Utilize bold, slightly exaggerated UI elements, soft geometry, and gamified feedback states. The interface should feel alive, friendly, and inherently tactile, prioritizing user delight and engagement without sacrificing core usability.
* `academic` -> Academic & Research-Heavy interface. Focus ruthlessly on legibility and information architecture. Draw inspiration from rigorous typesetting, LaTeX documents, and scientific journals. Utilize dense, highly structured data tables, strict center-focused reading columns, and subtle footnote/citation patterns. The design must elegantly handle massive text and data density without inducing cognitive overload.


* **Flavor Mix (`flavor`)** - *Dynamically filtered based on Archetype compatibility*
* `corporate` -> Corporate Clean
* `modern` -> Modern App Tech
* `web3` -> Web3/Crypto
* `minimalist` -> Minimalist
* `academic` -> Academic
* `editorial` -> Editorial
* `high-tech` -> High-Tech
* `glitch` -> Glitch Art
* `playful` -> Playful
* `retro` -> Retro


* **Core Emotion (`emotion`)**
* `stable` -> Secure & Stable
* `bold` -> High-Energy & Bold
* `calm` -> Calm & Minimal
* `edgy` -> Edgy & Disruptive


* **Typography (`typography`)**
* `sans` -> Modern Sans-Serif
* `serif` -> Elegant Serif
* `mono` -> Strict Monospace
* `mixed` -> Mixed (Serif headers, Sans body)



### Step 3: Color Engine & Material Physics

* **Colors (`primaryHex`, `secondaryHex`)**
* Direct string injection of 6-character hex codes (e.g., `#9141AC`, `#06B6D4`).


* **Harmony Strategy (`harmony`)**
* `monochromatic` -> Monochromatic
* `analogous` -> Analogous
* `complementary` -> Complementary
* `split` -> Split-Complementary


* **Neutral/Grayscale Scale (`neutrals`)**
* `slate` -> Slate (Cool, blue-tinted grays)
* `zinc` -> Zinc (Standard Tech)
* `neutral` -> Neutral (Pure Grayscale)
* `stone` -> Stone (Warm/Earthy)


* **Accessibility Target (`contrast`)**
* `aa` -> WCAG AA (4.5:1)
* `aaa` -> WCAG AAA (7:1)
* `edge` -> High Contrast Edge Mode
* `subdued` -> Aesthetic Subdued


* **Semantic States (`semantics`)**
* `vivid` -> Vivid Standard (R/G/Y)
* `pastels` -> Muted Pastels
* `neon` -> Neon High-Vis
* `mono` -> Strict Monochrome


* **Dark Mode Surface Root (`surfaceBase`)**
* `oled` -> Pitch Black OLED
* `zinc` -> Deep Zinc
* `navy` -> Midnight Navy


* **Surface Material & Textures (`surfaceMaterial`)**
* `matte` -> Opaque Matte
* `glass` -> Glassmorphism (backdrop-blur)
* `acrylic` -> Saturated Acrylic (Heavy backdrop-blur + saturate-150)
* `ghost` -> Wireframe/Ghost


* **Shadow & Elevation Paradigm (`elevation`)**
* `ambient` -> Soft Ambient Diffusion (Apple UX)
* `hard` -> Hard Solid Offset (Neo-brutalism)
* `neon` -> Colored Neon Glows
* `material` -> Strict Material Elevation
* `flat` -> Flat UI (Absolutely no box-shadow properties)


* **Border Execution Strategy (`borders`)**
* `hairline` -> Hairline Translucent (1px, highly transparent white borders like border-white/10)
* `thick` -> Thick Structural
* `gradient` -> Gradient Strokes
* `none` -> Strictly Borderless



### Step 4: Navigation & Layout

* **Navigational Architecture (`navigation`)**
* `island` -> Apple Dynamic Island (Floating expanding pill)
* `cmdk` -> Zero-Nav / Cmd+K Driven (Search palette only)
* `dock` -> Floating Icon Sidebar Dock
* `sticky` -> Standard Sticky Glassmorphic Header


* **Content Grid Strategy (`grid`)**
* `bento` -> Asymmetric Bento Box Grid
* `split` -> 50/50 Split Screen Workstation
* `center` -> Center-Focused Reading Column
* `dense` -> Dense Multi-panel Dashboard



---

## 3. The Output Prompt Blueprint Structure

The resulting text generated from the data model takes the following strictly formatted structural shape:

```markdown
<system_role>
You are an Elite UI/UX Architect and Staff-level Frontend Developer. Generate a production-ready, highly polished web component adhering strictly to the volumetric design tokens below. Do not hallucinate external assets.
</system_role>

### 1. IDENTITY & PERSONA
- Base Visual Archetype: [Mapped archetype string]
- Flavor Injection: Blend in subtle elements of "[Mapped flavor string]".
- Core Emotional Resonance: [Mapped emotion string]
- Target Audience Profile: [Mapped audience string]
- Typography Strategy: [Mapped typography string]

### 2. COLOR ENGINE & HARMONY
- Palette Root: Primary: [primaryHex] | Secondary/Glow: [secondaryHex]
- Harmony Strategy: [Mapped harmony string]
- Neutral/Grayscale Scale: [Mapped neutrals string]
- Semantic States (Feedback): [Mapped semantics string]
- Accessibility Target: [Mapped contrast string]

> Constraint: Extrapolate opacities and hover states natively using Tailwind arbitrary values based on the exact hex codes provided (e.g., bg-[[primaryHex]]/20).

### 3. MATERIAL PHYSICS & DEPTH ELEVATION
- Dark Mode Surface Root: [Mapped surfaceBase string]
- Surface Material & Textures: [Mapped surfaceMaterial string]
- Shadow & Elevation Paradigm: [Mapped elevation string]
- Border Execution Strategy: [Mapped borders string]

> Constraint: Execute the shadow and border constraints strictly. If "Flat UI" or "Borderless" is requested, rely entirely on padding and background tint shifts for component hierarchy.

### 4. LAYOUT & TECHNICAL SPECS
- Framework: [Mapped framework string]
- Navigational Architecture: [Mapped navigation string]
- Content Grid Strategy: [Mapped grid string]
- Interactivity: Embed realistic client-side mock state logic so the UI is interactive.
- Output: A single-file implementation inside a markdown code block.

```
