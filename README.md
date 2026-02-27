<p align="center">
  <h1 align="center">Oculo</h1>
  <p align="center"><strong>The AI Browser</strong></p>
  <p align="center">Give AI eyes to see and hands to interact with the web.</p>
  <p align="center">
    <code>Cursor:VSCode :: Oculo:Chrome</code>
  </p>
</p>

<p align="center">
  <a href="https://github.com/xidik12/oculo/releases/latest">Download</a> &bull;
  <a href="https://getoculo.com">Website</a> &bull;
  <a href="#mcp-setup">MCP Setup</a> &bull;
  <a href="#donate">Donate</a>
</p>

---

## What is Oculo?

Oculo is an AI-powered native browser built with Electron. It gives AI assistants like Claude the ability to see web pages and interact with them — click, type, fill forms, navigate, take screenshots, generate images, and more.

Think of it as **Cursor for your browser**.

## Features

- **AI Chat Panel** — Multi-provider support (Claude, OpenAI, Gemini, Grok, OpenClaw, Ollama)
- **MCP Tools** — 6 tools for Claude Code integration (~30 tokens per page description)
- **Media Generation** — Nano Banana images (Gemini), Veo 3.1 video, DALL-E 3
- **Smart Auth** — Credential vault (macOS Keychain), auto-login, TOTP 2FA
- **Privacy-First** — 4-tier permission gate, PII redaction, anti-injection, audit log
- **Voice Control** — Whisper STT for voice commands
- **Screenshots & Uploads** — Capture pages, generate images, upload programmatically

## Download

| Platform | Download |
|----------|----------|
| **macOS** (Apple Silicon) | [Oculo-0.1.0-arm64.dmg](https://github.com/xidik12/oculo/releases/latest) |

> Windows & Linux coming soon.

## MCP Setup

Connect Oculo to Claude Code so AI can control your browser:

1. **Download and launch Oculo**
2. **Install the MCP bridge:**

```bash
# Install the MCP SDK dependency
npm install -g @modelcontextprotocol/sdk

# Register with Claude Code
claude mcp add oculo -- node /path/to/mcp/oculo-mcp.mjs
```

3. **Start using it** — ask Claude Code to browse, fill forms, take screenshots, post on social media, and more.

### MCP Tools

| Tool | What it does | Tokens |
|------|-------------|--------|
| `page` | Describe current page (headings, forms, buttons, links) | ~30-80 |
| `act` | Navigate, click, type, scroll, screenshot, upload | ~1 line |
| `fill` | Fill form fields by label matching | ~1 line |
| `read` | Extract structured data (lists, tables, cards) | compact |
| `run` | Multi-step pipeline | header + last |
| `media` | Generate images/videos from text prompts | file path |

## Tech Stack

- Electron 34
- TypeScript
- React 19
- Tailwind CSS
- MCP SDK
- Whisper (voice)

## Donate

Oculo is free to use. If you find it useful, consider supporting development:

**Bitcoin (BTC):** `12yRGpUfFznzZoz4yVfZKRxLSkAwbanw2B`

Every contribution helps keep Oculo free for everyone.

## License

MIT &copy; 2026 Salakhitdinov Khidayotullo
