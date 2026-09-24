# GitHub Refs — reusable UI / motion / design libraries

A personal catalog of external libraries, component collections, and agent skills to pull from across projects. Curated by Cliff.

Each entry: **what it is**, **best used for**, and **how to pull it in**.

> Note on "skills": some of these ship as installable **agent skills** (Cursor/Claude Code), some are **npm/CLI component libraries**, and a couple are **browse-and-copy component sites**. The type is labelled per entry.

Last updated: 2026-09-24

---

## 1. Transitions & Motion

### transitions.dev
- **Link:** https://github.com/Jakubantalik/transitions.dev
- **Type:** CSS snippets + CLI + agent skill
- **What it is:** An interactive collection of ~18 production-ready CSS transitions (card resize, number pop-ins, modal open/close, page transitions, etc.). Self-contained CSS with semantic custom properties and `prefers-reduced-motion` support.
- **Best used for:** Dropping polished, tokenized motion into any web UI without hand-rolling keyframes. The "Refine" panel lets an agent suggest/apply transitions to a running app.
- **How to pull in:** `npx transitions-dev add [name]`, or install as an agent skill. (Already installed globally as the `transitions-dev` + `transitions-polish` skills.)

### shadcn-animated
- **Link:** https://github.com/sopo/shadcn-animated
- **Type:** Component library (React/TS)
- **What it is:** Animated versions of shadcn/ui components. Drop-in replacements built with Framer Motion + Tailwind + TypeScript.
- **Best used for:** Projects already on shadcn/ui that want polished animation without swapping design systems.
- **How to pull in:** npm install / component docs site (drop-in per component).

---

## 2. UI Component Libraries

### React Bits
- **Link:** https://github.com/DavidHDev/react-bits
- **Type:** Component library (copy-paste, 48k+ stars)
- **What it is:** 200+ free, customizable animations for text, backgrounds, UI, and micro-interactions. Four variants per component (JS-CSS, JS-Tailwind, TS-CSS, TS-Tailwind). Includes creative tools (Background Studio, Shape Magic, Texture Lab). Minimal-dependency, tree-shakeable. Vue + Svelte ports exist.
- **Best used for:** **Landing pages and marketing surfaces** — flashy text/background effects. Heavier WebGL/three.js/GSAP components are overkill for internal tools/CRMs.
- **How to pull in:** Copy-paste, or via shadcn / jsrepo CLI.

### Kobra
- **Link:** https://kobra.systems/
- **Type:** Component library site (React)
- **What it is:** 50+ reusable React components (form controls, navigation, overlays, feedback) plus agent-focused pieces like chat interfaces and code blocks. Styled layer built on top of open-source primitives (input-otp, shadcn). Free tier + Pro.
- **Best used for:** Production React apps needing accessible, animated, ready-made components — including AI/agent chat UIs.
- **How to pull in:** Browse site, copy components (some Pro-gated).

### Beautiful UI
- **Link:** https://www.beautifului.dev/
- **Type:** Component library site (copy-paste)
- **What it is:** 20+ primitives built specifically for **AI-native interfaces** — loading/thinking traces, streaming text, approval cards, chat composer, prompt bar, task rows, recommendation cards, flowcharts, diff displays. Made by Turbo (design studio).
- **Best used for:** Building agent/LLM app surfaces (like Rex, OnIt, Lens chat views) where you need purpose-built AI interaction components.
- **How to pull in:** Copy-paste ready from the site.

### loading-dev
- **Link:** https://github.com/jakubkrehel/loading
- **Type:** Component library (React 19+)
- **What it is:** 28+ animated loading indicators/spinners (Arc, Atom, Blocks, Wave, Orbit, etc.). Customizable size/color/duration, `playState` control, respects reduced motion. MIT. Requires React 19+.
- **Best used for:** Consistent, accessible loading states across React apps. Live previews at loading.dev.
- **How to pull in:** `npm install loading-dev`.

---

## 3. Design & UI Agent Skills

### emilkowalski/skills
- **Link:** https://github.com/emilkowalski/skills
- **Type:** Agent skill collection (Cursor/Claude)
- **What it is:** 11+ specialized skills encoding UI/design "taste" for agents — animation creation & review, Apple WWDC design principles, UI library selection, Swift, mobile-native web optimization, Sonner toast integration. Premise: "Agents don't have great taste" — these prevent common easing/design mistakes.
- **Best used for:** Giving coding agents production-quality UI judgment. (The `animate` / `animate-expo` / `mobile-native` skills in this stack are already installed globally.)
- **How to pull in:** `npx skills@latest add emilkowalski/skills`.

---

## 4. Anti-AI-Slop (writing + design)

### no-ai-slop
- **Link:** https://github.com/petergyang/no-ai-slop
- **Type:** Agent skill (ChatGPT / Claude Code)
- **Slop type:** Writing / copy
- **What it is:** Detects and removes 20+ AI writing patterns ("It's not X. It's Y.", "What nobody tells you is…", weasel attribution, corporate jargon) while preserving authentic voice. Edit mode, detect-only mode, and a satire generator. 24 distinct slop categories.
- **Best used for:** Cleaning AI-assisted copy — decks, brochures, UI microcopy, emails — so it reads human. Pairs with the `stop-slop` / `no-ai-slop` writing skills.
- **How to pull in:** `npx` install as a ChatGPT/Claude Code skill.

### open-design — anti-ai-slop.md
- **Link:** https://github.com/nexu-io/open-design/blob/main/craft/anti-ai-slop.md
- **Type:** Design-standards doc (from `nexu-io/open-design`, 97.9k stars)
- **Slop type:** Visual / UI design
- **What it is:** A tiered, enforceable checklist for making UI look human-crafted, not template-AI. **P0 Cardinal Sins** (no default Tailwind indigo, no gradient hero, SVG icons not emoji, design-system fonts, no "AI dashboard tile" patterns, no unverified metrics, no filler copy), **P1 Soft Tells** (vary the Hero→Features→Pricing order, no placeholder-image CDNs, limit raw hex, cap accent usage), **P2 Polish Tells**. Guiding principle: ~80% proven patterns + ~20% distinctive choice.
- **Best used for:** A pre-ship rubric for any landing page / dashboard UI to strip visual AI-slop. Complements the installed `unslop-ui` / `no-ai-slop` skills. Parent repo `nexu-io/open-design` is worth browsing as a broader design-standards reference.
- **How to pull in:** Read the doc as a checklist, or feed it to an agent as design rules.

---

## 5. Skill Directories / Discovery

### awesome-claude-skills
- **Link:** https://github.com/travisvn/awesome-claude-skills
- **Type:** Curated awesome-list (meta-resource)
- **What it is:** A curated directory of Claude skills — official Anthropic skills (docs, design, dev, comms), community skills (browser automation, security testing, iOS, etc.), creation guides, best practices, and guidance on when to use Skills vs MCP / prompts / subagents.
- **Best used for:** Discovering new skills to install, and as a reference when building custom skills. Check here first when hunting for a skill that solves a recurring task.
- **How to pull in:** Browse the list; install linked skills per their own instructions.

---

## Quick pick guide

| Need | Reach for |
|------|-----------|
| Tokenized CSS transitions | transitions.dev |
| Animated shadcn components | shadcn-animated |
| Landing-page eye candy | React Bits |
| General React components (incl. chat UI) | Kobra |
| AI-app interface primitives | Beautiful UI |
| Loading spinners | loading-dev |
| Give an agent UI taste | emilkowalski/skills |
| De-slop AI writing | no-ai-slop |
| De-slop AI visual/UI design | open-design — anti-ai-slop.md |
| Discover more Claude skills | awesome-claude-skills |
