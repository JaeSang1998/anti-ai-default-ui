# Anti-AI Default UI

[![skills.sh](https://skills.sh/b/JaeSang1998/anti-ai-default-ui)](https://skills.sh/JaeSang1998/anti-ai-default-ui)

**English** · [한국어](README.ko.md)

A strict negative design guardrail for web and app work: a prohibition list an agent reads before it writes or edits an interface.

Ask two different agents for a pricing page and you tend to get the same page. A gradient behind the header, an eyebrow pill above a centered headline, gray subcopy, three equal cards, a tinted icon tile on every row. These are defaults rather than decisions. They show up whether or not the product needs them, and they survive review because they look finished. This list takes them off the table, so the remaining choices have to come from the product.

The repository keeps one canonical instruction file, `SKILL.md`. Codex reads it as a skill. Claude Code reads the identical instructions through the repository’s `CLAUDE.md`, which imports `SKILL.md`. Nothing is duplicated per agent.

## What it blocks

- **Visual defaults** — blue-to-violet and purple-to-pink gradients, radial glows, ambient blobs, glassmorphism, near-black dark themes with low-opacity white borders.
- **Hero and marketing templates** — the eyebrow pill, oversized headline, gray subcopy, CTA stack; two competing primary calls to action; interchangeable SaaS copy; invented metrics and testimonials.
- **Cards and borders** — three-card feature grids, every statistic and FAQ wrapped in an elevated rounded card, accent borders on a single edge, nested outlines around the same region.
- **Geometry and layout** — one border radius shared by buttons, avatars, modals, and panels; even 8-point spacing applied without regard to content; pages assembled from stacked floating rectangles.
- **Icons and components** — a thin-stroke icon library standing in for visual identity, icons centered in tinted rounded squares, a differently colored tile for each feature.
- **Game and HUD drift** — ordinary software dressed as a command center: glowing status lamps, XP-like meters, crosshairs, all-caps micro-headings, pseudo-military status language.
- **Hierarchy and content** — size differences with no attention hierarchy, muted text that costs readability, color as the only channel for status or validation, and styling done before real copy, data, and empty, loading, and error states exist.
- **Process** — accepting the first generated layout and changing only its colors, using a component library as the product’s identity, adding novelty to avoid looking AI-generated.

`SKILL.md` holds the full list. The bullets above are its categories.

## What it does not do

This is a prohibition list, not a visual-style recipe. It names no replacement palette, type scale, or component library, and it hands you no house style. When removing a pattern leaves a real product question open — which action matters most on this screen, what the data looks like — the skill asks rather than inventing a treatment.

Any single prohibition yields to an explicit request. The list resists defaults, not decisions.

## Install

The [`skills` CLI](https://github.com/vercel-labs/skills) installs this repository into the skills directory of Claude Code, Codex, Cursor, and other supported agents. `SKILL.md` sits at the repository root with the `name` and `description` frontmatter the CLI requires, so there is nothing else to configure.

```sh
npx skills add JaeSang1998/anti-ai-default-ui
```

That installs into the current project, under `./.claude/skills/anti-ai-default-ui/` for Claude Code, and writes a `skills-lock.json` recording the source and a content hash of what was installed. Add `-g` to install for the current user instead, and `-a` to name agents rather than selecting them interactively.

```sh
npx skills add JaeSang1998/anti-ai-default-ui -g -a claude-code -a codex
```

A user-level install writes `~/.claude/skills/anti-ai-default-ui/` and `~/.codex/skills/anti-ai-default-ui/`. Run `npx skills update anti-ai-default-ui` to pull later changes, and `npx skills remove anti-ai-default-ui` to uninstall.

### Manual install for Codex

Copy or symlink this repository directory to your Codex skills directory as `anti-ai-default-ui`, then invoke it with `$anti-ai-default-ui`.

```sh
git clone https://github.com/JaeSang1998/anti-ai-default-ui.git
cp -R anti-ai-default-ui ~/.codex/skills/anti-ai-default-ui
```

### Manual install for Claude Code

Claude Code automatically loads a `CLAUDE.md` file from the project directory. Clone this repository into a project, or import its `SKILL.md` from the project’s or user-level `CLAUDE.md`.

```md
@/absolute/path/to/anti-ai-default-ui/SKILL.md
```

The included `CLAUDE.md` already contains that import, so no duplicate instruction file is maintained.

## How it behaves

**Codex.** Invoke the skill by name with `$anti-ai-default-ui`. `agents/openai.yaml` supplies the display name and the default prompt Codex offers: *Use $anti-ai-default-ui to create or review this interface.*

**Claude Code.** A skills-directory install loads when the work matches the skill description, which is creating or editing an interface. The `CLAUDE.md` import behaves differently: it keeps the rules in context for every turn in that project. Choose the import when you want the list always on.

## Example

The same request to the same agent: *build the pricing page.*

**Without the skill.** A gradient sits behind the header. A rounded "Pricing" pill floats above an oversized centered headline, with gray subcopy beneath it. Three equal cards follow, middle one enlarged, each feature row led by a tinted icon tile, every corner on the page sharing one radius. None of that came from the pricing model. It came from the shape of the request.

**With the skill.** Those moves are unavailable, so the questions they were covering surface instead. Which plan should most people pick, and how does the page show that without a "Most popular" pill? How long is the longest plan name once it is translated? What does the page render while prices load, and when the billing API fails? The agent answers from the product or asks you.

The skill does not supply a replacement design for that page. It removes the defaults and leaves the decisions.

## License

[MIT](LICENSE)
