# Change Log

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

Individual skills also keep their own changelogs under `skills/<name>/CHANGELOG.md`.

<!---
## [Unreleased] - yyyy-mm-dd

### ✨ Feature – for new features
### 🛠 Improvements – for general improvements
### 🚨 Changed – for changes in existing functionality
### ⚠️ Deprecated – for soon-to-be removed features
### 📚 Documentation – for documentation update
### 🗑 Removed – for removed features
### 🐛 Bug Fixes – for any bug fixes
### 🔒 Security – in case of vulnerabilities
### 🏗 Chore – for tidying code

See for sample https://raw.githubusercontent.com/favoloso/conventional-changelog-emoji/master/CHANGELOG.md
-->

## [1.1.0] - 2026-09-15

### ✨ Feature

- Guideline skills that fetch public handbooks from https://shellui.com/guidelines/:
  - [`guidelines`](skills/guidelines/) (v1.0.0) parent index
  - [`design-md`](skills/design-md/) (v1.2.0) → https://shellui.com/design.md
  - [`writing-guidelines`](skills/writing-guidelines/) (v1.0.0) → https://shellui.com/guidelines/writing.md
  - [`web-design-guidelines`](skills/web-design-guidelines/) (v1.1.0) → https://shellui.com/guidelines/web-design.md

### 📚 Documentation

- README documents the guidelines hub and how catalog skills relate to shellui.com / `shellui/website`

## [1.0.0] - 2026-08-25

### ✨ Feature

- Catalog repository for Shellui Agent Skills
- Initial [`shellui`](skills/shellui/) skill (v1.0.0): naming rules (`shellui` / `Shellui`), SDK overlays, config/CLI, and SDK vs tiny
