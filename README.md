# Developer Tools

Open-source and source-available CLI / MCP tools.

```bash
brew tap MikkoParkkola/tap && brew install trvl mcp-gateway nab nowifi
```

`axterminator` is macOS-only:

```bash
brew install axterminator
```

## Start with the right repo

- **One MCP endpoint for many backends:** [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway)
- **Travel search and trip planning:** [trvl](https://github.com/MikkoParkkola/trvl)
- **Authenticated web fetch, local ASR, or URL watching:** [nab](https://github.com/MikkoParkkola/nab)
- **macOS GUI automation:** [axterminator](https://github.com/MikkoParkkola/axterminator)
- **Captive portal bypass:** [nowifi](https://github.com/MikkoParkkola/nowifi)

| Tool | License | Platform | What it does |
|------|---------|----------|--------------|
| [trvl](https://github.com/MikkoParkkola/trvl) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS, Linux | AI travel agent -- flights, hotels, ferries, 33 MCP tools. Free, no API keys. |
| [axterminator](https://github.com/MikkoParkkola/axterminator) | Open source (`MIT OR Apache-2.0`) | macOS | macOS GUI automation -- 30 MCP tools, background interaction, audio/camera capture. |
| [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) | Open source (`MIT`) | macOS, Linux | Universal MCP gateway -- single port for all MCP servers, ~95% context token savings. |
| [nab](https://github.com/MikkoParkkola/nab) | Open source (`MIT`) | macOS, Linux | Token-optimized HTTP client for LLMs -- cookies, anti-bot, ASR, URL watching. |
| [nowifi](https://github.com/MikkoParkkola/nowifi) | Open source (`GPL-3.0-only`) | macOS, Linux | Captive portal bypass -- one command, 27 techniques, auto-restores on Ctrl+C. |

## Wire into your AI agent

There are two good setup paths:

1. **Install tools directly into your MCP client** when you only need one or two servers:

   ```bash
   trvl mcp install --client claude-code
   nab mcp install --client claude-code
   axterminator mcp install --client claude-code   # macOS only
   ```

2. **Use `mcp-gateway` as the front door** when you want one endpoint for many tools:

   ```bash
   mcp-gateway setup wizard --configure-client
   mcp-gateway serve
   ```

If you prefer to edit config by hand, the gateway entry is:

```json
{
  "mcpServers": {
    "gateway": { "type": "http", "url": "http://localhost:39400/mcp" }
  }
}
```

Replace `claude-code` with your client where needed (`cursor`, `vscode`, `zed`, and others are supported in the individual repos).

## Links

- [Homebrew Tap](https://github.com/MikkoParkkola/homebrew-tap)
- [trvl](https://github.com/MikkoParkkola/trvl) -- [axterminator](https://github.com/MikkoParkkola/axterminator) -- [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) -- [nab](https://github.com/MikkoParkkola/nab) -- [nowifi](https://github.com/MikkoParkkola/nowifi)
