# Shellui Skills

Official [Agent Skills](https://agentskills.io) for Shellui: config, CLI, SDK and conventions for coding agents.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

Install a skill and your coding agent knows how to build with Shellui: the `shellui.config.json` format, the CLI, the SDK, naming and the house guidelines. The skills stay small and link to [docs.shellui.com](https://docs.shellui.com) and [shellui.com/guidelines](https://shellui.com/guidelines/) for depth. Listed on [skills.sh](https://skills.sh/shellui/skills/shellui).

## Get started

```bash
npx skills add shellui/skills --skill shellui
```

Add `-g` to install it for every project on your machine. Update with `npx skills update`. To install by hand, copy `skills/<name>/` into `.agents/skills/<name>/` or `.cursor/skills/<name>/`.

New to Shellui? Point your agent at [shellui.ai](https://shellui.ai) first.

## Skills

| Skill | What it gives the agent |
| --- | --- |
| [`shellui`](skills/shellui/) | Config, CLI, SDK, frames and auth, naming |
| [`guidelines`](skills/guidelines/) | Index of the [Shellui guidelines](https://shellui.com/guidelines/) |
| [`design-md`](skills/design-md/) | Fetches [design.md](https://shellui.com/design.md) before composing a page |
| [`writing-guidelines`](skills/writing-guidelines/) | Fetches the [writing guide](https://shellui.com/guidelines/writing/) and reviews prose |
| [`web-design-guidelines`](skills/web-design-guidelines/) | Fetches the [web design guide](https://shellui.com/guidelines/web-design/) and reviews UI |

```bash
npx skills add shellui/skills --skill writing-guidelines
```

The guideline skills are thin wrappers. The handbooks live in [shellui/website](https://github.com/shellui/website) under `content/guidelines/`.

## Contributing

- Keep skills small. Prefer bullets and link to the docs for depth.
- Guideline skills fetch public URLs. Do not paste handbook bodies here.
- When the CLI, the SDK or the config changes, update the matching skill and bump its `metadata.version` and `CHANGELOG.md`.
- When a guideline version changes on shellui.com, bump the wrapper `metadata.version` to match.
- Add new skills under `skills/<name>/` with a valid `SKILL.md`, and note catalog changes in [CHANGELOG.md](CHANGELOG.md).

## Shellui projects

| Project | What it does |
| --- | --- |
| [shellui](https://github.com/shellui/shellui) | The shell, CLI and SDK |
| [admin](https://github.com/shellui/admin) | Administration app inside the shell |
| [files](https://github.com/shellui/files) | File explorer for storage-service |
| [identity-service](https://github.com/shellui/identity-service) | Sign-in, companies and tokens |
| [storage-service](https://github.com/shellui/storage-service) | File storage |
| [hosting-service](https://github.com/shellui/hosting-service) | Deploys and serves Shellui apps |
| [email-service](https://github.com/shellui/email-service) | Templates and sends email |
| [skills](https://github.com/shellui/skills) | Agent Skills for coding agents |
| [playground](https://github.com/shellui/playground) | Live demo of the shell |

## License

[MIT](LICENSE)
