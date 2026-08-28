# Anti-AI Default UI

A strict negative design guardrail for web and app work. It blocks recurring generic AI UI patterns: gradient atmospherics, rounded-card grids, decorative one-sided card borders, HUD and game-console drift, fake status indicators, generic SaaS heroes, and hierarchy that makes everything equally loud.

The repository keeps one canonical instruction file, `SKILL.md`. Codex reads it as a skill. Claude Code reads the identical instructions through the repository’s `CLAUDE.md`, which imports `SKILL.md`.

## Use with Codex

Copy or symlink this repository directory to your Codex skills directory as `anti-ai-default-ui`, then invoke it with `$anti-ai-default-ui`.

```sh
git clone https://github.com/JaeSang1998/anti-ai-default-ui.git
cp -R anti-ai-default-ui ~/.codex/skills/anti-ai-default-ui
```

## Use with Claude Code

Claude Code automatically loads a `CLAUDE.md` file from the project directory. Clone this repository into a project, or import its `SKILL.md` from the project’s or user-level `CLAUDE.md`.

```md
@/absolute/path/to/anti-ai-default-ui/SKILL.md
```

The included `CLAUDE.md` already contains that import, so no duplicate instruction file is maintained.

## Scope

This is intentionally a prohibition list, not a visual-style recipe. It does not prescribe a replacement aesthetic. A user can explicitly override an individual prohibition.

## License

[MIT](LICENSE)
