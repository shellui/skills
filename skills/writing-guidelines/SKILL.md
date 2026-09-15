---
name: writing-guidelines
description: >-
  Use when reviewing Shellui website or docs prose, checking writing style,
  auditing voice and tone, rewriting marketing copy, or applying the Shellui
  writing handbook.
license: MIT
metadata:
  author: shellui
  version: '1.0.0'
---

# Writing guidelines

Review files for compliance with Shellui writing guidelines.

Canonical rules are published at [shellui.com/guidelines/writing/](https://shellui.com/guidelines/writing/). This skill is a thin wrapper: fetch the markdown, do not scrape HTML, do not duplicate the handbook here.

Inspired by the public writing-handbook pattern from Vercel Labs; the rules are Shellui-specific (voice, product, hyphen preference). Do not copy Vercel branding, model catalogs, or dashboard links into Shellui copy.

For UI, accessibility, and chrome, also load [`web-design-guidelines`](../web-design-guidelines/).

## How it works

1. Fetch the latest guidelines from the source URL below
2. Read the specified files (or ask which files to review)
3. Check against every rule in the fetched guidelines
4. Output findings in the terse `file:line` format from the guidelines

## Guidelines source

Fetch fresh guidelines before each review:

```
https://shellui.com/guidelines/writing.md
```

Fallback (GitHub):

```
https://raw.githubusercontent.com/shellui/website/main/content/guidelines/writing.md
```

Use WebFetch (or equivalent) to retrieve the latest rules. The YAML frontmatter `version` field is the public label (for example `Guidelines v1.0.0`). That file is the single source of truth.

## Usage

When a user provides a file or pattern:

1. Fetch guidelines from the source URL above
2. Read the specified files
3. Apply all rules from the guidelines
4. Output findings using the format specified in **Review output** in the fetched file

If no files are specified, ask which files to review.
