---
name: shellui
description: >-
  Use when working on a Shellui project: shellui.config.json, the shellui CLI
  (init, start, build, deploy, login), @shellui/sdk in embedded iframe apps
  (toast, dialog, modal, drawer, auth, storage), app frames (ShelluiFrame,
  createAppFrame), per-app identity servers or regional token exchange, or any
  Shellui PDF, report, deck, one-pager, or other printed or exported document.
  Printed documents start from the brand kit templates and references/print.md.
  Not for generic React or Vite work outside a Shellui shell.
license: MIT
metadata:
  author: shellui
  version: '1.2.0'
  shellui: '>=0.7.0-alpha.5'
---

# Shellui

Host shell (`@shellui/core`, run by `@shellui/cli`) embeds apps in iframes. Nav, themes, auth and overlays live in the shell. Apps talk to it through `@shellui/sdk`.

A Shellui PDF, report, deck, one-pager, or other printed document starts from the matching template in `assets/print/` and follows [references/print.md](references/print.md). The brand kit PDF is the visual reference: https://shellui.com/brand-assets/shellui-brand-kit-v1.pdf.

## Read only what the task needs

| Task                                                          | Read                                                                        |
| ------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Create or run a shell, CLI flags, deploy, login               | [references/cli.md](references/cli.md)                                      |
| Edit `shellui.config.json`, navigation, themes, services      | [references/config.md](references/config.md)                                |
| Overlays, navigation, storage, tiny build in an embedded app  | [references/sdk.md](references/sdk.md)                                      |
| App inside an app, per-app identity server, regional sessions | [references/frames-and-auth.md](references/frames-and-auth.md)              |
| Write user-facing copy (UI strings, docs, emails)             | Fetch https://shellui.com/guidelines/writing.md (`writing-guidelines` skill) |
| Build a page or shell chrome                                  | Fetch https://shellui.com/design.md and https://shellui.com/guidelines/web-design.md (`design-md`, `web-design-guidelines` skills) |
| PDF, report, deck, one-pager, or any printed or exported document | [references/print.md](references/print.md) and the matching file in [assets/print/](assets/print/). Visual reference: https://shellui.com/brand-assets/shellui-brand-kit-v1.pdf |

Fetch guideline `.md` files for copy, UI, or print work. For a PDF, read [references/print.md](references/print.md) before the public summary. Hub: https://shellui.com/guidelines/. API detail: https://docs.shellui.com.

## Hard rules

1. Name: `shellui` (packages, CLI, paths) or `Shellui` (prose). Never `ShellUI`, `shellUI`, `ShellUi`.
2. Embedded apps call `await shellui.init()` before anything else. The shell sends settings only after it.
3. Overlays (toast, dialog, modal, drawer) go through `@shellui/sdk`. No local overlay libs. Tiny has no overlays.
4. Never hand-roll an iframe for a Shellui child app. Use `<ShelluiFrame>` or `createAppFrame`.
5. Origins are exact (`https://admin.example.com`). No `*`, in config or in `postMessage`. Validate incoming `event.origin`.
6. The shell token never reaches a child app. Children get their own session or none.
7. Refresh tokens stay in `sessionStorage`, never `localStorage`, and never go to an app.
8. Config is public. No secrets in `shellui.config.json`. `${VAR}` resolves at CLI load or build only.
9. Do not invent config fields. Keep `$schema` and let validation fail loudly.
10. Any Shellui PDF or printed document starts from the matching template in `assets/print/` and follows `references/print.md`. The brand kit PDF is the visual reference.
