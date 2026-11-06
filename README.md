<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stuxapis.net/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stuxapis.net/logo-dark.png"><img src="https://global.media.stuxapis.net/logo-dark.png" height="100" alt="StuxAPIs Logo"></picture>
</p>

# StuxAPIs GitHub Configuration

The central repository for StuxAPIs' GitHub organization configuration and profile settings.

## Overview

This repository holds StuxAPIs' GitHub organization profile and the defaults GitHub applies across the
organization. Every StuxAPIs API and service is listed at [services.stuxapis.net](https://services.stuxapis.net),
with live status at [status.stuxapis.net](https://status.stuxapis.net).

## What's Included

- **`profile/README.md`**: the organization profile shown at [github.com/StuxAPIs](https://github.com/StuxAPIs):
  the services, templates and discontinued projects, the live status badge, contact details and activity.
- **`CONTRIBUTING.md`**: the default contributing guidelines. GitHub shows it on any public StuxAPIs repository
  that has no `CONTRIBUTING.md` of its own.
- **`.github/workflows/generateMetrics.yml`**: builds the profile's activity card (`stats.svg`, plus the
  `notable_*` cards) daily and on every push to `main`, onto the orphan `metrics` branch. It needs a
  `METRICS_TOKEN` secret.
- **`commit.sh` / `commit.bat`** and **`tests/version.sh`**: the release flow (see [Versioning](#versioning)).

## File Structure

```
.github/
├── .github/workflows/
│   └── generateMetrics.yml   # Profile activity cards, onto the metrics branch
├── profile/
│   └── README.md             # The organization profile
├── tests/
│   └── version.sh            # Checks VERSION.md against CHANGELOG.md
├── CHANGELOG.md
├── CONTRIBUTING.md           # Default contributing guidelines
├── VERSION.md
├── commit.sh / commit.bat    # Commit and tag a release
└── LICENSE
```

When you add, rename or retire a StuxAPIs service, update the tables in `profile/README.md` to match
[services.stuxapis.net](https://services.stuxapis.net).

## Contributing

We welcome contributions! Please refer to our [Contributing Guidelines](CONTRIBUTING.md) for details on how to participate in improving our organization's standards.

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

Releases are committed and tagged on the `test` branch and reach `main` through a pull request from `test`, which needs CI to pass and is reviewed and merged by Leo; see [Branches](CONTRIBUTING.md#branches).

## License

MIT — see [LICENSE](LICENSE).

## Copyright

(C) 2026 Stux Group Ltd. All rights reserved.

---

*Built & Maintained by <img src="https://global.media.stuxapis.net/icon.png" height="14" alt="StuxAPIs" valign="middle"> [StuxAPIs](https://github.com/StuxAPIs), Hosted by <img src="https://github.com/Stuxedo.png" height="14" alt="Stuxedo" valign="middle"> [Stuxedo](https://stuxedo.com).    
StuxAPIs is a part of the <img src="https://global.media.stux.group/icon.png" height="14" alt="Stux.Group" valign="middle"> Stux.Group brand of businesses.*
