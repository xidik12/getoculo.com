<p align="center">
  <h1 align="center">Oculo</h1>
  <p align="center"><strong>The AI Browser That Sees the Web</strong></p>
  <p align="center">7 MCP tools. ~30 tokens per page. Works with any MCP client.</p>
  <p align="center">
    <code>Cursor:VSCode :: Oculo:Chrome</code>
  </p>
</p>

<p align="center">
  <a href="https://github.com/xidik12/getoculo.com/releases/download/v0.2.0/Oculo-0.2.0-arm64.dmg">Download</a> &bull;
  <a href="https://getoculo.com">Website</a> &bull;
  <a href="#mcp-setup">MCP Setup</a> &bull;
  <a href="#donate">Donate</a>
</p>

---

## What is Oculo?

Oculo is an AI-powered native browser built with Electron. It gives AI assistants the ability to see web pages and interact with them — click, type, fill forms, navigate, take screenshots, generate media, and more.

Works with **Claude Code, Cursor, Windsurf, Zed**, or any MCP-compatible client.

Think of it as **Cursor for your browser**.

## Features

- **AI Chat Panel** — Multi-provider support (Claude, OpenAI, Gemini, Grok, OpenClaw, Ollama)
- **7 MCP Tools** — Universal MCP integration (~30 tokens per page description)
- **Media Generation** — Nano Banana images, Veo 3.1 video
- **Smart Auth** — Credential vault (macOS Keychain), auto-login, TOTP 2FA
- **Privacy-First** — 4-tier permission gate, PII redaction, anti-injection, audit log
- **Voice Control** — On-device Whisper STT for voice commands
- **Shell** — Execute browser-side JavaScript, sandboxed and permission-gated

## Download

| Platform | Download |
|----------|----------|
| **macOS** (Apple Silicon) | [Oculo-0.2.0-arm64.dmg](https://github.com/xidik12/getoculo.com/releases/download/v0.2.0/Oculo-0.2.0-arm64.dmg) |
| **macOS** (Apple Silicon, zip) | [Oculo-0.2.0-arm64-mac.zip](https://github.com/xidik12/getoculo.com/releases/download/v0.2.0/Oculo-0.2.0-arm64-mac.zip) |

> Windows & Linux coming soon.

## MCP Setup

Connect Oculo to any MCP client:

### Claude Code
```bash
claude mcp add oculo -- node /path/to/mcp/oculo-mcp.mjs
```

### Cursor
Add to `.cursor/mcp.json`:
```json
{
  "mcpServers": {
    "oculo": {
      "command": "node",
      "args": ["/path/to/mcp/oculo-mcp.mjs"]
    }
  }
}
```

### Any stdio MCP Client
Point your client to `node /path/to/mcp/oculo-mcp.mjs` via stdio transport.

### MCP Tools

| Tool | What it does | Tokens |
|------|-------------|--------|
| `page` | Describe current page (headings, forms, buttons, links) | ~30 |
| `act` | Navigate, click, type, scroll, screenshot, login | ~10 |
| `fill` | Fill form fields by label matching | ~15 |
| `read` | Extract structured data (lists, tables, cards) | ~100 |
| `run` | Multi-step pipeline in a single call | ~200 |
| `media` | Generate images/videos from text prompts | varies |
| `shell` | Execute browser-side JavaScript (sandboxed) | ~50 |

## Tech Stack

- Electron 34
- TypeScript
- React 19
- Tailwind CSS
- MCP SDK
- Whisper (on-device voice)

## Donate

Oculo is free. If you find it useful, consider supporting development:

**Bitcoin (BTC):** `12yRGpUfFznzZoz4yVfZKRxLSkAwbanw2B`

## License

[MIT](LICENSE) &copy; 2026 Salakhitdinov Khidayotullo
