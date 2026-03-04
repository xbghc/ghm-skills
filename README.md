# ghm-skills

Personal Claude Code plugin — a collection of skills for UI design and frontend development workflows.

## Skills

### stitch-ui

UI design skill powered by Stitch MCP. Two-phase delivery: generate screenshots for review first, then produce code verified by Playwright.

- Generate UI designs from natural language descriptions
- Manage Stitch projects and screens via `.stitch/stitch.json`
- Maintain visual consistency across pages with `.stitch/DESIGN.md`
- Verify generated code against approved designs using Playwright

## Installation

```
/plugin install ghm-skills@claude-plugin-directory
```

Or install directly from this repository:

```
claude --plugin-dir /path/to/ghm-skills
```

## Requirements

- [Stitch MCP Server](https://stitch.withgoogle.com/)
- [Playwright MCP Server](https://github.com/anthropics/mcp-playwright)

## License

MIT
