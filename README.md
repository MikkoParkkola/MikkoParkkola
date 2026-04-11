# Open-Source Tools

```bash
brew tap MikkoParkkola/tap && brew install trvl axterminator mcp-gateway nab nowifi
```

| Tool | What it does |
|------|-------------|
| [trvl](https://github.com/MikkoParkkola/trvl) | AI travel agent -- flights, hotels, ferries, 33 MCP tools. Free, no API keys. |
| [axterminator](https://github.com/MikkoParkkola/axterminator) | macOS GUI automation -- 30 MCP tools, background interaction, audio/camera capture. |
| [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) | Universal MCP gateway -- single port for all MCP servers, ~95% context token savings. |
| [nab](https://github.com/MikkoParkkola/nab) | Token-optimized HTTP client for LLMs -- cookies, anti-bot, ASR, URL watching. |
| [nowifi](https://github.com/MikkoParkkola/nowifi) | Captive portal bypass -- one command, 27 techniques, auto-restores on Ctrl+C. |

## Wire into your AI agent

Claude Code / Cursor / OpenCode -- add to MCP config:

```json
{
  "mcpServers": {
    "trvl":          { "command": "trvl", "args": ["mcp", "serve"] },
    "axterminator":  { "command": "axterminator", "args": ["mcp", "serve"] },
    "nab":           { "command": "nab-mcp" },
    "gateway":       { "type": "http", "url": "http://localhost:39400/mcp" }
  }
}
```

Run `mcp-gateway` first, then point `gateway` at it to get all backends through 4 meta-tools.

## Links

- [Homebrew Tap](https://github.com/MikkoParkkola/homebrew-tap)
- [trvl](https://github.com/MikkoParkkola/trvl) -- [axterminator](https://github.com/MikkoParkkola/axterminator) -- [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) -- [nab](https://github.com/MikkoParkkola/nab) -- [nowifi](https://github.com/MikkoParkkola/nowifi)
