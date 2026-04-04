# yyl/dev-tools

Shared development image and VS Code workspace config for repos under `coding/`.

## Includes

- Python 3.12 on `python:3.12-slim-bookworm`
- Node.js and npm
- `uv`
- `git`
- Bash and common shell utilities
- `build-essential` and `pkg-config`

## Build

```bash
docker build -t yyl/dev-tools:latest .
```

Build from this folder:

```bash
cd ~/Documents\ \(local\)/coding/dev-tools
docker build -t yyl/dev-tools:latest .
```

## VS Code Workspace

This repo tracks a parent-level devcontainer and a multi-root workspace:

- `.devcontainer/devcontainer.json` uses `yyl/dev-tools:latest`
- `coding.code-workspace` starts with `digital-footprint-dump` and can be extended with more repos over time

Suggested flow:

1. Open `coding.code-workspace` in VS Code.
2. Run "Dev Containers: Reopen in Container".
3. Add more repo folders to the workspace as needed.
