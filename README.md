# Tools for AI agents and everyday use

Open-source and source-available tools. Most are MCP servers you can wire straight into an agent. A few run entirely on their own, no AI required.

I build these mostly for the fun of it: small, sharp tools for my own workflows, released once they are useful enough that someone else might want them too.

```bash
brew tap MikkoParkkola/tap && brew install trvl mcp-gateway nab nowifi
```

`axterminator` is macOS-only:

```bash
brew install axterminator
```

## No AI needed

Some of these are just good standalone tools:

- **Stuck behind a hotel or airport wifi login?** [nowifi](https://github.com/MikkoParkkola/nowifi) — one command and you are online.
- **A page your translator gives up on?** [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension) — translates the pages Google Translate and built-in browser translators fail on, and can run on-device so nothing leaves your browser.
- **Planning a trip?** [trvl](https://github.com/MikkoParkkola/trvl) — flights, hotels, trains, ferries, price alerts. No API keys.

## Start with the right repo

- **One endpoint for many AI tools:** [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway)
- **Travel search and trip planning:** [trvl](https://github.com/MikkoParkkola/trvl)
- **Authenticated web fetch, local transcription, or URL watching:** [nab](https://github.com/MikkoParkkola/nab)
- **macOS GUI automation:** [axterminator](https://github.com/MikkoParkkola/axterminator)
- **Captive portal bypass:** [nowifi](https://github.com/MikkoParkkola/nowifi)
- **Cut your Claude Code token bill:** [glyphdown](https://github.com/MikkoParkkola/glyphdown)
- **Translate the pages other translators fail on, privately:** [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension)
- **Stop your prose reading like a bot wrote it:** [anti-ai-tell](https://github.com/MikkoParkkola/anti-ai-tell)

| Tool | License | Platform | What it does |
|------|---------|----------|--------------|
| [trvl](https://github.com/MikkoParkkola/trvl) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS, Linux | Travel search and planning -- flights, hotels, trains, ferries, price alerts. One smart `travel` tool + 66 aliases, no API keys. |
| [axterminator](https://github.com/MikkoParkkola/axterminator) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS | macOS GUI automation -- 30 tools, background interaction, audio/camera capture. |
| [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) | Dual-license (`MIT` + `PolyForm NC` EE modules) | macOS, Linux | Universal MCP gateway -- single endpoint, fixed small tool surface, many backends. |
| [nab](https://github.com/MikkoParkkola/nab) | Mixed per-file (`MIT` + `PolyForm-NC`) | macOS, Linux | Token-lean web fetch for LLMs -- cookies, anti-bot reach, transcription, URL watching. |
| [nowifi](https://github.com/MikkoParkkola/nowifi) | Open source (`AGPL-3.0-only`) | macOS, Linux | Captive portal bypass -- one command, 27 techniques, auto-restores on Ctrl+C. |
| [glyphdown](https://github.com/MikkoParkkola/glyphdown) | Source-available (`PolyForm-Noncommercial-1.0.0`) | macOS, Linux | Token-cost reduction for Claude Code -- lossless output compression, context dedup, stacks on prompt caching. |
| [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension) | Open source (`GPL-3.0-or-later`) | Chrome, Firefox | Full-page translation -- 10+ providers. Handles pages built-in translators fail on; optional on-device model keeps your data off third-party servers. |
| [anti-ai-tell](https://github.com/MikkoParkkola/anti-ai-tell) | Open source (`MIT`) | Any AI client | Writing discipline for AI-assisted prose -- prompt constraints, linter, judgment checklist. |

## Install with your AI agent

Most of these install and wire themselves. Point your agent (Claude Code, Cursor, Windsurf, Codex, or anything with terminal access) at a repo and let it do the work:

> Read https://github.com/MikkoParkkola/trvl and install it for me.

Swap the URL for any tool on this page. Your agent reads that repo's README, installs the binary, sets up the connection, and verifies it. Usually under a minute.

**Install the whole set in one prompt:**

> Install these tools for me. For each one, read the repo's README first, then follow its setup steps: github.com/MikkoParkkola/trvl, github.com/MikkoParkkola/mcp-gateway, github.com/MikkoParkkola/nab, github.com/MikkoParkkola/nowifi, github.com/MikkoParkkola/axterminator, github.com/MikkoParkkola/glyphdown

**Rather do it by hand?** Each repo's README has copy-paste commands. To use `mcp-gateway` as a single front door for everything, the client entry is:

```json
{
  "mcpServers": {
    "gateway": { "type": "http", "url": "http://localhost:39400/mcp" }
  }
}
```

## Links

- [Homebrew Tap](https://github.com/MikkoParkkola/homebrew-tap)
- [trvl](https://github.com/MikkoParkkola/trvl) -- [axterminator](https://github.com/MikkoParkkola/axterminator) -- [mcp-gateway](https://github.com/MikkoParkkola/mcp-gateway) -- [nab](https://github.com/MikkoParkkola/nab) -- [nowifi](https://github.com/MikkoParkkola/nowifi) -- [glyphdown](https://github.com/MikkoParkkola/glyphdown) -- [translate-browser-extension](https://github.com/MikkoParkkola/translate-browser-extension) -- [anti-ai-tell](https://github.com/MikkoParkkola/anti-ai-tell)
