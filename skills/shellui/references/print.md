# Print and the brand kit

Agent-readable Shellui brand kit, v1, October 2026. A4, 33 pages.

Humans use the PDF: https://shellui.com/brand-assets/shellui-brand-kit-v1.pdf

This file is the copy agents read. Logos and the zip: https://shellui.com/brand-assets/

The public summary is https://shellui.com/guidelines/print.md. Where that page and the PDF disagree, follow the PDF. Differences are at the end of this file.

Templates you can print are in `assets/print/`. Each HTML file is one section 8 template, with the kit's sample content. The PNG beside it is a preview of that page, not a file to trace. The gray line at the top right (`Template 8.x...`) is kit chrome. Drop it when you ship a real document. Page numbers in the samples are the kit's own page numbers, so the preview matches the PDF. A real document numbers body pages only.

Anything marked example, or set in a dashed box, is sample data. Replace it.

## How to make a document

1. Pick the matching template in `assets/print/`.
2. Keep the page size, margins, type, and colors below.
3. Replace sample data. Keep a real figure marked with its source.
4. One gold accent per page. Gold text is `#8A6300` on light paper. Brand gold `#E3A512` is for fills, rules, bars, and the logo, never for text.
5. Flat backgrounds only: white, mist, ink, or night. No gradients, washes, or shadows in a PDF.

## Page

- Size: A4, 210 x 297 mm. Slides: 297 x 167 mm (the file uses 167.0625 mm, a true 16:9).
- Margins: 20 mm top and sides, 22 mm bottom. Live area 170 x 255 mm.
- Slides: 12 mm margin on every side.
- Grid: 12 columns of 8.67 mm, gutter 6 mm. 11 gutters of 6 mm leave 104 mm of column, 8.67 mm each.
- Full width is the default. Text, tables, charts, and screenshots span all 12 columns, 170 mm, about 100 characters at body size.
- Long prose, more than three paragraphs: two columns of 81 mm, 8 mm apart, about 46 characters per line.
- Feature layout, optional: label in columns 1 to 3, content in columns 4 to 12, 8 mm apart. Only for covers, section openers, pull quotes, and showcase pages. The content below returns to full width.
- Never leave columns 1 to 3 empty beside running text. Snap every edge to a column or a gutter.
- Side by side blocks: 8 mm minimum.
- Running head and folio sit 10 mm from the trim, inset to the side margins, 7.5 / 10 pt.
- Running head: section or document name on the left, a short label on the right, slate. The head does not carry the page number.
- Folio: one page number, bottom right, tabular, ink, weight 600. The rest of the footer line is slate.
- No page number on covers, or on section dividers that read as covers. Body pages carry no logo, only the running head.
- Do not put the number in the head and the foot. That reads as two counts.

## Color

Flat only. One gold accent per page. A typical page is about canvas 70%, ink 18%, slate 6%, mist 4%, gold 2%.

CMYK below is an ICC conversion from sRGB with a generic CMYK profile, relative colorimetric. Ask the printer for their profile and a proof before a large run. Print body text in 100% K, and slate text in 70% K, so small type does not blur in registration.

| Name | Token | Hex | RGB | CMYK | Use |
| --- | --- | --- | --- | --- | --- |
| Ink | foreground | `#111827` | 17 24 39 | 80 71 60 84 | Text, rules, dark fills |
| Canvas | background | `#FFFFFF` | 255 255 255 | 0 0 0 0 | Page, cards |
| Brand gold | primary | `#E3A512` | 227 165 18 | 11 38 100 0 | Fills, rules, the logo. Never text |
| Gold ink | primary-ink | `#8A6300` | 138 99 0 | 39 57 100 25 | Gold text and links on light |
| Slate | muted-foreground | `#4B5563` | 75 85 99 | 76 64 46 31 | Secondary text, captions |
| Border | border | `#E5E7EB` | 229 231 235 | 9 7 5 0 | Hairlines, table rules |
| Mist | muted | `#F9FAFB` | 249 250 251 | 1 1 1 0 | Quiet wells, callouts |
| On gold | primary-foreground | `#1A1408` | 26 20 8 | 68 66 71 85 | Text on gold fills |
| Night | background, dark | `#030712` | 3 7 18 | 76 69 63 88 | Dark pages, slides, dark og:images |
| Gold tint | flat tint, print only | `#FDF6E3` | 253 246 227 | 0 2 11 0 | Flat fill behind a callout. Never a gradient |
| Dark slate | muted-foreground, dark | `#9CA3AF` | 156 163 175 | 42 32 25 0 | Secondary text on dark, chart series |
| Dark gold | primary, dark | `#E8B84A` | 232 184 74 | 9 29 89 0 | Gold text, links, and fills on dark screens. Not print text |

Gold text on a light background is `#8A6300`. `#E3A512` is for fills and the logo, never text. Gold text on a dark screen, including the website in dark mode, is `#E8B84A`. In print, a dark page carries no gold text. On a dark page, gold is a fill, a rule, or the mark in `#E3A512`.

Inline code chips in the templates use `#F3F4F6`. That chip is not a palette color. The giant mark on covers is `#F3F3F4`.

### Contrast

Body text needs WCAG AA: 4.5:1. Large text (18 pt, or 14 pt bold) needs 3:1. Ratios use the WCAG 2.2 formula.

| Pair | Ratio | WCAG |
| --- | --- | --- |
| Ink `#111827` on canvas | 17.7:1 | AAA |
| Slate `#4B5563` on canvas | 7.6:1 | AAA |
| Gold ink `#8A6300` on canvas | 5.4:1 | AA |
| Gold ink `#8A6300` on mist | 5.2:1 | AA |
| Brand gold `#E3A512` as text on canvas | 2.2:1 | Fail |
| On gold `#1A1408` on brand gold | 8.4:1 | AAA |
| White on brand gold | 2.2:1 | Fail |
| Mist `#F9FAFB` on night | 19.3:1 | AAA |
| Dark slate `#9CA3AF` on night | 7.9:1 | AAA |
| Gold ink `#8A6300` on night | 3.7:1 | Fail |
| Slate `#4B5563` on night | 2.7:1 | Fail |
| Dark gold `#E8B84A` on night, screen only | 10.9:1 | AAA |

- Do: on-gold text on a gold fill. `#1A1408` on `#E3A512`. Sample label: "Get started".
- Don't: white text on gold.
- Do: gold ink for a link or a label on light paper. Sample: "Read the changelog for what shipped in v0.6.0." The word "changelog" is `#8A6300`, underlined.
- Don't: body text in brand gold. Sample of the mistake: "Read the changelog for what shipped in v0.6.0. Brand gold body text is hard to read."

### Pantone and paper

Closest spot colors by CIEDE2000 against the digital Pantone Solid Coated and Solid Uncoated libraries (October 2026). Under 2 is hard to see. Above 5 reads as a different color. Confirm against a physical swatch book and a printed proof.

| Color | Coated | CIEDE2000 | Next coated | Uncoated | CIEDE2000 | Next uncoated |
| --- | --- | --- | --- | --- | --- | --- |
| Brand gold `#E3A512` | PANTONE 124 C | 1.4 | 2007 C, 1.7 | PANTONE 7405 U | 4.1 | 3514 U, 4.8 |
| Gold ink `#8A6300` | PANTONE 4027 C | 4.1 | 1265 C, 4.9 | PANTONE 132 U | 9.8 | No close uncoated match |

Gold ink has no close uncoated spot. On uncoated stock, print it in CMYK and check the proof.

Paper:

- Uncoated, bright white.
- About 120 g/m2 for reports and letterhead.
- About 300 g/m2 for covers and cards.
- Uncoated paper prints gold duller and type slightly heavier. Specify the U reference and proof first.

### Dark pages

Allowed in print, with light text, and gold only as a fill, a rule, or the mark.

Use them for covers, section openers, slides, one-message pages, and showcase pages for a dark UI screenshot. Not for long reading, forms, or pages people write on. One dark page sets a moment. A dark document tires the eye.

- Night converts to 296% total ink. Ask the printer for the coverage limit and a rich black, above all on uncoated stock.
- Mist on night is 19.3:1. Dark slate `#9CA3AF` on night is 7.9:1. Gold ink on night fails at 3.7:1. Slate `#4B5563` on night fails at 2.7:1.
- Reversed type: at least 9 pt, weight 400. No hairline under 0.5 pt.
- Do: mist text, dark slate for the secondary line, a gold rule, generous margins. Sample line: "Ship sooner without rebuilding basic features".
- Don't: gold ink or slate `#4B5563` as the text on night.

## Type

Print uses one family. IBM Plex Sans sets every word, from the H1 to the folio. IBM Plex Mono sets code, file paths, versions, and package names. Weights for Sans: 400, 500, 600. SIL Open Font License. Embed the fonts.

Do not set print or PDF text in Inter. Inter is for generated screen images only: og:images, social images, icons, and email. The website uses the system font stack.

Tables are Plex Sans with tabular figures, not Plex Mono. Use Mono inside a table only for a package name, a path, or a version.

Sizes are in points. Leading follows the slash.

| Style | Face | Size / leading | Weight | Sample |
| --- | --- | --- | --- | --- |
| Display | Plex Sans | 40 / 46 | 600 | Brand kit |
| H1 | Plex Sans | 26 / 32 | 600 | Ship sooner |
| Lede | Plex Sans | 12 / 18 | 400, slate | Open-source web app platform. |
| H2 | Plex Sans | 15 / 20 | 600 | Configure the iframe SDK |
| H3 | Plex Sans | 11.5 / 15.5 | 600 | Caveats on a custom domain |
| H4 | Plex Sans | 10 / 14 | 600 | Starting the SDK |
| Body | Plex Sans | 10.5 / 17 | 400 | Call init before the shell sends settings. Your app then reads the theme and locale from the shell. |
| Table | Plex Sans | 8.5 / 12.5 | 400, tabular | identity-service, Python, CHF 2'551.15 |
| Caption | Plex Sans | 8 / 12 | 400, slate | Figure 1. Features removed per app. Example data. |
| Folio | Plex Sans | 7.5 / 10 | 400, slate. The numeral is ink, 600 | Running heads and page numbers |
| Code | Plex Mono | 8.5 / 13 | 400 | `await init({ clientId: your_client_id_here })` |

Display and H1 tracking in the scale samples is tight (about -0.015 em and -0.01 em). H2 is about -0.005 em. Cover and slide titles in the templates use -0.025 em and a weight of 650, which renders with the 600 cut. Use 600.

Section labels in the templates (`.sec`) are 8.5 / 12 pt, weight 600, gold ink `#8A6300`.

### Screen scale

Not for print. Tailwind sizes used on shellui.com. Generated images use Inter.

| Class | Size, px | Use |
| --- | --- | --- |
| text-5xl | 48 / 48 | Feature page h1, semibold, tight |
| text-4xl | 36 / 40 | Inner page h1, bold |
| text-3xl | 30 / 36 | Section heading |
| text-2xl | 24 / 32 | Section heading, compact |
| text-lg | 18 / 28 | Lede, slate |
| text-base/7 | 16 / 28 | Body |
| text-sm | 14 / 20 | Buttons, labels, tables |
| text-xs | 12 / 16 | Badges, meta |

### Rules for print and screen

- Sentence case for every heading. Title case only in nav labels.
- Line length: at most about 100 characters at full width in print. Two columns for long prose. `max-w-3xl` on the web.
- Left aligned, ragged right. Never justify.
- One H1 per page or slide. Do not skip levels.
- Tabular figures in tables and prices.
- Hyphens, never em or en dashes. Units with a space: 64 KB, 200 ms, 12 GB. Seconds stay bare: 30s.
- Bold marks a UI element or a critical fact, not emphasis.
- No serif anywhere.
- Swiss grouping in sample prices: CHF 2'551.15. VAT sample: 8.1%.
- Placeholder shape: `your_access_token_here`. The code samples use `your_client_id_here`.

### Type do and don't

- Do: set the whole document in IBM Plex Sans. Sample: heading "Configure the iframe SDK", the init sentence, caption "Figure 2. Hours per week on release chores."
- Don't: mix a serif and a sans on one page.
- Do: sentence case, ragged right, about 70 characters per line.
- Don't: justified text or Title Case. Sample of the mistake: "Configure The Iframe SDK" set justified and tight.
- Do: hierarchy from size and weight. 400 for text, 600 for headings. Sample: "Section 2", "Two weights, one size step", "Hierarchy from size and weight."
- Don't: a tracked all-caps eyebrow, or many weights at once. Sample of the mistake: "FEATURES · PLATFORM".

## Spacing

Print base unit is 2 mm, written as u. One half step of 3.5 mm sits between paragraphs. List items are 2 mm. Not every step is a multiple of 2 mm: paragraphs are 3.5 mm, table cells are 2.5 mm vertically.

| Step | Print | Screen |
| --- | --- | --- |
| 1u | 2 mm | 4 px |
| 2u | 4 mm | 8 px |
| 3u | 6 mm | 12 px |
| 4u | 8 mm | 16 px |
| 6u | 12 mm | 24 px |
| 8u | 16 mm | 32 px |
| 10u | 20 mm | 40 px is not on the screen scale. Screen continues 48, 64, 96 px |
| 12u | 24 mm | 48 px |

Screen scale, 4 px base: 4, 8, 12, 16, 24, 32, 48, 64, 96.

| Element | Print | Screen |
| --- | --- | --- |
| Page margin | 20 mm (10u), bottom 22 mm | 16, 24, 32 px. og:image 72 px |
| Column gutter | 6 mm (3u). Columns 8.67 mm | 24 px. 32 px from 1024 px wide |
| Feature label to content | 8 mm (4u) | 32 px |
| Side-by-side blocks | 8 mm minimum | 32 px |
| Card or callout padding | 8 mm | 32 or 40 px |
| Stacked cards | 6 mm | 24 px |
| Table cell | 2.5 mm above and below, 3 mm each side | 12 px |
| Corner radius | 2 mm cards, 1.5 mm controls | 12 px cards, 6 px controls |

Child radius is less than or equal to the parent radius. Screen content widths: `max-w-7xl` 1280 px, `max-w-5xl` 1024 px, prose `max-w-3xl` 768 px. Header, body, and footer share one content edge.

- Do: every gap on the scale. Sample card "Storage" / "Upload and serve files." / "Read the docs", padding 8 mm, title to text 2 mm, text to button 6 mm.
- Don't: nudge spacing by eye.
- Do: one page number, bottom right. Sample head "Shellui brand kit" and "Spacing", foot number only.
- Don't: repeat the number. Sample of the mistake: head "Page 12 of 31" and foot "12", or head "Shellui report" with "12" in the head.

### Vertical rhythm

Seven tokens. A heading sits closer to the text it introduces than to the text above it. Every figure gets 10 mm of air. Gaps do not stack: when a figure ends right before an H2, use one 10 mm gap, not 10 plus 10.

| Token | Print | Screen | Use |
| --- | --- | --- | --- |
| space-3xl | 12 mm | 64 px | Above H1 when it follows content |
| space-2xl | 10 mm | 40 px | Above H2. Before and after tables, charts, callouts, screenshots, code |
| space-xl | 8 mm | 32 px | Card padding. Gap between side-by-side blocks and text columns |
| space-lg | 6 mm | 24 px | Above H3. Grid gutter. Between stacked cards |
| space-md | 4 mm | 16 px | Below H1 and H2. Above H4 |
| space-sm | 3.5 mm | 20 px | Between paragraphs |
| space-xs | 2 mm | 8 px | Below H3 and H4. Figure to caption. List items |

## Layout do and don't

- Do: run text pages full width. Long prose splits in two.
- Don't: leave columns 1 to 3 empty on a text page. That wastes about a fifth of the page.
- Do: one claim, left aligned. Supporting text sits under the heading, on the same left edge.
- Don't: a centered hero plus three equal cards.

## Logo

Two marks: the wordmark and the S mark. v1 has no lockup. Do not redraw, retype, recolor, stretch, rotate, outline, shadow, or combine them. If none of the six versions fits, change the background.

Clear space is measured from the artwork, not from the file bounds.

- Wordmark: clear space on every side is half the wordmark height. At 14 mm high the wordmark is 53.1 mm wide, so clear space is 7 mm.
- Mark: clear space on every side is half the mark width.

| Use | Version | File | Size | Position |
| --- | --- | --- | --- | --- |
| Report cover | Wordmark, ink | `logo/shellui-wordmark-ink.svg` | 9 mm high | Top left, on the margins |
| Letters, quotes, product sheet, proposal | Wordmark, ink | same | 6 mm high | Top left, on the margins |
| Slides | Mark, ink | `logo/shellui-mark-ink.svg` | 6 mm high | Top left, 12 mm in |
| og:image, social | Mark | `logo/shellui-mark-ink.svg` or white | 44 px high | Top left, 72 px in |
| Minimum, wordmark | Wordmark | | 18 mm wide, or 72 px wide | Below that, use the mark |
| Minimum, mark | Mark | | 4 mm high, or 16 px high | Favicon size |

Six approved versions. SVG first, PNG when a vector will not load.

- Wordmark, ink, on white and light gray: https://shellui.com/brand-assets/logo/shellui-wordmark-ink.svg and `shellui-wordmark-ink-2048.png`
- Wordmark, white, on ink, night, and a dark area of a photo: https://shellui.com/brand-assets/logo/shellui-wordmark-white.svg and `shellui-wordmark-white-2048.png`
- Mark, ink, for small spaces, nav, footers, slides: https://shellui.com/brand-assets/logo/shellui-mark-ink.svg and `shellui-mark-ink-1024.png`
- Mark, gold on ink, for avatars and app icons: https://shellui.com/brand-assets/logo/shellui-mark-gold.svg and `shellui-mark-gold-1024.png`
- Icon, white on black: the favicon and app icons in `brand-assets/icons/`
- Mark, on gold: stickers and merch only. The mark is on-gold `#1A1408` sitting on `#E3A512`. There is no separate file for that pair.

There is no gold wordmark file. A gold wordmark on white is 2.2:1 and is a mistake. A gold mark goes on ink or night only.

- Do: official wordmark, ink on white, full clear space.
- Don't: stretch or squash. Scale with the aspect ratio locked. Wordmark ratio is 1024 / 270. Mark ratio is 493.40 / 681.33.
- Do: white wordmark on `#111827` or `#030712`.
- Don't: the wordmark in gold on white.
- Do: the mark alone in a favicon, an avatar, or the site nav.
- Don't: invent a lockup.
- Do: place the logo on a calm dark area of a photo. Darken the photo until the logo passes 4.5:1.
- Don't: gradients, shadows, outlines, or rotation.

Do not use the logo to suggest Shellui endorses, sponsors, or partners with you unless it does. Questions: open an issue at github.com/shellui.

## Charts, screenshots, photos

A chart makes one point. The title or the caption states the finding, not the metric. Gold marks that point. White space sets the chart apart from the text.

- Gray series `#9CA3AF`. One gold highlight `#E3A512`, value labeled in ink.
- Label lines and bars directly. Skip the legend when you can.
- Bars start at zero. No 3D. No pie with more than three slices.
- Chart text is IBM Plex Sans. Axis 7 pt slate. Labels 8 pt. Tabular figures.
- Gridlines `#E5E7EB`, 0.2 pt. The baseline is a little stronger, about `#9CA3AF`.
- 10 mm of white space above and below every chart, screenshot, and table.
- Caption under the figure: figure number, the finding in one line, and the source. 8 / 12 pt. The figure number is ink, weight 600. The rest is slate. 2 mm under the figure.
- One figure per reading moment. If two figures do not fit with full spacing, move one to the next page.
- Mark sample figures as example data.

Do: one series, October in gold, value labeled. Example data: Jul 42, Aug 51, Sep 58, Oct 74, axis to 80.

Don't: a rainbow, shadows, and a legend. The mistake uses red, green, blue, and purple bars named Series 1 to 4.

Screenshots:

- Shipping UI only, captured at 2x, current version.
- Frame: 0.4 pt border `#E5E7EB`, 2 mm radius (12 px on screen). No device mock, no shadow.
- Photography: real places and real work, natural light. Zurich is the home city.
- Print, PDFs, og:images, and social images stay flat: white, mist, ink, or night.
- A soft gold wash is allowed on the website only, behind the hero.

- Do: 10 mm above and below, caption 2 mm under.
- Don't: two figures crammed against text, with no caption.
- Do: the real shellui.com home page in a plain frame. The sample capture is October 2026, file `assets/print/sample-home.jpg`.
- Don't: an invented dashboard. Sample of the mistake: "Users 98k", "AI score 99%", "Growth +412%".
- Do: a flat ground. The type and the mark carry the brand.
- Don't: a gradient or a gold wash on print or social.

## Templates

Sample content below is the kit's sample data. The HTML files repeat it so a print matches the PDF page.

Shared report chrome, pages 8.2 to 8.4: running head "Running Shellui in production" and "Example document". Footer "Shellui, example document" and the kit page number.

### 8.1 Report cover

File: `assets/print/report-cover.html`. Kit page 19. No folio.

- Ghost mark `#F3F3F4`, 240 mm high, bleeding off the bottom right (right -40 mm, bottom -60 mm).
- Wordmark, ink, 9 mm high, at the 20 mm margin, 20 mm from the top.
- Gold rule 20 mm by 1.2 mm, radius 0.6 mm, starting 96 mm from the top.
- Kicker, 6 mm under the rule, 10.5 pt gold ink, weight 600. Sample: "Platform report, example document".
- Title, 3 mm under the kicker, 40 / 44 pt, weight 600, tracking -0.025 em, width 150 mm. Sample: "Running Shellui in production".
- Lede, 6 mm under the title, 13 / 19 pt slate, max 120 mm. Sample: "How three sample teams moved authentication, administration, and storage into the shell, and what changed in their release work."
- Meta row on a 0.8 pt ink rule, 26 mm from the bottom, 4 mm of padding, four columns. Labels ink, values slate 8 pt. Sample: Prepared by / Author name. Date / October 2026. Version / 1.0. Audience / Engineering leads.

### 8.2 Report body, text and headings

File: `assets/print/report-body.html`. Kit page 20.

- Section label on its own line, gold ink: "2 Architecture". Then the H1. This page is not a 3 + 9 split. The label stacks above the title, then the text goes full width.
- H1, sample: "How the shell wraps your app".
- Lede, sample: "The shell owns navigation, sign-in, settings, and toasts. Your app runs in an iframe and reads that context through `@shellui/sdk`."
- H2, 10 mm down: "Shared navigation and identity".
- Two columns, 8 mm apart. Left column, two paragraphs. Sample: the three apps and three login screens, then identity-service, RSA, and JWKS.
- Right column starts with H3 "What the shell provides to your app". Then: "After you call `init`, your app receives:" and three bullets: the signed-in account and a token, theme and locale, toasts and modals and drawers rendered by the shell.
- H3 "Starting the SDK". Sample: "Call `init` once, before the shell sends settings. The call resolves when the shell answers."
- Note under a 0.8 pt ink rule, 8 pt. Sample: "Note. JSON Web Key Set (JWKS): the public keys that services use to verify tokens."
- Code block, mist, 2 mm radius, 8 mm padding, Plex Mono 8.5 / 13. Keywords `import`, `from`, and `await` are gold ink. Sample:

```
import { init } from "@shellui/sdk";

await init({
  clientId: your_client_id_here,
});
```

- Callout, mist, gold left bar 1 mm, square left corners. Sample: "Key finding. Example data: the three sample teams removed an average of 4 duplicated features per app after the move."

### 8.3 Report body, table and chart

File: `assets/print/report-table-chart.html`. Kit page 21.

- Feature row: gold label "3 Results" in columns 1 to 3. Title in columns 4 to 12 at 18 / 23 pt, weight 600. Sample: "Team D removed the most duplicated work".
- Intro, sample: "The table lists the services in the stack. The chart compares how many duplicated features each sample team removed per app. Chart figures are example data."
- Table, full width. Header row has a 0.8 pt ink rule. Body rows have a 0.4 pt border rule. Service names are Plex Mono 8 pt. Sample rows:

| Service | Role | Language | License |
| --- | --- | --- | --- |
| shellui | Shell and @shellui/sdk | TypeScript | MIT |
| identity-service | Sign-in, sessions, JWKS | Python | MIT |
| admin | Users, roles, settings at /admin | TypeScript | MIT |
| storage-service | Uploads, serving large files | Python | MIT |
| email-service | Templates and sending | Python | MIT |
| hosting-service | Deploy and serve apps | Python | MIT |

- Caption, sample: "Table 1. Repositories in the Shellui stack. Source: github.com/shellui, October 2026."
- Paragraph, sample: "Team D ran four internal apps before the move, more than any other team, so it had the most to remove. Teams B and C started with two apps each."
- Bar chart, 170 mm by 62 mm, axis 0 to 12. Gray bars, Team D in gold with the value labeled. Example data: Team A 6, Team B 4, Team C 3, Team D 9, Team E 5.
- Caption, sample: "Figure 1. Duplicated features removed per app, by team. Example data."

### 8.4 Report body, figure and screenshot

File: `assets/print/report-figure.html`. Kit page 22. Screenshot file: `assets/print/sample-home.jpg`.

- H2, sample: "Release chores dropped by two thirds".
- Paragraph, sample: "Before the move, each release meant updating login screens and settings pages in every app. After six weeks in the shell, the sample teams spent about 5 hours a week on those chores instead of 15."
- Line chart, 170 mm by 54 mm, axis 0 to 20, weeks W1 to W6. Direct labels, no legend. Example data: "After move" in gold, 14, 12, 9, 7, 6, 5. "Before move" in `#9CA3AF`, 14, 15, 14, 16, 15, 16.
- Caption, sample: "Figure 2. Hours per week on release chores over six weeks. Example data."
- H3 "What your users see". Sample: "Users get one sign-in and one navigation bar across every app. The home page of shellui.com runs the same shell chrome."
- Screenshot at 170 mm, 0.4 pt border, 2 mm radius.
- Caption, sample: "Figure 3. shellui.com home page, captured in October 2026."

### 8.5 Letterhead

File: `assets/print/letterhead.html`. Kit page 23.

- Fold marks on the left edge, `#9CA3AF`, 0.4 pt: 4 mm at 105 mm and at 210 mm, 6 mm at 148.5 mm.
- Wordmark 6 mm, 20 mm from the top and the left.
- Sender block, top right, 7.5 pt, right aligned. "Shellui" in ink. Then dashed placeholders: [Company name], [Street and number], [Postcode, city, country], [Email]. Then "shellui.com" with no box.
- Return line at 118 mm from the left, 52 mm from the top, 72 mm wide, 7.5 pt, hairline under it. Sample: "Shellui, [Company name], [Address]".
- Address, sample: Example AG, Anna Muster, Bahnhofstrasse 1, 8001 Zurich.
- Date line at 100 mm from the top. Sample: "[City], 25 October 2026". The city stays in a dashed box.
- Subject, 11.5 pt, weight 600, 8 mm under the date. Sample: "Your customer portal on Shellui".
- Body at 10.5 / 17, 5 mm under the subject. Sample paragraphs: the Tuesday call, the shell around the portal, the half-day workshop in November, "I look forward to hearing from you."
- "Kind regards" 6 mm down. Signature block 12 mm down. Sample: "Max Muster", "Solutions engineer, Shellui (example)". Enclosure 6 mm down, 8 pt: "Enclosure: quote Q-2026-0042".
- Footer hairline, 7.5 pt slate: "[Company name], [Address]. UID [UID or VAT number]. shellui.com" and the page number.

### 8.6 Quote and invoice

File: `assets/print/quote-invoice.html`. Kit page 24. One page covers the quote. The same header and footer fit an invoice. Amounts are example data.

- Same wordmark and sender block as the letterhead.
- Left, from 52 mm down: label "Client", then Example AG, Anna Muster, Bahnhofstrasse 1, 8001 Zurich.
- Right, a tight table: Quote number Q-2026-0042, Date 25 October 2026, Valid until 24 November 2026, Contact Max Muster.
- Title "Quote" at 24 / 29 pt, with a gold-tint pill "Example data" (`#FDF6E3` ground, `#8A6300` text, `#F1D58F` hairline).
- Subtitle, slate: "Customer portal on Shellui. Amounts in Swiss francs."
- Lines, 9 / 13 pt, tabular prices. Sample:

| # | Description | Quantity | Unit price CHF | Amount CHF |
| --- | --- | --- | --- | --- |
| 1 | Example service. Short description of the service | 1 pc | 1'000.00 | 1'000.00 |
| 2 | Example workshop. Half day, remote | 4 h | 150.00 | 600.00 |
| 3 | Example setup. One-time configuration | 1 pc | 800.00 | 800.00 |

- Totals, right aligned, 82 mm wide: Subtotal 2'400.00. VAT 8.1% on CHF 2'400.00 is 194.40. Rounding to 5 centimes +0.00. Total CHF 2'594.40 on a 0.8 pt ink rule, 11 pt, weight 600.
- Terms, sample: "Payment within 30 days of invoice. Amounts are examples. Travel is billed separately."
- Payment, sample: "IBAN [IBAN]", "Bank [Bank name, city]", "The invoice includes a Swiss QR-bill payment slip." IBAN and bank stay dashed.
- Acceptance box, mist, 6 mm by 8 mm padding: "To accept, sign and return this quote, or reply to the email it came with." Two signature rules: "Place and date" and "Signature, Example AG".
- Same legal footer as the letterhead.

### 8.7 Product sheet

File: `assets/print/product-sheet.html`. Kit page 25.

- Wordmark 6 mm on the left. Right: "Product sheet, October 2026", 8 pt slate.
- H1 at 32 / 36 pt, max 150 mm. Sample: "The shell around your web app".
- Lede, max 140 mm. Sample: "Shellui is an open-source web app development platform: a microfrontend shell that wraps your application with shared navigation, authentication, storage, and administration."
- Diagram, 170 mm by 46 mm, 2 mm-class radius, hairline border. Top bar mist: mark, "Shell", "Navigation, account, theme, locale", gold "Account" pill with on-gold text. Left rail mist with five bars. Right: gold tint `#FDF6E3`, dashed gold stroke, "Your app, in an iframe", "Any framework. Talks to the shell through @shellui/sdk".
- Two columns, 8 mm apart.
- Left, "What ships today". Sample rows, hairline between them: Shell and SDK. Identity (identity-service, magic links, OAuth, sessions). Administration (users, roles, settings at `/admin`). Storage and Files. Email (transactional mail, newsletters, broadcasts). Hosting.
- Right, "Run it your way": Self-host, free (MIT, Docker images on hub.docker.com/u/shellui). Shellui hosting (managed hosting, details on shellui.com). Expert help (architecture, custom work, support from the maintainer). Then the same `init` code block as 8.2.
- Footer on a 0.8 pt ink rule, 12 mm from the bottom: "shellui.com · docs.shellui.com · github.com/shellui · Made in Zurich" and the page number. "shellui.com" is ink, weight 600.

### 8.8 Proposal

File: `assets/print/proposal.html`. Kit page 26.

- Running head, sample: "Proposal for Example AG" and "Q-2026-0042".
- Wordmark 6 mm, and a pill "Sample proposal".
- Feature row: gold label "Proposal", H1 "A customer portal on Shellui in seven weeks".
- Lede, sample: "You keep your React front end. Shellui adds sign-in, roles, file storage, and an admin area around it, so your team spends the seven weeks on portal screens."
- The sections under the opener return to full width.
- H2 "Scope and timeline". Sample rows:

| # | Phase | What you get | When |
| --- | --- | --- | --- |
| 1 | Workshop and plan | Map current apps, pick the first two to move | Week 1 |
| 2 | Shell and identity | Deploy the shell, connect Keycloak through identity-service | Weeks 2 to 3 |
| 3 | Move the portal | Run the portal in the shell, add storage and /admin | Weeks 4 to 6 |
| 4 | Handover | Documentation, training, support window | Week 7 |

- H2 "At a glance". Three cards, 8 mm apart, 8 mm padding, 2 mm radius, mist. The third card is gold tint, text on gold. Sample, all marked example: Duration 7 weeks. Team 2 engineers. You save 6 weeks, "Auth and roles, estimate".
- Caption: "All figures are examples for this template."
- H2 "Next steps". Numbered: reply to confirm the workshop date, share read access to the three existing repositories, sign the quote to reserve weeks 2 to 7.
- Footer: "Shellui, [Company name], [Address]" with the company and address in dashed boxes, plus the page number.

### 8.9 Presentation, 16:9

File: `assets/print/presentation.html`. Two pages. Kit pages 27 and 28. Page size 297 x 167 mm, margins 12 mm. Mark, ink, 6 mm, top left.

Title slide:

- Ghost mark `#F3F3F4`, 200 mm high, bleeding off the bottom right.
- Title at 52 mm from the top, 34 / 38 pt, weight 600, tracking -0.025 em, width 190 mm. Sample: "Ship sooner without rebuilding basic features".
- Subtitle 15 / 21 pt slate, 6 mm under the title. Sample: "Shellui overview for engineering teams".
- Footer 9 pt, 10 mm from the bottom. Sample: "Speaker name" in ink, ", role" in slate, and "October 2026" on the right. No page number.

Content slide. Sample label at the top right: "Why a shell".

- Title, 24 / 29 pt, width 130 mm. Sample: "Your team builds the product, not the chrome".
- Bullets, 13 / 19 pt: "Sign-in, roles, and settings come with the shell". "Your app runs in an iframe, in any framework". "MIT licensed and self-hosted".
- Chart on the right, 120 mm by 72 mm, titled "Days of work per area, example project". Axis 0 to 24. Example data: Auth 14, Roles 9, Settings 6, Uploads 8, Your app 23 in gold with the value labeled. Note: "Example data. Gold marks the time left for your own product."
- Callout, 13 / 19 pt, 1.2 mm ink bar. Sample: "37 of 60 days go to sign-in, roles, settings, and uploads in this example. The shell gives them back to your product."
- Footer 8 pt: "shellui.com" and the page number.

## Cheat sheet

The values to pin. Kit page 32.

Color: ink `#111827`, slate `#4B5563`, brand gold `#E3A512`, gold ink `#8A6300`, on gold `#1A1408`, border `#E5E7EB`, mist `#F9FAFB`, night `#030712`, gold tint `#FDF6E3`, dark gold `#E8B84A` for screens. Pantone 124 C / 7405 U for brand gold. Confirm on a proof.

Type: Plex Sans in print, Plex Mono for code. System font on the website. Inter for generated images. Body 10.5 / 17. Display 40 / 46 and H1 26 / 32, weight 600. H2 15 / 20, H3 11.5 / 15.5, H4 10 / 14. Table 8.5 / 12.5 tabular. Caption 8 / 12 slate. Code 8.5 / 13 Mono. Web body 16 / 28 px, `max-w-3xl`.

Writing: the name is Shellui, never The Host. Sentence case. Hyphen only. Do not use easy, simple, quick, just, very, really, simply, seamless, robust, powerful, unlock, leverage. Active voice, "you", under 20 words. Units: 64 KB, 200 ms, 30s. Numbers: CHF 2'551.15, 8.1% VAT. Mark example data as example.

Logo: wordmark for documents, covers, and footers. Mark for icons, avatars, nav, and slides. Clear space is half the wordmark height, or half the mark width. Minimum 18 mm or 72 px wide for the wordmark, 4 mm or 16 px for the mark. Cover 9 mm, letter 6 mm, top left. Never stretch, recolor, rotate, add effects, or invent a lockup.

Files: `brand-assets/logo/`, `brand-assets/og/og-*.png`, `brand-assets/social/`, `brand-assets/icons/`, `brand-assets/email/`.

Vertical rhythm: above H1 12 mm, above H2 10 mm, above H3 6 mm, above H4 4 mm, below H1 and H2 4 mm, below H3 and H4 2 mm, figures 10 mm before and after, paragraphs 3.5 mm, list items 2 mm, caption 2 mm under the figure.

Check before you send:

- Official logo file, clear space kept, no effects.
- One gold accent. Gold text `#8A6300`, or `#E8B84A` on a dark screen.
- Every text pair at 4.5:1 or more.
- One family: IBM Plex Sans, body 10.5 / 17 pt.
- Edges on the 12 column grid, gaps on the scale.
- Sample figures marked as example data.
- One page number, bottom right, none on covers.
- Real screenshots and real data, sources under charts.
- Flat print and social. The gold wash stays on the website.

## Digital files

Not print templates. Sizes an agent needs when the same brand files ship next to a PDF. Sections 9 and 10.

og:image, 1200 x 630 PNG, under 300 KB, in `brand-assets/og/`:

- `og-default.png`: home and pages without their own image. Flat white. Mark at 4% opacity, cropped.
- `og-docs.png`: guide title, section path, docs URL.
- `og-blog.png`: dark canvas. The only dark variant. Night `#030712`, dark gold `#E8B84A` for the mark and fills only.
- `og-changelog.png`: version pill, release title, highlights, date.

Safe margin 72 px. The mark row can use 64 px at the top. Mark 44 px, top left, page label 24 px slate. Title: Inter, weight 650, 64 px, 1.08 leading, 3 lines or 60 characters. Lede 26 px slate, 2 lines. No gradient.

Social, in `brand-assets/social/`:

- Avatars 800 x 800: `avatar-dark-800.png` (default), `avatar-gold-800.png`, `avatar-light-800.png`. The mark fills 50% of the height so a circle crop still works.
- X banner `x-banner-1500x500.png`, 1500 x 500. Text sits right of center. Leave the bottom left empty. That is where X places the avatar.
- LinkedIn personal banner `linkedin-banner-1584x396.png`, 1584 x 396. Company cover `linkedin-company-cover-1128x191.png`, 1128 x 191.
- GitHub preview `github-social-preview-1280x640.png`, 1280 x 640. GitHub asks for 40 px of empty border. This file keeps 96 px.

Email: `brand-assets/email/email-signature.html`. HTML table, inline styles, system fonts. Name at 15 px semibold, role in slate, one gold ink link. No tagline, banner, quote, legal paragraph, or "sent from" line. Logo image 40 px, hosted at shellui.com. No attachments, no social icon row. Replace the example name and role.

Icons, white mark on black, in `brand-assets/icons/`. The mark grows to 82% at 16 to 48 px. `maskable-512.png` keeps the mark at 44% for the Android safe zone.

- `favicon.ico` (16, 32, 48), `favicon.svg`, `favicon-16.png`, `favicon-32.png`, `favicon-48.png`
- `app-icon-64.png`, `app-icon-180.png`, `app-icon-192.png`, `app-icon-512.png`, `app-icon-1024.png`
- `app-icon-gold-180.png`, `app-icon-gold-512.png`
- `maskable-512.png`

```html
<link rel="icon" href="/favicon.ico" sizes="32x32">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/app-icon-180.png">
```

## What shipped in v1

October 2026 is the first public release.

- Brand gold `#E3A512` for the logo, fills, rules, and chart highlights.
- Dark gold `#E8B84A` for gold text, links, the mark, and fills on dark screens.
- Gold ink `#8A6300` for gold text and links on light, on screen and in print. 5.4:1 on white.
- Pantone references and a paper recommendation, to confirm on a proof.
- Website: system font stack. Generated images: Inter. Print: IBM Plex Sans, Plex Mono for code.
- Full width is the default. A left title column only on covers, openers, and showcase pages.
- Print, PDFs, og:images, and social images stay flat. A soft gold wash is on the website only.
- Dark pages are allowed, with light text and gold only as a fill.
- No lockup. The mark and the wordmark stay separate.
- In the templates, company details are dashed placeholders. Names, items, and amounts are examples.

## Differences from print.md

https://shellui.com/guidelines/print.md is the short public page. Follow this file, and the PDF, when they disagree.

- Numeric tables. The public page says IBM Plex Mono for numeric tables. The PDF sets tables in IBM Plex Sans, 8.5 / 12.5 pt, tabular figures. Mono is for code, file paths, versions, and package names. In template 8.3 only the service name is Mono.
- Paper. The public page says coated 150 gsm silk for photography, uncoated 120 gsm for type, and 250 gsm covers. The PDF says uncoated bright white, about 120 g/m2 for reports and letterhead, about 300 g/m2 for covers and cards. It does not specify coated silk or 150 gsm.
- Gold ink, uncoated. The public page says "verify against swatch" and names no uncoated number. The PDF names PANTONE 132 U at CIEDE2000 9.8 and says there is no close match, so print gold ink in CMYK on uncoated stock and proof it. Coated is PANTONE 4027 C at 4.1, next 1265 C at 4.9.
- Dark pages. The public page says they are allowed anywhere, including covers. The PDF agrees they are allowed, including covers, and then limits them: covers, section openers, slides, one-message pages, and dark UI showcases. Not for long reading, forms, or pages people write on. A whole dark document is too much.
- Spacing. The public page calls 2 mm a baseline unit for every step. The PDF also uses 3.5 mm between paragraphs and 2.5 mm of vertical table padding.

The public page does not carry the type scale, the RGB and CMYK builds, gold tint, dark gold, 100% K text, the chart rules, the logo sizes, or the section 8 layouts. Use this file for those.
