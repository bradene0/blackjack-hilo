# Contributing

Contributions are welcome.

Hi-Lo Trainer is intentionally maintained as a single-file application. Before opening a pull request, please read `ADR-001-single-file-architecture.md`.

## Rules

- Keep the application in `index.html`.
- Do not add a framework.
- Do not add a build step.
- Do not add runtime dependencies.
- Keep the GitHub Pages deployment working.
- Run `hiloSelfCheck()` after changes to game or strategy logic.
- Test changes in a browser before submitting them.
- Keep changes focused and reasonably small.

Bug fixes, strategy corrections, accessibility improvements, training improvements, insults, and browser compatibility fixes are all welcome.

If your contribution requires splitting up `index.html`, the pull request will automatically be closed.
