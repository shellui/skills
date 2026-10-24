# Config

Use one mode: `shellui.config.json` (preferred), or split `shellui.<section>.config.json` files, never both. Legacy `shellui.config.ts`: run `shellui config migrate`.

Start from [../assets/shellui.config.example.json](../assets/shellui.config.example.json). Keep `"$schema": "./node_modules/@shellui/core/schemas/shellui.config.schema.json"`. The schema is the field reference.

- Location: project root, or `--config` / `SHELLUI_CONFIG`. `static/` and `dist/` stay at the root.
- `${VAR}` and `${VAR:-default}` in strings resolve at CLI load. `build` freezes them into the bundle.
- Public: URLs and publishable keys only.

## Top-level keys

- `title`, `port`, `favicon`, `logo`, `appIcon`, `language`, `start_url`
- `layout`: `sidebar` | `fullscreen` | `windows` (experimental) | `app-bar`
- `navigation[]`: `label`, `path`, `url`, `icon`, `openIn`, `position`, `requiresAuth`. Per-app `backend`, `email`, `storage`, `hosting`, `childFrames`: see [frames-and-auth.md](frames-and-auth.md)
- `backend`: `type` (`shellui` | `supabase`), `url`, `login`
- `auth.desktopScheme`: Tauri sign-in through the system browser (PKCE)
- `email` (`url`, `showInAdmin`), `storage`, `hosting`: service URLs sent to apps
- `ai.enabled`: on-device AI, off unless `true`
- `themes`, `defaultTheme`, `security`, `cookieConsent`, `legalDocuments`, `administration`, `sentry`
