# SDD Workflows — VS Code Extension

Ambient workflow visualization for [SDD](https://github.com/sdd-engine) projects in Visual Studio Code.

## Features

- **Workflow Tree View**: See all active workflows in the activity bar
- **Status Bar**: Current workflow phase displayed at a glance
- **Lifecycle Stepper**: Visual progress through SDD phases (spec, plan, implement, verify)
- **Approval Notifications**: Get notified when a workflow needs your approval

## Installation

Install from the VS Code Marketplace or build from source:

```bash
npm install
npm run build
```

Then press `F5` in VS Code to launch the extension in development mode.

## How It Works

The extension watches for `sdd/workflows/` directories in your workspace and renders workflow state in real-time (with legacy `.sdd/` fallback). It reads `workflow.yaml` files and displays:

- Workflow name and ID
- Current phase (spec, plan, implement, verify)
- Change items and their status
- Phase gate requirements

## Requirements

- VS Code 1.96.0 or later
- An SDD project with `sdd/` directory (legacy `.sdd/` also supported)

## Documentation

- [Extension Architecture](docs/architecture.md)

## Lineage

Extracted from [LiorCohen/sdd](https://github.com/LiorCohen/sdd) v7.3.0 (`vscode-extension/`).

## License

MIT
