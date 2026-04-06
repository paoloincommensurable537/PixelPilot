# Changelog

All notable changes to **PixelPilot** are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [11.2.0] - 2026-04-07

### Added
- Multi-editor support with dedicated folders:
  - `cursor/` - Cursor AI with `.cursorrules` + `.cursor/rules/`
  - `vscode/` - VS Code/GitHub Copilot with `.github/copilot-instructions.md`
  - `windsurf/` - Windsurf with `.windsurf/rules/` and frontmatter triggers
  - `opencode/` - OpenCode with `AGENTS.md` + `.opencode/rules/`
  - `zed/` - Zed Editor with `.rules` file
- Professional README with collapsible quick-start guides
- FAQ section with common questions
- Editor icons and badges

### Changed
- **Renamed project to PixelPilot** (formerly UI/UX 2026 Design System)
- Restructured repository for better organization
- Simplified folder names (`cursor/` instead of `uiux2026-cursor/`)
- Updated all documentation to reflect new branding

---

## [11.1.1] - 2026-04-07

### Changed
- Reorganized repository structure for better organization
- Renamed `shared-rules/` to `rules/` for cleaner naming
- Created agent-specific folders with proper configurations
- Created comprehensive root `README.md` with full documentation

### Added
- Per-agent setup instructions in each folder
- Quick setup commands for each agent type

---

## [11.1.0] - 2026-04-06

### Added
- `uiux-performance-budget.md` - Performance budgeting guidelines
- `uiux-cognitive-load.md` - Cognitive load management
- `uiux-real-user-monitoring.md` - RUM implementation patterns
- GitHub-ready repository packaging

### Changed
- Updated rule indexing to reflect 91+ total rules

---

## [11.0.0] - 2026-04-06

### Added
- 13 advanced UX skill files:
  - `uiux-spatial-ui.md` - WebGPU, Three.js, 3D product viewers
  - `uiux-voice-ui.md` - Web Speech API, voice commands
  - `uiux-sound-design.md` - UI sound cues, data sonification
  - `uiux-ambient-awareness.md` - Battery-aware, light sensor, network-adaptive
  - `uiux-temporal-ui.md` - Time-of-day themes, deadline urgency
  - `uiux-progressive-disclosure.md` - Info architecture, expert mode
  - `uiux-easter-eggs.md` - Konami codes, achievements
  - `uiux-loading-storytelling.md` - Progress narratives, skeleton theatre
  - `uiux-microcopy.md` - Error messages, empty states, CTAs
  - `uiux-anti-dark-patterns.md` - Ethical UI, trust signals
  - `uiux-trust-signals.md` - Security badges, verification
  - `uiux-webxr.md` - AR try-on, VR experiences
  - `uiux-biometric-auth.md` - WebAuthn/passkeys

---

## [10.0.0] - 2025-10-15

### Added
- Critical Rule: Custom components for all native browser UI
- Design language classification (7 languages)
- 10 component states (including "Busy" state)

---

## [9.0.0] - 2025-08-20

### Added
- Design token system (3-tier DTCG)
- Mobile-first methodology (390px base)
- 20 Non-Negotiable Laws

---

## [8.0.0] - 2025-06-10

### Added
- Core rule files for tokens, components, accessibility
- Initial forms and motion guidelines
- Performance optimization rules

---

For detailed rule-specific changes, see `cursor/.cursor/rules/uiux-changelog.md`.
