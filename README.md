# Design System Collection

```
██████╗ ███████╗ ██████╗██╗ ██████╗███╗   ██╗███╗   ███╗██████╗
██╔══██╗██╔════╝██╔════╝██║██╔════╝████╗  ██║████╗ ████║██╔══██╗
██║  ██║█████╗  ███████╗██║██║  ███╗██╔██╗ ██║██╔████╔██║██║  ██║
██║  ██║██╔══╝  ╚════██║██║██║   ██║██║╚██╗██║██║╚██╔╝██║██║  ██║
██████╔╝███████╗██████╔╝██║╚██████╔╝██║ ╚████║██║ ╚═╝ ██║██████╔╝
╚═════╝╚══════╝╚═════╝╚═╝ ╚═════╝╚═╝  ╚═══╝╚═╝     ╚═╝╚═════╝
```

---

## ◆ PULSE

Great products leave behind a grammar of their own - and someone
should transcribe it. This collection holds production-ready design
system documentation inspired by world-class products: Codemod,
Dataforest, JetBrains, Logto, Neon, Node.js, Nuxt, Pnpm, Zed, and El
Patita - each in its own `DESIGN.md`, each following the same
9-section structure, from visual theme to the agent prompt guide. A
Rust CLI named `design-md` keeps the library honest: list, lint
against the structure and WCAG AA contrast, build a static site, and
scaffold the next transcription.

| 10 systems ▣ | 9 sections ▣ | WCAG lint ▣ | Rust CLI ▣ |
|---|---|---|---|

*The library - collect, lint, generate, scaffold - is sealed.*

> Built with Rust 1.80+, maintained with `design-md` - hex codes,
> CSS snippets, token names, and contrast ratios over adjectives.
>
> **suradet-ps**, artifact keeper

---

## ◆ IGNITION

One toolchain, four commands.

```
⟫ cargo run -- list
⟫ cargo run -- lint
⟫ cargo run -- build
⟫ cargo run -- new <name> --source <url>
```

Open `out/index.html` after `build` - a responsive grid with
search and filter, dark and light modes, and a full-text index.

<details>
<summary>CLI reference</summary>

| Command | What it does |
|---|---|
| `design-md list` | Lists every design under `designs/` with source and section count |
| `design-md show <name>` | Summarizes one design system |
| `design-md lint [--fix]` | Validates structure (all 9 sections) and WCAG AA contrast (4.5:1) |
| `design-md build [--out-dir]` | Generates the static HTML site |
| `design-md new <name> --source <url>` | Scaffolds a design from the template |

</details>

---

## ◆ ANATOMY

One structure, one linter, a library that refuses to be decorative.

- **Collects** - every system lives at `designs/<name>/DESIGN.md`,
  each a complete transcription: theme and atmosphere, color roles,
  typography, component stylings, layout, elevation, responsive
  behavior, accessibility states, and the agent prompt guide.
- **Lints** - `design-md lint` checks the facts an implementation
  depends on: all nine sections present, and every color pair at
  WCAG AA (4.5:1) or the spec says so out loud.
- **Generates** - `design-md build` renders a static documentation
  site: responsive grid, per-design pages, dark and light modes, and
  a `search.json` full-text index.
- **Scaffolds** - `design-md new` creates a new system from the
  template with the source URL pre-filled - transcribing a product
  starts with the form, not the blank page.
- **Guards** - the contribution rules are explicit: English, hex
  codes, CSS snippets, token names, both modes, contrast references -
  and no subjective language. Measurable specs only.

---

## ◆ RITUALS

**The core ceremony** - transcribing a new design system:

1. `design-md new <name> --source <url>` - the scaffold appears with
   its source and its nine sections.
2. Fill the sections with implementation-ready content: tokens,
   snippets, ratios - what a developer can build from, not what they
   must interpret.
3. `design-md lint` - the structure and contrast checks answer; a
   failing pair is a failing spec.
4. `design-md build` - the site renders; the system joins the
   library.

**The ceremony of the measurable** - no "beautiful", no "elegant":
the collection accepts hex codes, CSS snippets, token names, and
contrast ratios. A spec that cannot be verified is a sketch.

**The ceremony of the nine sections** - every system speaks the same
grammar, from theme to agent prompts. A developer who has read one
can navigate any: the structure is the interface.

---

## ◆ ECHOES

**Where this artifact is heading**

```
collect ▸ 10 design systems, one 9-section structure ────────────────── ▸ sealed
lint    ▸ structure + WCAG AA validation ────────────────────────────── ▸ sealed
build   ▸ static site, search, dark/light ───────────────────────────── ▸ sealed
scaffold ▸ template-driven new designs ──────────────────────────────── ▸ sealed
```

**Raising the artifact** - the CLI lives in `src/`; the systems in
`designs/`; the template in `template/`. Propose a new design via an
issue with the product name and URL; discuss ideas in Discussions.
Open an issue first to discuss a change.

**Status** - the collection is active and growing.

---

```
  ─────────────────────────────────────────
   A design without a spec is a mood.
   A spec without a ratio is a hope.
  ─────────────────────────────────────────
```

Licensed under the [MIT License](LICENSE).