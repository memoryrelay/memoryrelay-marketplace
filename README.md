# MemoryRelay Plugin Marketplace

A plugin marketplace for [Claude Code](https://claude.com/claude-code) providing persistent context and memory via [MemoryRelay](https://memoryrelay.ai).

## Installation

```bash
claude plugin marketplace add memoryrelay/memoryrelay-marketplace
claude plugin install memoryrelay@memoryrelay
```

Inside a session: `/plugin marketplace add memoryrelay/memoryrelay-marketplace`, then `/plugin install memoryrelay@memoryrelay`.

## Available plugins

### memoryrelay

Source: [`memoryrelay/api` → `plugins/memoryrelay`](https://github.com/memoryrelay/api/tree/main/plugins/memoryrelay) (this marketplace lists it; it no longer carries a copy).

- **Hooks**: SessionStart (the repository's bound ICM context through `icm_context_for`, then `memory_search` in the repository's namespace), Stop (asks once per context receipt for `icm_report_reads` and `icm_report_outcome`), PreToolUse (privacy filter on `memory_store` and `memory_update`). Node scripts, so they run on Windows, macOS and Linux.
- **Skill**: `memory-awareness`.
- **Commands**: `/memoryrelay:memory-search`, `memory-store`, `memory-list`, `memory-get`, `memory-update`, `memory-delete`, `memory-entity`, `memory-agent`, `memory-health`, `icm-context`, `icm-search`, `icm-report`.
- **MCP server**: the remote server `https://api.memoryrelay.net/mcp` (Streamable HTTP).

**Requirements**: `MEMORYRELAY_API_KEY` set where Claude Code starts (scopes `icm:context`, `icm:observe`, `read`, `write`), and Node.js on the `PATH`. Docs: [Connect an agent](https://docs.memoryrelay.ai/connect-an-agent#the-claude-code-plugin).

## License

MIT
