# Prettier Configuration

This project uses [Prettier](https://prettier.io/) to enforce consistent code formatting across all files.

## Configuration

The Prettier configuration is defined in `.prettierrc.json` with the following rules:

- **Semicolons**: Enabled (`semi: true`)
- **Trailing Commas**: ES5 compatible (`trailingComma: "es5"`)
- **Single Quotes**: Enabled (`singleQuote: true`)
- **Print Width**: 80 characters (`printWidth: 80`)
- **Tab Width**: 2 spaces (`tabWidth: 2`)
- **Use Tabs**: Disabled (`useTabs: false`)

## Usage

### Format all files

To format all files in the project according to the Prettier configuration:

```bash
npx prettier . --write
```

### Check formatting

To check if files are formatted correctly without making changes:

```bash
npx prettier . --check
```

### Format specific files

To format specific files:

```bash
npx prettier path/to/file.js --write
```

## Integration with VS Code

To automatically format files on save in VS Code:

1. Install the [Prettier VS Code extension](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
2. Add the following to your VS Code settings:

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
}
```

## Ignored Files

Files and directories listed in `.prettierignore` will be skipped during formatting. This includes:

- `node_modules/`
- `dist/`, `build/`, `.out/`
- Log files (`*.log`)
- OS generated files (`.DS_Store`, `Thumbs.db`)
- Git files (`.git/`)

## Package Scripts

The following npm scripts are available for convenience:

- `npm run format`: Format all files
- `npm run format:check`: Check formatting of all files
