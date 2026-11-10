---
name: print
description: >-
  Use before making any Shellui PDF, report, deck, one-pager, letterhead,
  invoice, quote, product sheet, proposal, or other printed or exported
  document. Start from the brand kit templates and read print.md in the
  shellui skill. The brand kit PDF is the visual reference.
license: MIT
metadata:
  author: shellui
  version: '1.0.0'
---

# Print

Use this before any Shellui PDF or other printed or exported document. This skill points at the print reference and the templates. Start from the matching template.

Read the print reference first:

- In this repo: [../shellui/references/print.md](../shellui/references/print.md)
- Installed alone: https://raw.githubusercontent.com/shellui/skills/main/skills/shellui/references/print.md

Templates are in [../shellui/assets/print/](../shellui/assets/print/). Installed alone, fetch `https://raw.githubusercontent.com/shellui/skills/main/skills/shellui/assets/print/<file>`.

Visual reference: https://shellui.com/brand-assets/shellui-brand-kit-v1.pdf

Where the shellui [print.md](../shellui/references/print.md) linked above and https://shellui.com/guidelines/print.md disagree, follow the shellui print.md.

## Templates

| Document | File | Brand kit |
| --- | --- | --- |
| Report cover | [report-cover.html](../shellui/assets/print/report-cover.html) | 8.1 |
| Report body | [report-body.html](../shellui/assets/print/report-body.html) | 8.2 |
| Report table and chart | [report-table-chart.html](../shellui/assets/print/report-table-chart.html) | 8.3 |
| Report figure | [report-figure.html](../shellui/assets/print/report-figure.html) | 8.4 |
| Letterhead | [letterhead.html](../shellui/assets/print/letterhead.html) | 8.5 |
| Quote and invoice | [quote-invoice.html](../shellui/assets/print/quote-invoice.html) | 8.6 |
| Product sheet | [product-sheet.html](../shellui/assets/print/product-sheet.html) | 8.7 |
| Proposal | [proposal.html](../shellui/assets/print/proposal.html) | 8.8 |
| Presentation | [presentation.html](../shellui/assets/print/presentation.html) | 8.9 |

The PNG beside each HTML file is the preview to compare against. The deck has two: [presentation-title.png](../shellui/assets/print/presentation-title.png) and [presentation-content.png](../shellui/assets/print/presentation-content.png). `presentation.html` is both of those slides, still section 8.9.

## Steps

1. Read print.md from the repo path or the raw URL above.
2. Start from the matching template and keep its CSS: A4, IBM Plex Sans, the grid, the colors, and the folios. No folio on the cover. The deck template stays 297 x 167 mm, and its title slide has no folio.
3. Replace every sample marker with real content. Drop the gray `Template 8.x` line, fill every dashed placeholder, and replace anything marked example.
4. Render with headless Chromium.
5. Render the pages to PNG and compare them with the template preview.
