# Contributing to SDD VS Code Extension

## Development Setup

```bash
git clone https://github.com/sdd-engine/sdd-vscode-extension.git
cd sdd-vscode-extension
npm install
npm run compile
```

Then press `F5` in VS Code to launch the Extension Development Host.

## Making Changes

1. Create a feature branch: `git checkout -b feature/my-change`
2. Make changes in `src/` or `webview/`
3. Test in the Extension Development Host (`F5`)
4. Update `package.json` version if needed
5. Open a pull request

## Packaging

```bash
npm run package  # Creates .vsix file
```

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
