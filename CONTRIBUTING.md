# Contributing to StuxAPIs

Thank you for your interest in contributing to StuxAPIs projects! We welcome contributions from everyone and appreciate your effort in helping us improve.

## Getting Started

1. **Fork the repository** you want to contribute to.
2. **Clone your fork** locally and create a new branch for your changes.
3. **Make your changes**, ensuring they follow the guidelines below.
4. **Submit a pull request** with a clear description of what you've changed and why.

## Code of Conduct

By participating in any StuxAPIs project, you agree to uphold our community standards. We expect all contributors to be respectful, constructive, and inclusive in all interactions.

## How to Contribute

### Reporting Bugs

- Check existing issues to avoid duplicates before opening a new one.
- Provide a clear title and description, steps to reproduce, and the expected vs. actual behaviour.
- Include your environment details (OS, language/runtime version, etc.) where relevant.

### Suggesting Features

- Open an issue with the label `enhancement` and describe your idea clearly.
- Explain the problem it solves and any alternatives you've considered.

### Submitting Pull Requests

- Keep pull requests focused — one change or fix per PR.
- Write clear, descriptive commit messages.
- Update documentation if your change affects behaviour or usage.
- Ensure your changes do not break existing functionality.
- Link any related issues in your pull request description.

## Style Guidelines

- Follow the coding conventions already present in the repository.
- Keep code clean, readable, and well-structured.
- Avoid introducing unnecessary dependencies.

## Questions

If you have any questions, feel free to reach out at [hello@stuxapis.net](mailto:hello@stuxapis.net) or open a discussion in the relevant repository.

We appreciate every contribution, no matter how small. Thank you for helping make StuxAPIs better!

## Branches and going live

- **`main` is what's live.** Nothing is pushed to it directly: it only changes when a pull request from `staging` is merged. The organization profile updates when the pull request is merged.
- **`staging` is the last check before live.** It only changes when a pull request from `test` is merged.
- **Work happens on `test`**, or on a branch off `test` that's merged back into it. Releases are committed and tagged on `test`; `commit.sh` / `commit.bat` refuse to run on `staging` or `main`.
- **Going live:** push `test` with its tag (`git push origin test --tags`), open a pull request into staging (`gh pr create --base staging --head test`), check staging once it's merged, then open one from staging into main (`gh pr create --base main --head staging`). Both pull requests need CI to pass and are reviewed and merged by Leo.

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.

---

*StuxAPIs is part of the [Stux.Group](https://github.com/StuxGroup) Brand of Companies.*
