# MemoryRelay Plugin Marketplace

A plugin marketplace for [Claude Code](https://claude.ai/code) providing persistent long-term memory via [MemoryRelay](https://memoryrelay.ai).

## Installation

1. Add the marketplace:
```
/plugin add-marketplace memoryrelay/memoryrelay-marketplace
```

2. Install the plugin:
```
/plugin install memoryrelay@memoryrelay
```

## Available Plugins

### memoryrelay

Seamless long-term memory for Claude Code. Automatically manages sessions, recalls relevant context, captures important information, and filters sensitive content.

**What it provides:**
- **4 Hooks** — SessionStart (auto-session), Stop (session cleanup), PreCompact (context rescue), PreToolUse (privacy filter)
- **1 Skill** — `memory-awareness` for intelligent auto-recall and auto-capture
- **20 Commands** — Full coverage of all 42 MemoryRelay MCP tools (memory, session, decision, pattern, entity, project, agent)
- **MCP Server** — Bundled `memoryrelay-mcp` configuration

**Requirements:**
- `memoryrelay-mcp` npm package installed globally (`npm install -g memoryrelay-mcp`)
- `MEMORYRELAY_API_KEY` environment variable set
- `jq` and `curl` available in PATH

## License

MIT
