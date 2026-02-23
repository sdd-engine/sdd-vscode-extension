# CLAUDE.md

## Repository Structure

```
sdd-vscode-extension/
├── src/                           # Extension TypeScript source
│   ├── extension.ts               # Extension entry point
│   ├── providers/                  # Tree data providers
│   ├── watchers/                   # File system watchers
│   └── types/                     # Type definitions
├── webview/                       # Webview panel source (lifecycle stepper)
├── media/                         # Icons and images
├── dist/                          # Compiled output (gitignored)
├── package.json                   # Extension manifest
├── webpack.config.js              # Build configuration
├── tsconfig.json                  # Base TypeScript config
├── tsconfig.extension.json        # Extension-specific TS config
├── tsconfig.webview.json          # Webview-specific TS config
└── docs/                          # Documentation
```

## Build

```bash
npm install
npm run compile       # Build extension
npm run watch         # Watch mode for development
npm run package       # Create .vsix package
```

## Development

Press `F5` in VS Code to launch the Extension Development Host.

## Key Concepts

- Extension activates on startup (looks for `.sdd/` or `sdd/` directories)
- Uses `FileSystemWatcher` to track workflow file changes
- Tree view is the primary UI — shows workflows and their changes
- Status bar shows current phase of the active workflow
