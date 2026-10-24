# Changelog

## 1.1.0

- Task table routes to one reference file, guideline handbooks fetched only for copy or UI work
- New `references/frames-and-auth.md`: `ShelluiFrame`, `createAppFrame`, `childFrames`, per-app `backend`, token exchange
- Hard rules: `init` first, no hand-rolled child iframes, exact origins, no shell token to children, refresh tokens in `sessionStorage`
- SDK: `useShelluiNavigation` from `@shellui/sdk/react`
- CLI: `deploy`, `login`, `logout`, `whoami`
- Config: per-app services, `auth.desktopScheme`, `email`, `ai.enabled`
- Targets Shellui `>=0.7.0-alpha.5`, no em or en dashes

## 1.0.2

- Cross-link to https://shellui.com/guidelines/ via the catalog `guidelines` skill

## 1.0.1

- CLI isolation: ignore consumer Vite / PostCSS / tsconfig / `VITE_*`; cache `.vite-shellui`

## 1.0.0

- Initial official shellui Agent Skill
- Hard rules: product naming (`shellui` / `Shellui`), SDK for overlays, public config
- Lean references for config, CLI, and SDK vs tiny
