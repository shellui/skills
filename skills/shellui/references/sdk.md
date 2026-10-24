# SDK

## Full SDK (`@shellui/sdk`)

```js
import { shellui } from '@shellui/sdk';
await shellui.init(); // first, always

shellui.toast({ title: 'Saved', type: 'success' });
shellui.dialog({ title: 'Delete?', mode: 'okCancel', onOk: () => {} });
shellui.openModal('/settings');
shellui.openDrawer({ url: '/filters', position: 'right', size: '400px' });
shellui.closeDrawer();
shellui.navigate('/dashboard');
shellui.login({ method: 'oauth', provider: 'github' });
```

Also `shellui.storage`, `selectFiles`, `selectFolders`. Details: https://docs.shellui.com/sdk

Router-less React app, two-way route sync with the shell:

```tsx
import { useShelluiNavigation } from '@shellui/sdk/react';
const { location, navigate } = useShelluiNavigation(import.meta.env.BASE_URL);
```

Apps with React Router or TanStack Router need nothing: the SDK reports history changes.

## Tiny (`@shellui/sdk/tiny`): theme, language, nav only

```js
import shellui from '@shellui/sdk/tiny';
await shellui.ready;
shellui.applyTheme();
shellui.on('theme', () => shellui.applyTheme());
```

CDN: `https://cdn.jsdelivr.net/npm/@shellui/sdk/dist/shellui.tiny.js` (sets `window.shellui`). No auth, storage or overlays.

`layout: "windows"` is shell config. Do not build windowing inside an iframe.
