<h1 align="center">👁️ Agent Reach</h1>

<p align="center">
  <strong>Give Your AI Agent Internet Superpowers — One Command Away</strong>
</p>

<p align="center">
  The most stable integration method for AI agents. We pick the tools, install them, and test them for you — integration methods evolve, but you won't have to worry.
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.10+-green.svg?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.10+"></a>
  <a href="https://github.com/Panniantong/agent-reach/stargazers"><img src="https://img.shields.io/github/stars/Panniantong/Agent-Reach?style=for-the-badge" alt="GitHub Stars"></a>
  <a href="https://trendshift.io/repositories/24387"><img src="https://trendshift.io/api/badge/repositories/24387" alt="Trendshift GitHub Trending #1 Repository of the Day"></a>
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> · <a href="docs/README_zh.md">中文</a> · <a href="docs/README_ja.md">日本語</a> · <a href="docs/README_ko.md">한국어</a>
</p>

---

## Why You Need Agent Reach

AI agents can write code, edit documents, manage projects — but the moment you ask them to find something on the internet, they hit a wall:

- 📺 "Watch this YouTube tutorial and summarize it" → **Can't do it**, no subtitle access
- 🐦 "Search Twitter for reviews on this product" → **Can't do it**, Twitter API requires payment
- 📖 "Check Reddit for anyone with the same bug" → **403 Forbidden**, server IP rejected
- 📕 "Look up reputation on Red (XiaoHongShu)" → **Can't access**, login required
- 📺 "Summarize this Bilibili tech video" → **Can't download**, Bilibili blocks all standard tools
- 🔍 "Search the web for latest LLM framework comparisons" → **No good free option**, paid APIs suck
- 🌐 "Read what's on this webpage" → **Pulls raw HTML**, unreadable
- 📦 "What does this GitHub repo do?" → Works, but auth setup is painful
- 📡 "Subscribe to these RSS feeds and alert me on updates" → Requires writing custom code

**These aren't hard problems, but they require endless configuration.**

Every platform has its own barriers — paywalled APIs, anti-scraping measures, login walls, messy data formats. You end up spending hours finding tools, installing dependencies, tweaking configs. By the time your agent can read Twitter, search Reddit, and watch YouTube, you've lost a whole day to setup.

**Agent Reach makes it one line:**

```
Help me install Agent Reach: https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/install.md
```

Paste this into your AI agent (Claude Code, OpenClaw, Cursor, etc.), and in minutes it'll have the power to read Twitter, search Reddit, watch YouTube, and browse XiaoHongShu.

**Already installed? Updating is one line too:**

```
Help me update Agent Reach: https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/update.md
```

> ⭐ **Star this repo** and we'll keep tracking platform changes and adding new channels. We monitor the web so you don't have to — when platforms block us, we route around them. When new services launch, we add them.

### ✅ What You Should Know Before Using It

| Feature | Details |
|---------|---------|
| 💰 **100% Free** | All tools open-source, all APIs free. Only optional cost: server proxy (~$1/month); not needed for local machines |
| 🔒 **Privacy First** | Credentials stored locally only, never uploaded. Code fully open-source and auditable |
| 🔄 **Always Evolving** | Each platform has primary + fallback backends. When one breaks, we switch to the next seamlessly — you won't notice |
| 🤖 **Works Everywhere** | Claude Code, OpenClaw, Cursor, Windsurf — any agent that runs shell commands can use it |
| 🩺 **Self-Diagnosing** | `agent-reach doctor` tells you which channels work, which don't, and how to fix them |

---

## Supported Platforms

| Platform | Works Out-of-Box | Requires Config | How to Setup |
|----------|------------------|-----------------|-------------|
| 🌐 **Web** | Read any webpage | — | No setup needed |
| 📺 **YouTube** | Subtitles + video search | — | No setup needed |
| 📡 **RSS** | Parse any RSS/Atom feed | — | No setup needed |
| 🔍 **Global Search** | — | Semantic web search | Auto-setup (MCP, free) |
| 📦 **GitHub** | Read public repos + search | Private repos, Issues/PRs, Fork | Tell agent: "Help me set up GitHub" |
| 🐦 **Twitter/X** | Read single tweets | Search tweets, view timeline, read threads | Tell agent: "Help me set up Twitter" |
| 📺 **Bilibili** | Search + video info (no login needed) | Subtitles | Tell agent: "Help me set up Bilibili" |
| 📖 **Reddit** | — (no zero-config path) | Search + read posts/comments | Desktop: OpenCLI; Server: rdt-cli + Cookie |
| 📕 **XiaoHongShu** | — | Search, read, comments | Desktop: OpenCLI; Server: xiaohongshu-mcp |
| 💼 **LinkedIn** | Read public pages with Jina | Profile details, companies, job search | Tell agent: "Help me set up LinkedIn" |
| 💻 **V2EX** | Trending, threads, user info | — | No setup needed |
| 📈 **Snowball (Stock)** | Stock quotes, trending stocks | — | Tell agent: "Help me set up Snowball" |
| 🎙️ **Podcast** | — | Convert audio to transcripts (Whisper) | Tell agent: "Help me set up podcasts" |

> **Don't know how to configure something?** Don't read the docs. Just tell your AI agent "Help me set up XXX" and it'll guide you step-by-step.

---

## Quick Start

> ⚠️ **OpenClaw Users:** First ensure `exec` permissions are enabled.
>
> Agent Reach requires your agent to execute shell commands (`pip install`, `mcporter`, etc.). If your OpenClaw uses the default `messaging` tool profile, commands will fail.
>
> Enable it:
> ```bash
> openclaw config set tools.profile "coding"
> ```
> Or edit `~/.openclaw/openclaw.json` and set `"tools": { "profile": "coding" }`. Then restart your gateway and start a new chat. (Other platforms like Claude Code, Cursor, Windsurf don't have this restriction.)

**Copy this line to your AI agent:**

```
Help me install Agent Reach: https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/install.md
```

That's it. The agent handles everything else.

> 🔄 **Already installed?** Update with one line:
> ```
> Help me update Agent Reach: https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/update.md
> ```

> 🛡️ **Security-conscious?** Use safe mode — no automatic system packages, just recommendations:
> ```
> Help me install Agent Reach (safe mode): https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/install.md
> Use the --safe flag during installation
> ```

<details>
<summary>What happens during installation? (Click to expand)</summary>

1. **Installs CLI tools** — `pip install agent-reach` command + bundled tools (yt-dlp, feedparser)
2. **Sets up system foundation** — Auto-detects and installs Node.js, gh CLI, mcporter
3. **Configures search** — Connects to Exa semantic search via MCP (free, no API key)
4. **Detects environment** — Checks if it's a local machine or server, gives appropriate advice
5. **Registers SKILL.md** — Installs usage guide in your agent's skills directory so it automatically knows which tools to use for "web research", "search Twitter", "watch video" type requests
6. **Asks what else** — By default activates 6 zero-config channels; platforms like XiaoHongShu, Twitter, Reddit get added only if you ask

After setup, `agent-reach doctor` shows every channel's status and which backend it's currently using.
</details>

---

## Works Out-of-the-Box (No Config)

No setup required — just tell your agent:

- "Read this link for me" → `curl https://r.jina.ai/URL` reads any webpage
- "What does this GitHub repo do?" → `gh repo view owner/repo`
- "Summarize this YouTube video" → `yt-dlp` extracts subtitles
- "Search Bilibili for AI tutorials" → `bili search` (no login needed)
- "Search the web for LLM framework comparisons" → Exa semantic search
- "Subscribe to this RSS feed" → `feedparser` parses it

**Don't memorize commands.** After reading SKILL.md, your agent knows what to call. For login-required platforms (XiaoHongShu, Twitter, Reddit), just tell your agent "Help me set up XXX" to unlock them.

---

## Scope: Content Reading vs Browser Automation

Some tasks go beyond simple content reading: logged-in webpage interactions, form submissions, multi-account isolation, parallel browser sessions, login/auth/captcha handling in automation flows. These need **browser automation** (Selenium, Playwright), not just HTTP clients.

**Agent Reach focuses on:** Reading content, searching, extracting data.  
**Agent Reach doesn't do:** Interactive browsing, form filling, account management across multiple sessions.

For interactive tasks, use browser automation tools. Agent Reach gives you the data-reading foundation.

---

## Design Philosophy

**Agent Reach is a capability layer, not another tool.**

It sits above specific implementations — responsible for **selection, installation, health checks, routing** — not the core reading logic. Agents call upstream tools directly. There's no wrapper layer.

When setting up a new agent, you always waste time finding tools, installing deps, tweaking configs. Which tool for Twitter? How to log into Reddit? Did XiaoHongShu's CLI stop updating? Need a replacement? Every time you start from scratch.

### 🔌 Each Platform = Ordered List of Primary + Fallback Backends

Changing backends = reordering the list, not rewriting code. `agent-reach doctor` shows you which backend each platform currently uses.

```
channels/
├── web.py          → Jina Reader
├── twitter.py      → twitter-cli ▸ OpenCLI ▸ bird
├── youtube.py      → yt-dlp
├── github.py       → gh CLI
├── bilibili.py     → bili-cli ▸ OpenCLI ▸ Search API
├── reddit.py       → OpenCLI ▸ rdt-cli
├── xiaohongshu.py  → OpenCLI ▸ xiaohongshu-mcp ▸ xhs-cli
├── linkedin.py     → linkedin-mcp ▸ Jina Reader
├── rss.py          → feedparser
├── exa_search.py   → Exa via mcporter
└── __init__.py     → Channel registry (for doctor checks)
```

Each channel file **actively probes** candidate backends (not just checking if commands exist). The first fully-working option is selected; broken ones get repair instructions. Actual reading/searching is done by the agent calling upstream tools directly.

### Current Backend Selection

| Use Case | Primary | Fallback | Why This Choice |
|----------|---------|----------|-----------------|
| Read webpages | [Jina Reader](https://github.com/jina-ai/reader) | — | Free, no API key |
| Read Twitter | [twitter-cli](https://github.com/public-clis/twitter-cli) | [OpenCLI](https://github.com/jackwener/opencli) | Stable search; OpenCLI fallback uses browser auth |
| Reddit | [OpenCLI](https://github.com/jackwener/opencli) (desktop) | [rdt-cli](https://github.com/public-clis/rdt-cli) | Anonymous API blocked, official API requires approval — only auth path remains |
| YouTube subtitles + search | [yt-dlp](https://github.com/yt-dlp/yt-dlp) | — | 154K stars, best maintained; no longer used for Bilibili |
| Bilibili | [bili-cli](https://github.com/public-clis/bilibili-cli) | OpenCLI ▸ Search API | yt-dlp blocked by Bilibili (2026-06 confirmed); bili-cli works without login |
| Global web search | [Exa](https://exa.ai) via [mcporter](https://github.com/nicobailon/mcporter) | — | AI-powered semantic search, MCP integration, free with no key |
| GitHub | [gh CLI](https://cli.github.com) | — | Official tool, full API after auth |
| RSS | [feedparser](https://github.com/kurtmckee/feedparser) | — | Python ecosystem standard |
| XiaoHongShu | [OpenCLI](https://github.com/jackwener/opencli) (desktop) | [xiaohongshu-mcp](https://github.com/xpzouying/xiaohongshu-mcp) (server) ▸ xhs-cli | xhs-cli author moved to OpenCLI; server option available |
| LinkedIn | [linkedin-mcp](https://github.com/stickerdaniel/linkedin-mcp-server) | Jina Reader | MCP service with browser automation |

> 📌 These are "current selections" based on real-world testing. If a path breaks, we switch — `agent-reach doctor` always shows which backend is active right now.

---

## Security

Agent Reach prioritizes security by design:

| Measure | Details |
|---------|---------|
| 🔒 **Local Credential Storage** | Cookies, tokens stored only in `~/.agent-reach/config.yaml` with 600 file permissions (owner-only read/write). Never uploaded, never external. |
| 🛡️ **Safe Mode** | `agent-reach install --safe` won't auto-modify your system — just lists what's needed and lets you decide |
| 👀 **Fully Open Source** | Code is transparent and auditable. All dependencies are open-source projects. |
| 🔍 **Dry Run Mode** | `agent-reach install --dry-run` previews all operations without making changes |
| 🧩 **Pluggable Architecture** | Don't trust a component? Swap out its channel file — doesn't affect anything else |

### 🍪 Cookie Security Recommendations

> ⚠️ **Account Ban Risk:** Platforms using cookie auth (Twitter, XiaoHongShu) may detect and ban accounts using script/API calls. **Always use a dedicated secondary account**, not your main one.

For cookie-based platforms (Twitter, XiaoHongShu), use a **dedicated secondary account**. Two reasons:

1. **Ban Risk** — Platforms detect non-browser API calls and may restrict or ban the account
2. **Damage Control** — Cookies = full login access; using a secondary account limits exposure if credentials leak

### 📦 Installation Methods

| Method | Command | Best For |
|--------|---------|----------|
| Full Auto (Default) | `agent-reach install --env=auto` | Personal computers, dev environments |
| Safe Mode | `agent-reach install --env=auto --safe` | Production servers, shared machines |
| Preview Only | `agent-reach install --env=auto --dry-run` | See what would happen first |

### 🗑️ Uninstall

```bash
agent-reach uninstall
```

Removes: `~/.agent-reach/` (all tokens/cookies), skill files from agents, MCP config from mcporter.

```bash
# Preview without deleting
agent-reach uninstall --dry-run

# Keep config, remove only skill files (useful for reinstalls)
agent-reach uninstall --keep-config
```

Uninstall the Python package: `pip uninstall agent-reach`

---

## Contributing

This project was built with pure passion 🎸 and might have rough edges. We appreciate your patience with bugs. Found an issue? [File a GitHub Issue](https://github.com/Panniantong/agent-reach/issues).

**Want a new platform?** Create an Issue describing it, or submit a PR directly.

**Want to customize locally?** Have your agent clone the repo and modify. Each platform is just one file — adding a new one is straightforward.

[PRs welcome anytime!](https://github.com/Panniantong/agent-reach/pulls)

---

## ⭐ Why Star This Project

I use this every day, so it'll stay maintained.

- New requests or community-requested channels get added progressively
- Every channel aims to be **working, useful, and free**
- When platforms change anti-scraping measures or APIs break, we find a workaround

Contributing to Web 4.0 infrastructure. Give us a star so you can find it next time you need it. ⭐

---

## FAQ / Frequently Asked Questions

<details>
<summary><strong>How do I search Twitter/X with my AI agent for free (no API fees)?</strong></summary>

Agent Reach uses [twitter-cli](https://github.com/public-clis/twitter-cli) with cookie auth — completely free. Install with `pipx install twitter-cli`, make sure you're logged into x.com in your browser, then your agent can search with `twitter search "query"`.
</details>

<details>
<summary><strong>I get 403 errors from Reddit. How do I fix it?</strong></summary>

Reddit requires authentication for all access (anonymous API fully blocked, official API requires manual approval). Desktop: use **OpenCLI** — if you've browsed reddit.com in your browser, it'll work directly. Server: use OpenCLI or rdt-cli with saved cookies.
</details>

<details>
<summary><strong>How do I extract YouTube video transcripts for my AI?</strong></summary>

Use `yt-dlp --dump-json "https://youtube.com/watch?v=xxx"` to get metadata, or `yt-dlp --write-sub --skip-download "URL"` to extract subtitles. yt-dlp handles multiple subtitle languages and formats. Agent Reach wraps this for easy agent integration.
</details>

<details>
<summary><strong>How do I let my AI agent read XiaoHongShu content?</strong></summary>

Desktop: **OpenCLI** is the top choice (`agent-reach install --channels opencli`) — it reuses your browser's login session. If you've been browsing XiaoHongShu, it works instantly with zero config. Just install from the Chrome Web Store and you're done.
</details>

<details>
<summary><strong>Does this work with Claude Code / Cursor / OpenClaw / Windsurf?</strong></summary>

Yes! Agent Reach is an installer + config tool — any agent that runs shell commands works with it. Tested and working on Claude Code, Cursor, OpenClaw, Windsurf, Codex, and more. Installation: `pip install agent-reach` and you're done.

**Note for OpenClaw users:** If using the default `messaging` tool profile, shell execution is disabled. Enable coding first: `openclaw config set tools.profile "coding"` (see Quick Start section).
</details>

<details>
<summary><strong>Is this really free? Any hidden API costs?</strong></summary>

100% free. All backends are open-source tools (OpenCLI, twitter-cli, bili-cli, rdt-cli, yt-dlp, Jina Reader, Exa, xiaohongshu-mcp) that don't require paid API keys. The only optional expense: server-side HTTP proxy (~$1/month) if deploying on a server; local machines don't need it.
</details>

---

## Acknowledgments

[OpenCLI](https://github.com/jackwener/opencli) · [twitter-cli](https://github.com/public-clis/twitter-cli) · [rdt-cli](https://github.com/public-clis/rdt-cli) · [xiaohongshu-mcp](https://github.com/xpzouying/xiaohongshu-mcp) · [yt-dlp](https://github.com/yt-dlp/yt-dlp) · [Jina Reader](https://github.com/jina-ai/reader) · [Exa](https://exa.ai) · [feedparser](https://github.com/kurtmckee/feedparser) · [gh CLI](https://cli.github.com) · [bili-cli](https://github.com/public-clis/bilibili-cli)

## Contact

- 📧 **Email:** pnt01@foxmail.com
- 🐦 **Twitter/X:** [@Neo_Reidlab](https://x.com/Neo_Reidlab)

---

## License

[MIT](LICENSE)

## Helpful Resources

- **Ark Agent Plan (Doubao)** — Subscribe to Bytedance AI models including Doubao-Seed with integrated Agent Reach
- **Tencent Cloud OpenClaw** — Deploy OpenClaw on Lighthouse with one click, compose Agent Reach into conversations seamlessly
- **AtomGit Mirror** — Agent Reach synchronized mirror on AtomGit for faster access in mainland China

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Panniantong/Agent-Reach&type=Date&v=20260309)](https://star-history.com/#Panniantong/Agent-Reach&Date)
