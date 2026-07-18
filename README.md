# AetherPrompt: The UI Prompt Architect

AetherPrompt is a dark-themed, minimalist, single-page developer tool designed to bridge the gap between human design intent and AI code generation. Instead of feeding LLMs generic prompts like *"make a clean dashboard,"* AetherPrompt allows you to visually configure strict design tokens, spatial layouts, and behavioral constraints to instantly compile an instruction-dense **UI Blueprint Prompt**.

Copy the generated blueprint, drop it into your UI engine of choice (v0, Lovable, Claude, or Cursor), and watch it output production-grade, bespoke interfaces that rival custom design agencies.

---

## 🏗️ The Generative UI Pipeline

AetherPrompt fits perfectly at the starting line of your frontend development workflow:

```
┌─────────────────────────┐
│   AetherPrompt UI       │  ◄── Configure aesthetics, grid layouts, 
└───────────┬─────────────┘      and framework design tokens visually.
            │
            ▼ (Click "Copy Blueprint Prompt")
┌─────────────────────────┐
│   UI Blueprint Prompt   │  ◄── A hyper-specific, instruction-dense text block
└───────────┬─────────────┘      enforcing spatial mechanics and strict style tokens.
            │
            ▼ (Paste into Claude / v0 / Lovable / Cursor)
┌─────────────────────────┐
│  High-Fidelity Project  │  ◄── Flawless, modular frontend code matching your 
└─────────────────────────┘      exact architectural guidelines.

```

---

## ⚡ Features

* **Token-Driven Aesthetic Configurations:** Dynamically switch engine behavior between hyper-focused design choices including **Minimalist (Linear-style)**, **Glassmorphism**, **Neo-Brutalist**, and **Cyberpunk Synthwave**.
* **Spatial Grid Strategies:** Force AI models out of standard vertical column stacking by mandating layout paradigms like Asymmetric Bento Grids, Split-Screen Heroes, or Interactive Sidebars.
* **Multi-Framework Tailoring:** Injects framework-specific idiomatic patterns natively into the generated prompt string (e.g., SvelteKit lifecycle + Tailwind vs. React functional TSX + hooks).
* **Zero-Dependency Client-Side Engine:** Runs completely in the browser with vanilla JavaScript and utility-first styling. No databases, no API keys, and no server configuration required.

---

## 🚀 Getting Started

Since AetherPrompt is self-contained into a single interactive file, deploying or running it locally requires zero installation.

### Local Development

1. Clone your generated layout repository or copy the code to an `index.html` file.
2. Spin up a local static server or simply double-click the file to open it in your browser:
```bash
# Using Python
python3 -m http.server 8080

# Or using Node.js
npx serve .

```


3. Open `http://localhost:8080` in your browser.

---

## 🛠️ Configuration Knobs Available

| Category | Input Types | Impact on Blueprint |
| --- | --- | --- |
| **Core Stack** | Dropdown Selector | Modifies code syntax instructions, file structure semantics, and primitive libraries. |
| **Design System** | Preset + Color Picker | Generates strict background, surface alpha values (`bg-slate-900/40`), and border-radius tokens. |
| **Grid Layout** | Dropdown Options | Outlines the DOM rendering layout to enforce advanced layout containers. |
| **Interaction Engine** | Multi-Select Checkboxes | Appends deep micro-interaction directives for hover animations, transition scales, and focus states. |

---

## 📖 Recommended Workflow

1. **Dial it in:** Open AetherPrompt and select your preferred visual parameters, primary framework, and component requirements.
2. **Extract the Prompt:** Click **"Copy Blueprint Prompt"** from the right-hand panel code viewer.
3. **Generate the Shell:** Paste that exact prompt text into a specialized layout generator like **v0** or **Lovable** to build the raw frontend composition.
4. **Refine in Cursor:** Download or copy those components into your IDE, open Cursor's Composer (`⌘ + I`), and instruct the local agent to connect those presentation elements directly to your backend APIs and type systems.
