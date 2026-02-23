# Extension Architecture

## Overview

The SDD Workflows extension provides ambient visualization of SDD workflow state in VS Code.

## Components

### Extension Host (`src/`)

- **extension.ts**: Activation, registration of providers and watchers
- **views/**: `TreeDataProvider` (workflow-tree.ts), status bar (status-bar.ts), lifecycle webview (lifecycle-webview.ts)
- **notifications/**: Approval gate notification handlers
- **workflow-parser.ts**: Parses workflow YAML files into typed state
- **workflow-watcher.ts**: `FileSystemWatcher` for `.sdd/workflows/` and `sdd/workflows/` directories
- **types.ts**: Shared type definitions (workflow state, phases, changes)

### Webview (`webview/`)

- Lifecycle stepper panel rendered as a VS Code webview
- Shows visual progress through SDD phases
- Communicates with extension host via message passing

### Media (`media/`)

- SVG icons for activity bar and tree view items
- Phase-specific icons (spec, plan, implement, verify)

## Data Flow

1. `FileSystemWatcher` detects changes to workflow YAML files
2. Parser reads and validates workflow state
3. `TreeDataProvider` transforms state into tree items
4. Status bar updates with current phase
5. Webview receives state updates via `postMessage`

## Activation

The extension activates on startup (`onStartupFinished`) and checks for SDD project markers (`.sdd/` or `sdd/` directories). If no SDD project is found, it shows a welcome message in the tree view.
