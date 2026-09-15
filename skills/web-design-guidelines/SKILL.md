---
name: web-design-guidelines
description: >-
  Use when reviewing Shellui website, docs, or in-shell UI, checking
  accessibility, auditing layout, or applying the Shellui web design handbook.
license: MIT
metadata:
  author: shellui
  version: '1.1.0'
---

# Web design guidelines

Review files for compliance with Shellui web design guidelines (accessibility, focus, forms, motion, iframe chrome, light/dark).

Canonical rules are published at [shellui.com/guidelines/web-design/](https://shellui.com/guidelines/web-design/). This skill is a thin wrapper: fetch the markdown, do not scrape HTML, do not duplicate the handbook here.

Inspired by the public web-interface-guidelines pattern from Vercel Labs; the rules are Shellui-specific (microfrontend host, themes, hyphen preference). Do not copy Vercel branding or dashboard links into Shellui UI.

For copy, also load [`writing-guidelines`](../writing-guidelines/). When composing pages, fetch design.md first via [`design-md`](../design-md/).

## How it works

1. Fetch the latest guidelines from the source URL below
2. Read the specified files (or ask which files to review)
3. Check against every rule in the fetched guidelines
4. Output findings in the terse `file:line` format from the guidelines

## Guidelines source

Fetch fresh guidelines before each review:

```
https://shellui.com/guidelines/web-design.md
```

Fallback (GitHub):

```
https://raw.githubusercontent.com/shellui/website/main/content/guidelines/web-design.md
```

Use WebFetch (or equivalent) to retrieve the latest rules. The YAML frontmatter `version` field is the public label (for example `Guidelines v1.1.0`). That file is the single source of truth.

## Usage

When a user provides a file or pattern:

1. Fetch guidelines from the source URL above
2. Read the specified files
3. Apply all rules from the guidelines
4. Output findings using the format specified in **Review output** in the fetched file

If no files are specified, ask which files to review.
