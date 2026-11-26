# Changelog

## 1.3.0

- `references/mcp.md` holds the MCP detail. Config, CLI, SDK, and print tasks do not load it
- The only URL is `https://ai.shellui.com/mcp`. Connect only if the person asks or the task needs live Shellui data, and only if the person agrees
- The person signs in and consents. The agent does not complete consent and does not paste or fetch tokens
- Recommend Ask before changes. Do not suggest full access or Allow destructive actions unless the person asks
- Project tools open at Ask. A read only connection stays read only. Destructive project tools need an approval link from an owner
- Setup: https://shellui.com/mcp/ and https://docs.shellui.com/ai/mcp-device-login/#global-mcp-shellui-account

## 1.2.0

- Printed documents start from `assets/print/` and follow `references/print.md`
- `references/print.md` is the agent-readable brand kit (v1, October 2026): type, color, grid, logo, charts, and every section 8 template
- Task table routes a PDF, report, deck, one-pager, or other printed document to that file first. The brand kit PDF stays the visual reference
- Hard rule: start from the matching template

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
