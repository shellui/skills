# CLI

`npm i -D @shellui/cli` (bin `shellui`, Node >= 18).

| Command                                    | Purpose                                         |
| ------------------------------------------ | ----------------------------------------------- |
| `shellui init [root]`                      | Create `shellui.config.json` (`--force`)        |
| `shellui start` (alias `dev`)              | Dev server. Auto-inits if no config             |
| `shellui build`                            | Production build to `dist/`                     |
| `shellui deploy`                           | Deploy the build. Warns on missing redirect URL |
| `shellui login` / `logout` / `whoami`      | PKCE sign-in. Token in OS keychain (or `0600`)  |
| `shellui config migrate`                   | `shellui.config.ts` to JSON (keeps `.bak`)      |
| `shellui config split` / `unsplit`         | Split or merge section config files             |

Flags: `--config <dir|file>` (beats `SHELLUI_CONFIG`), `--host` (listen on `0.0.0.0`), `--app` (Tauri desktop, https://docs.shellui.com/tauri).

Isolation: the CLI ignores the project `vite.config.*`, PostCSS, Tailwind, `tsconfig` and `VITE_*`. Cache: `node_modules/.vite-shellui`. A shell and an iframe app can share one folder.

After init: add `static/` (`favicon.svg`, `logo.svg`, `icons/`), keep `dist/` gitignored.
