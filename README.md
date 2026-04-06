<div align="center">

# PixelPilot

### Stop AI Slop. Start Shipping Unique UI.

[![GitHub stars](https://img.shields.io/github/stars/dev-lou/pixelpilot?style=flat&logo=github&color=yellow)](https://github.com/dev-lou/pixelpilot/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/dev-lou/pixelpilot?style=flat&logo=github)](https://github.com/dev-lou/pixelpilot/network/members)
[![Version](https://img.shields.io/badge/version-11.2-blue.svg)](CHANGELOG.md)
[![Rules](https://img.shields.io/badge/rules-91+-green.svg)](#rules-list)
[![License](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)

[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink?logo=github-sponsors)](https://github.com/sponsors/dev-lou)

**91+ rules that force AI to write original, production-ready frontend code.**

No more generic templates. No more copy-paste UI. No more AI slop.

Cursor | VS Code | Windsurf | OpenCode | Zed

[Quick Start](#quick-start) | [Features](#features) | [Rules List](#rules-list) | [Sponsor](#support-the-project)

</div>

---

## The Problem

AI coding assistants generate **the same boring UI** every time:
- Generic hero sections
- Copy-paste Bootstrap layouts
- No personality, no craft
- Looks like every other AI-generated site

## The Solution

PixelPilot trains your AI to write **unique, opinionated, professional UI** by enforcing:

- **7 distinct design languages** - Not one generic style, but Luxury, Minimalist, Editorial, and more
- **10 component states** - Every button handles loading, error, success, not just default
- **20 non-negotiable laws** - No `transition: all`, no native selects, no grey placeholders
- **Real design decisions** - Mixed image shapes, proper spacing scales, dark mode by default

> **One-time setup. AI that actually designs.**

---

## Supported Editors

| Editor | Status | Config Location |
|--------|--------|-----------------|
| <img src="https://cursor.sh/favicon.ico" width="16"/> **Cursor** | Full Support | `.cursorrules` + `.cursor/rules/` |
| <img src="https://code.visualstudio.com/favicon.ico" width="16"/> **VS Code (Copilot)** | Full Support | `.github/copilot-instructions.md` |
| <img src="https://codeium.com/favicon.svg" width="16"/> **Windsurf** | Full Support | `.windsurf/rules/` |
| <img src="https://opencode.ai/favicon.ico" width="16"/> **OpenCode** | Full Support | `AGENTS.md` + `.opencode/rules/` |
| <img src="https://zed.dev/favicon.ico" width="16"/> **Zed** | Full Support | `.rules` |

---

## Quick Start

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/pixelpilot.git
cd pixelpilot
```

### Step 2: Copy Rules to Your Project

<details>
<summary><b>Cursor</b></summary>

```bash
# Navigate to your project
cd /path/to/your-project

# Copy the Cursor rules
cp /path/to/pixelpilot/cursor/.cursorrules ./
cp -r /path/to/pixelpilot/cursor/.cursor ./
```

**Result:**
```
your-project/
├── .cursorrules          # Main rules file
└── .cursor/
    └── rules/            # 91 detailed rule files
        ├── uiux-a11y.md
        ├── uiux-components.md
        ├── uiux-tokens.md
        └── ...
```

</details>

<details>
<summary><b>VS Code (GitHub Copilot)</b></summary>

```bash
# Navigate to your project
cd /path/to/your-project

# Copy the Copilot instructions
cp -r /path/to/pixelpilot/vscode/.github ./
```

**Result:**
```
your-project/
└── .github/
    ├── copilot-instructions.md    # Main instructions
    └── instructions/              # 91 detailed instruction files
        ├── uiux-a11y.instructions.md
        ├── uiux-components.instructions.md
        └── ...
```

</details>

<details>
<summary><b>Windsurf</b></summary>

```bash
# Navigate to your project
cd /path/to/your-project

# Copy the Windsurf rules
cp -r /path/to/pixelpilot/windsurf/.windsurf ./
```

**Result:**
```
your-project/
└── .windsurf/
    └── rules/            # 91+ rule files with frontmatter triggers
        ├── uiux-main.md
        ├── uiux-a11y.md
        └── ...
```

</details>

<details>
<summary><b>OpenCode</b></summary>

```bash
# Navigate to your project
cd /path/to/your-project

# Copy the OpenCode rules
cp /path/to/pixelpilot/opencode/AGENTS.md ./
cp -r /path/to/pixelpilot/opencode/.opencode ./
```

**Result:**
```
your-project/
├── AGENTS.md             # Main agent instructions
└── .opencode/
    └── rules/            # 91 detailed rule files
        ├── uiux-a11y.md
        └── ...
```

</details>

<details>
<summary><b>Zed</b></summary>

```bash
# Navigate to your project
cd /path/to/your-project

# Copy the Zed rules
cp /path/to/pixelpilot/zed/.rules ./
```

**Result:**
```
your-project/
└── .rules                # Combined rules file
```

</details>

### Step 3: Start Coding

That's it! Your AI assistant now follows professional UI/UX standards automatically.

---

## Features

### 20 Non-Negotiable Laws

These rules are **always enforced** by your AI assistant:

| # | Law |
|---|-----|
| 1 | Classify design language FIRST — before any code |
| 2 | Brand tokens in `:root` once — never override per-page or inline |
| 3 | Never `window.alert/confirm/prompt` — SweetAlert2 or custom toast only |
| 4 | No grey placeholder boxes — Picsum/Unsplash URLs, context-matched |
| 5 | No `localhost` in any user-visible text or URL |
| 6 | Dark + light mode on every project — `[data-theme]` on `<html>` |
| 7 | Mobile-first always — design at 390px, expand outward |
| 8 | `transition: all` NEVER — specify only changed properties |
| 9 | Every `<img>`: width, height, loading, alt — no exceptions |
| 10 | Every async state has a skeleton — never blank |
| 11 | `prefers-reduced-motion` respected in all animations |
| 12 | Only animate `transform` and `opacity` (GPU S-Tier) |
| 13 | Every interactive component handles all 10 states |
| 14 | Never native `<select>`, native date input — always custom |
| 15 | Image grids mix shapes — never all-square |
| 16 | Min contrast: 4.5:1 body, 3:1 large text |
| 17 | Every page has a footer with `role="contentinfo"` |
| 18 | All spacing on the 8px scale — 4,8,12,16,24,32,48,64,80,96,120,160px |
| 19 | Every empty data state shows an empty-state component |
| 20 | Images: `<picture>` + AVIF source + WebP fallback |

### 10 Component States

Every interactive component is built to handle all possible states:

```
default → hover → focus → active → loading → disabled → error → success → empty → busy
```

### 7 Design Languages

Choose the visual language that matches your project:

| Language | Best For | Key Characteristics |
|----------|----------|---------------------|
| **Luxury** | Fashion, hotels, jewelry, art galleries | Slow animations, generous whitespace, sharp typography |
| **Premium Modern** | SaaS, fintech, B2B, productivity apps | Polished surfaces, confident colors, clean hierarchy |
| **Minimalist** | Portfolios, studios, agencies | Silent aesthetics, precise alignments, hidden complexity |
| **Expressive** | Gaming, music, events, youth brands | Bold colors, energetic motion, playful interactions |
| **Editorial** | News, blogs, magazines, documentation | Typography-first, optimal reading experience |
| **Warm & Human** | Health, education, NGO, consumer apps | Rounded shapes, friendly colors, approachable feel |
| **Technical** | Dashboards, dev tools, admin panels | Dense information, zero decoration, maximum utility |

---

## Rules List

<details>
<summary><b>View all 91 rule files</b></summary>

### Core Rules
| File | Description |
|------|-------------|
| `uiux-tokens.md` | Design tokens, CSS custom properties, color systems |
| `uiux-components.md` | Component architecture, atomic design |
| `uiux-a11y.md` | Accessibility requirements, WCAG compliance |
| `uiux-forms.md` | Form design, validation, error handling |
| `uiux-motion.md` | Animation principles, transitions, micro-interactions |
| `uiux-states.md` | Component states, loading, error, empty states |
| `uiux-performance.md` | Core Web Vitals, optimization techniques |
| `uiux-layouts.md` | Grid systems, responsive design, breakpoints |

### Advanced Rules
| File | Description |
|------|-------------|
| `uiux-ai-frontend.md` | AI/ML integration patterns |
| `uiux-voice-ui.md` | Voice interface design |
| `uiux-spatial-ui.md` | 3D and spatial interfaces |
| `uiux-webxr.md` | WebXR/VR/AR experiences |
| `uiux-biometric-auth.md` | Biometric authentication UX |
| `uiux-ambient-awareness.md` | Context-aware interfaces |
| `uiux-temporal-ui.md` | Time-based UI patterns |

### Specialized Rules
| File | Description |
|------|-------------|
| `uiux-data-table.md` | Data tables, sorting, filtering |
| `uiux-admin-dashboard.md` | Admin panel patterns |
| `uiux-seo.md` | SEO optimization |
| `uiux-i18n.md` | Internationalization |
| `uiux-pwa.md` | Progressive Web Apps |
| `uiux-offline-pwa.md` | Offline-first strategies |
| `uiux-realtime.md` | Real-time features |

### Framework-Specific
| File | Description |
|------|-------------|
| `uiux-laravel.md` | Laravel integration |
| `uiux-flutter.md` | Flutter patterns |
| `uiux-graphql.md` | GraphQL best practices |
| `uiux-edge.md` | Edge computing UI |
| `uiux-monorepo.md` | Monorepo architecture |

### Quality & Testing
| File | Description |
|------|-------------|
| `uiux-testing.md` | UI testing strategies |
| `uiux-a11y-ci.md` | Accessibility in CI/CD |
| `uiux-performance-ci.md` | Performance testing |
| `uiux-audit-automation.md` | Automated audits |
| `reasoning.md` | AI reasoning patterns |

*...and 50+ more specialized rules*

</details>

---

## Repository Structure

```
pixelpilot/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
│
├── cursor/                      # Cursor AI rules
│   ├── .cursorrules
│   └── .cursor/
│       └── rules/
│
├── vscode/                      # VS Code / GitHub Copilot
│   └── .github/
│       ├── copilot-instructions.md
│       └── instructions/
│
├── windsurf/                    # Windsurf / Codeium
│   └── .windsurf/
│       └── rules/
│
├── opencode/                    # OpenCode
│   ├── AGENTS.md
│   └── .opencode/
│       └── rules/
│
└── zed/                         # Zed Editor
    └── .rules
```

---

## FAQ

<details>
<summary><b>Do I need all the rule files?</b></summary>

No! The main config file (`.cursorrules`, `copilot-instructions.md`, etc.) contains the essential rules. The additional rule files in the `rules/` folder are loaded on-demand based on context. Keep all files for the best experience, but the system works with just the main file.

</details>

<details>
<summary><b>Will this slow down my AI assistant?</b></summary>

No. Rule files are read on-demand and cached. The impact on response time is negligible.

</details>

<details>
<summary><b>Can I customize the rules?</b></summary>

Absolutely! All rules are in Markdown format. Edit any file to match your team's standards. Consider forking the repo to maintain your customizations.

</details>

<details>
<summary><b>How do I update to new versions?</b></summary>

Pull the latest changes and re-copy the files to your projects:
```bash
cd pixelpilot
git pull origin main
# Then copy to your projects again
```

</details>

<details>
<summary><b>What if my editor isn't listed?</b></summary>

Most AI coding assistants support some form of custom instructions. Check your editor's documentation for "custom rules", "system prompts", or "instructions" features. The rule content is portable — only the file location differs.

</details>

---

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Ways to contribute:**
- Add new rule files for emerging patterns
- Improve existing rules with better examples
- Add support for additional editors
- Fix typos and improve documentation
- Share your customizations

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history and updates.

---

## Support the Project

If PixelPilot helps you build better UIs, consider supporting its development:

<a href="https://github.com/sponsors/dev-lou">
  <img src="https://img.shields.io/badge/Sponsor_on_GitHub-%E2%9D%A4-pink?style=for-the-badge&logo=github-sponsors" alt="Sponsor on GitHub">
</a>

Your support helps:
- Maintain and update rule files
- Add support for new editors
- Create video tutorials and documentation
- Keep the project free and open source

---

## License

MIT License - see [LICENSE](LICENSE) for details.

---

<div align="center">

**Created by Lou Vincent Baroro**

[Report Bug](https://github.com/dev-lou/pixelpilot/issues) | [Request Feature](https://github.com/dev-lou/pixelpilot/issues) | [Star on GitHub](https://github.com/dev-lou/pixelpilot)

</div>
