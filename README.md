# shellui skills

Official [Agent Skills](https://agentskills.io) for [Shellui](https://github.com/shellui/shellui) and related apps.

## Guidelines

Voice, UI, and composition for Shellui sites and in-shell surfaces live on the public hub:

**https://shellui.com/guidelines/**

This catalog ships thin skills that tell agents to **fetch** the published markdown (same pattern as Vercel’s writing / web-interface guideline skills). Long-form handbooks are not duplicated here.

| Skill | Fetch | Human page |
| ----- | ----- | ---------- |
| [`guidelines`](skills/guidelines/) | parent index | [Hub](https://shellui.com/guidelines/) |
| [`design-md`](skills/design-md/) | https://shellui.com/design.md | [Design handbook](https://shellui.com/guidelines/design/) (visual; agents use `/design.md` only) |
| [`writing-guidelines`](skills/writing-guidelines/) | https://shellui.com/guidelines/writing.md | [Writing](https://shellui.com/guidelines/writing/) |
| [`web-design-guidelines`](skills/web-design-guidelines/) | https://shellui.com/guidelines/web-design.md | [Web design](https://shellui.com/guidelines/web-design/) |

Source of truth for the handbooks: [shellui/website](https://github.com/shellui/website) (`content/guidelines/`). Skills under that repo’s `skills/` match these wrappers for local website work.

## Install

```bash
# Product / CLI / SDK (config, overlays, naming)
npx skills add shellui/skills --skill shellui

# Guidelines (fetch shellui.com markdown)
npx skills add shellui/skills --skill guidelines
npx skills add shellui/skills --skill design-md
npx skills add shellui/skills --skill writing-guidelines
npx skills add shellui/skills --skill web-design-guidelines

# Or globally across all your projects
npx skills add shellui/skills --skill shellui -g
```

Update:

```bash
npx skills update
```

Manual copy: put `skills/<name>/` into `.agents/skills/<name>/` or `.cursor/skills/<name>/`.

## Skills

| Skill | Description |
| ----- | ----------- |
| [`shellui`](skills/shellui/) | Config, CLI, SDK vs tiny, naming, overlays |
| [`guidelines`](skills/guidelines/) | Parent index → https://shellui.com/guidelines/ |
| [`design-md`](skills/design-md/) | Fetch https://shellui.com/design.md first when composing pages |
| [`writing-guidelines`](skills/writing-guidelines/) | Fetch writing handbook; review prose |
| [`web-design-guidelines`](skills/web-design-guidelines/) | Fetch web design handbook; review UI / a11y / chrome |

## Contributing

- Keep skills small (token budget). Prefer bullets; link https://docs.shellui.com for product depth and https://shellui.com/guidelines/ for voice/UI/composition.
- Guideline skills must stay thin wrappers that fetch public URLs. Do not paste handbook bodies into this repo.
- When Shellui CLI/SDK/config breaks, update the matching skill and bump `metadata.version` + that skill’s `CHANGELOG.md`.
- When public guideline versions change on shellui.com, bump the matching wrapper `metadata.version` to match the published frontmatter `version`.
- Note catalog-level changes in [CHANGELOG.md](CHANGELOG.md).
- Add new skills under `skills/<name>/` with a valid `SKILL.md`.

## License

MIT
