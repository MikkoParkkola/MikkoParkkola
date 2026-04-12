# Developer Tools

Open-source and source-available CLI / MCP tools.

```bash
brew tap MikkoParkkola/tap && brew install trvl mcp-gateway nab nowifi
```

`axterminator` is macOS-only:

```bash
brew install axterminator
```

| Tool | License | Platform | What it does |
|------|---------|----------|--------------|
| [trvl](https://github.com/MikkoParkkola/trvl) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS, Linux | AI travel agent -- flights, hotels, ferries, 33 MCP tools. Free, no API keys. |
| [axterminator](https://github.com/MikkoParkkola/axterminator) | Open source (`MIT OR Apache-2.0`) | macOS | macOS GUI automation -- 30 MCP tools, background interaction, audio/camera capture. |
| [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) | Open source (`MIT`) | macOS, Linux | Universal MCP gateway -- single port for all MCP servers, ~95% context token savings. |
| [nab](https://github.com/MikkoParkkola/nab) | Open source (`MIT`) | macOS, Linux | Token-optimized HTTP client for LLMs -- cookies, anti-bot, ASR, URL watching. |
| [nowifi](https://github.com/MikkoParkkola/nowifi) | Open source (`GPL-3.0-only`) | macOS, Linux | Captive portal bypass -- one command, 27 techniques, auto-restores on Ctrl+C. |

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
