# Developer Tools

Open-source and source-available CLI / MCP tools.

I build these mostly for the fun of it: small, sharp tools for my own agent workflows, released when they are useful enough that someone else might want them too.

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
- **Cut your Claude Code token bill:** [glyphdown](https://github.com/MikkoParkkola/glyphdown)
- **Translate any web page, offline if you want:** [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension)
- **Stop your prose reading like a bot wrote it:** [anti-ai-tell](https://github.com/MikkoParkkola/anti-ai-tell)

| Tool | License | Platform | What it does |
|------|---------|----------|--------------|
| [trvl](https://github.com/MikkoParkkola/trvl) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS, Linux | AI travel agent -- flights, hotels, ferries, 57 MCP tools. Free, no API keys. |
| [axterminator](https://github.com/MikkoParkkola/axterminator) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS | macOS GUI automation -- 30 MCP tools, background interaction, audio/camera capture. |
| [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) | Dual-license (`MIT` + `PolyForm NC` EE modules) | macOS, Linux | Universal MCP gateway -- single endpoint, fixed small tool surface, many backends. |
| [nab](https://github.com/MikkoParkkola/nab) | Mixed per-file (`MIT` + `PolyForm-NC`) | macOS, Linux | Token-optimized HTTP client for LLMs -- cookies, anti-bot, ASR, URL watching. |
| [nowifi](https://github.com/MikkoParkkola/nowifi) | Open source (`AGPL-3.0-only`) | macOS, Linux | Captive portal bypass -- one command, 27 techniques, auto-restores on Ctrl+C. |
| [glyphdown](https://github.com/MikkoParkkola/glyphdown) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS, Linux | Token-cost reduction for Claude Code -- lossless output compression, context dedup, stacks on prompt caching. |
| [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension) | Open source (`GPL-3.0-or-later`) | Chrome, Firefox | Full-page translation -- 10+ providers, including local offline models via WebAssembly. |
| [anti-ai-tell](https://github.com/MikkoParkkola/anti-ai-tell) | Open source (`MIT`) | Any AI client | Writing discipline for AI-assisted prose -- prompt constraints, linter, judgment checklist. |

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
- [trvl](https://github.com/MikkoParkkola/trvl) -- [axterminator](https://github.com/MikkoParkkola/axterminator) -- [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) -- [nab](https://github.com/MikkoParkkola/nab) -- [nowifi](https://github.com/MikkoParkkola/nowifi) -- [glyphdown](https://github.com/MikkoParkkola/glyphdown) -- [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension) -- [anti-ai-tell](https://github.com/MikkoParkkola/anti-ai-tell)
