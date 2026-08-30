# Anti-AI Default UI

[![skills.sh](https://skills.sh/b/JaeSang1998/anti-ai-default-ui)](https://skills.sh/JaeSang1998/anti-ai-default-ui)

A strict negative design guardrail for web and app work. It blocks recurring generic AI UI patterns: gradient atmospherics, rounded-card grids, decorative one-sided card borders, HUD and game-console drift, fake status indicators, generic SaaS heroes, and hierarchy that makes everything equally loud.

The repository keeps one canonical instruction file, `SKILL.md`. Codex reads it as a skill. Claude Code reads the identical instructions through the repository’s `CLAUDE.md`, which imports `SKILL.md`.

## Install

The [`skills` CLI](https://github.com/vercel-labs/skills) installs this repository into the skills directory of Claude Code, Codex, Cursor, and other supported agents. `SKILL.md` sits at the repository root with the `name` and `description` frontmatter the CLI requires, so there is nothing else to configure.

```sh
npx skills add JaeSang1998/anti-ai-default-ui
```

That installs into the current project, under `./.claude/skills/anti-ai-default-ui/` for Claude Code, and records the resolved version in `skills-lock.json`. Add `-g` to install for the current user instead, and `-a` to name agents rather than selecting them interactively.

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

## Scope

This is intentionally a prohibition list, not a visual-style recipe. It does not prescribe a replacement aesthetic. A user can explicitly override an individual prohibition.

## License

[MIT](LICENSE)
