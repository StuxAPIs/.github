# Changelog

All notable changes to this repository are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v1.1.5

### Changed
- `CONTRIBUTING.md` and `profile/README.md`'s general contact address changed from `contact@stuxapis.net` to `hello@stuxapis.net`, matching the convention used across other StuxAPIs repos

## v1.1.4

### Changed
- StuxAPIs now has its own logo/icon (`https://global.media.stuxapis.net/logo.png` / `/icon.png`) instead of relying on a placeholder URL or the GitHub org avatar as a stand-in. `README.md` and `profile/README.md`'s header logo now points at the real hosted logo (was a broken/never-live `media.stuxapis.net/global/logo.png` URL), and both files' footer "Built & Maintained by StuxAPIs" icon now uses the real icon instead of `github.com/StuxAPIs.png`

## v1.1.3

### Changed
- `README.md` and `profile/README.md`'s footer brand-attribution block updated to the new two-line format (Built & Maintained by StuxAPIs, Hosted by Stuxedo / StuxAPIs is a part of the Stux.Group brand of businesses), replacing the older single-line disclaimer; `README.md`'s redundant separate "Made by StuxAPIs" line was also removed since the new footer already covers that

## v1.1.2

### Changed
- This changelog's preamble now uses the standard Keep a Changelog wording

## v1.1.1

### Changed
- `README.md` and `profile/README.md`'s "StuxAPIs is part of the Stux.Group Brand of Companies" line now includes the Stux.Group icon inline

## v1.1.0

### Added
- `LICENSE` (MIT, copyright Stux.Group) — this repo is StuxAPIs' own (not a fork), so it should carry an explicit copyright notice rather than the vague "open source and available for use and modification" line it had before

### Changed
- `README.md`'s License section now points at `LICENSE` and adds a dedicated Copyright section

## v1.0.1

### Fixed
- `generateMetrics.yml`'s `setup` job created the `metrics` branch by branching off `main`'s current commit, so
  it wasn't actually an orphan branch — it carried the whole repo history and file tree instead of starting
  empty. Now creates a true root commit (via the git empty-tree hash, no parents) and points `metrics` at that,
  so the branch only ever holds what the `gh-metrics/metrics` action commits to it. The already-created (wrong)
  `metrics` branch needs to be deleted so the next run recreates it correctly and regenerates the SVGs

## v1.0.0

### Added
- `VERSION.md`, `CHANGELOG.md`, `commit.sh`/`commit.bat` — brought the repo onto the standard StuxAPIs release flow (bump `VERSION.md`, update this changelog, run `commit.sh`/`commit.bat` to commit and tag `vX.Y.Z`)
