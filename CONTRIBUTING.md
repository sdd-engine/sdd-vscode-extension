# Contributing to SDD VS Code Extension

## Development Setup

```bash
git clone https://github.com/sdd-engine/sdd-vscode-extension.git
cd sdd-vscode-extension
npm install
npm run build
```

Then press `F5` in VS Code to launch the Extension Development Host.

## Making Changes

1. Create a feature branch: `git checkout -b feature/my-change`
2. Make changes in `src/` or `webview/`
3. Test in the Extension Development Host (`F5`)
4. Update `package.json` version if needed
5. Open a pull request

## Build Commands

```bash
npm run build
```

## Versioning

Version is tracked in `package.json` under `version`.

- **PATCH** (x.x.Z): Bug fixes, small improvements
- **MINOR** (x.Y.0): New features, backwards compatible
- **MAJOR** (X.0.0): Breaking changes

**Version bump required for:** changes under `src/`, `webview/`, `package.json`

**No version bump for:** `README.md`, `CLAUDE.md`, `CONTRIBUTING.md`, `docs/`

## Changelog

Use `CHANGELOG.md` with format:

```markdown
## [x.y.z] - YYYY-MM-DD

### Added
- New feature description

### Fixed
- Bug fix description

### Changed
- Change description
```

One commit = one changelog entry.

## Commit Message Format

```
[Action] [Component]: [Description]

[Optional detailed explanation]

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>
```

**Actions:** Add, Fix, Update, Remove, Refactor, Docs

## Packaging

```bash
npm run package  # Creates .vsix file
```

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
