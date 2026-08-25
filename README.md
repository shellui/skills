# shellui skills

Official [Agent Skills](https://agentskills.io) for [Shellui](https://github.com/shellui/shellui) and related apps.

## Install

```bash
# Project (recommended for shared repos)
npx skills add shellui/skills --skill shellui

# Or globally across all your projects
npx skills add shellui/skills --skill shellui -g
```

Update:

```bash
npx skills update
```

Manual copy: put `skills/shellui/` into `.agents/skills/shellui/` or `.cursor/skills/shellui/`.

## Skills

| Skill | Description |
| ----- | ----------- |
| [`shellui`](skills/shellui/) | Config, CLI, SDK vs tiny, naming, overlays |

## Contributing

- Keep skills small (token budget). Prefer bullets; link https://docs.shellui.com for depth.
- When Shellui CLI/SDK/config breaks, update the matching skill and bump `metadata.version` + that skill’s `CHANGELOG.md`.
- Add new skills under `skills/<name>/` with a valid `SKILL.md`.

## License

MIT
