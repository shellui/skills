# App frames and per-app identity

## Host a Shellui app inside an app

```tsx
import { ShelluiFrame } from '@shellui/sdk/react';

<ShelluiFrame
  title="Admin"
  src="https://admin.example.com/users"
  backend={{ url: 'https://id.eu.example.com', companyId: 'abc', provider: 'upstream' }}
  onNavigate={(loc) => navigate(`/admin${loc.fullPath}`)}
  fallback={<Spinner />}
  renderError={(retry, status) => <Button onClick={retry}>Retry</Button>}
/>;
```

No React: `const frame = createAppFrame(iframe, { url, backend, onNavigate, onReady, onSession })` from `@shellui/sdk`, then `frame.destroy()` on teardown.

- Hidden behind `fallback` until the child sends `SHELLUI_INITIALIZED`. After 20 s (`readyTimeoutMs`) `renderError(retry, status)` shows. `status.reason` / `hint` explain a missing session (`onSession`).
- New `src` or `backend` reloads the frame. Child navigation never does: mirror it via `onNavigate`, pass it back in `src` for deep links.
- Allow hosting on the host app's nav item, exact origins only:

```json
"childFrames": { "origins": ["https://admin.example.com"], "backendOrigins": ["https://id.eu.example.com"] }
```

Without an allowed `backendOrigins` entry the child gets no token, user or service URLs.

## Per-app identity server

A nav item `backend` (`url`, `type`, `companyId`, `provider`, `publishableKey`) gives that app a separate session. The shell token is never sent to it. If `backend` differs from the shell and `email` / `storage` / `hosting` are omitted on the item, the app gets `null` for them.

## Regional servers: token exchange (`provider: "upstream"`)

- `companyId` is the regional company id, not the shell one.
- The shell calls `POST {url}/oauth/token` (RFC 8693, `subject_token` = shell access token). The app only gets the regional access token.
- Renewal uses the regional refresh token first (kept in `sessionStorage`). Re-exchange only when there is no session, refresh fails, or the user changes. Shell sign-out clears all regional sessions.
- Regional identity-service (>= 0.9.1) needs `OIDC_CORS_ALLOWED_ORIGINS` with the shell origin (not the app origin), plus `GLOBAL_ISSUER_URL`, `GLOBAL_JWKS`, `GLOBAL_ACCESS_TOKEN_AUDIENCE`. Global staff are refused: they use a regional account.
- Other providers use a hidden-frame silent sign-in. Add the shell origin to that server's redirect allowlist.

Docs: https://docs.shellui.com/features/app-frames, https://docs.shellui.com/features/authentication
