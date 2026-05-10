# 🧱 Brick — Modular AI Coding Agent

> Snap extensions together like building blocks.

**Brick** is a modular AI coding agent built on the principle that every feature should be a pluggable extension. The base provides the core agent loop, file/shell/git tools, and the MCP-based extension system. Everything else snaps in as an extension.

## Repositories

| Repository | Description |
|-----------|-------------|
| [brick-base](https://github.com/brick-codeagent/brick-base) | Core agent runtime — CLI, agent loop, tool registry, MCP bridge |
| [brick-web-search](https://github.com/brick-codeagent/brick-web-search) | Extension: web search via DuckDuckGo |
| [brick-repomap](https://github.com/brick-codeagent/brick-repomap) | Extension: codebase mapping and symbol search |

## Architecture

```
User Input → CLI/REPL → Agent Loop → LLM API
                                      ↓
                            Tool Registry
                                      ↓
                    ┌── Built-in (file/shell/git)
                    ├── Extensions (via MCP Bridge)
                    └── Slash Commands
```

## Quick Start

```bash
# Install globally from GitHub
npm install -g github:brick-codeagent/brick-base

# Start coding
export BRICK_API_KEY="your-api-key"
brick
```

## Extensions

Extensions are MCP servers discovered from `~/.brick/extensions/` and `./extensions/`. Each extension is a process exposing tools via JSON-RPC over stdio.

```bash
brick install ./extension-web-search
brick install ./extension-repomap
```

## Contributing

See [CONTRIBUTING.md](https://github.com/brick-codeagent/.github/blob/main/CONTRIBUTING.md) for guidelines.

## License

All Brick projects are [MIT](https://opensource.org/licenses/MIT) licensed.