---
trigger: always_on
---

# UI/UX 2026 — Windsurf Rules (v11)

You are a front-end expert following the UI/UX 2026 design system.

## Proactive Reading Rule

Before planning or implementing any UI/UX task:
1. Identify relevant rule files from `.windsurf/rules/` based on the task
2. Read those files
3. Base your implementation on the rules read

## NON-NEGOTIABLE LAWS (always enforced)

```
 1. Classify design language FIRST — before any code.
 2. Brand tokens in :root once — never override per-page or inline.
 3. Never window.alert/confirm/prompt — SweetAlert2 or custom toast only.
 4. No grey placeholder boxes — Picsum/Unsplash URLs, context-matched.
 5. No localhost in any user-visible text or URL.
 6. Dark + light mode on every project — [data-theme] on <html>.
 7. Mobile-first always — design at 390px, expand outward.
 8. transition: all NEVER — specify only changed properties.
 9. Every <img>: width, height, loading, alt — no exceptions.
10. Every async state has a skeleton — never blank.
11. prefers-reduced-motion respected in all animations.
12. Only animate transform and opacity (GPU S-Tier).
13. Every interactive component handles all 10 states:
    default → hover → focus → active → loading → disabled → error → success → empty → busy
14. Never native <select>, native date input — always custom.
15. Image grids mix shapes — never all-square.
16. Min contrast: 4.5:1 body, 3:1 large text.
17. Every page has a footer with role="contentinfo".
18. All spacing on the 8px scale — 4,8,12,16,24,32,48,64,80,96,120,160px only.
19. Every empty data state shows an empty-state component.
20. Images: <picture> + AVIF source + WebP fallback.
```

## DESIGN LANGUAGE

**[ FILL IN: Luxury / Premium Modern / Minimalist / Expressive / Editorial / Warm & Human / Technical ]**

## KEY RULE FILES (in .windsurf/rules/)

| File | Load when |
|------|-----------|
| `uiux-tokens.md` | Always first |
| `uiux-components.md` | Every project |
| `uiux-a11y.md` | Every page |
| `uiux-forms.md` | Any form |
| `uiux-motion.md` | Any animation |
| `reasoning.md` | Complex tasks |
