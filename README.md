<p align="center">
  <a href="https://bridgistic.app"><img src="https://bridgistic.app/assets/bridgistic-logo.png" alt="Bridgistic" width="420"></a>
</p>

<p align="center"><strong>Bridgistic for Claude and MCP marketplaces: safe AI control for WordPress, with scoped keys, signed requests, human approvals, snapshots and a full audit trail.</strong></p>

<p align="center">
  <a href="https://github.com/Wordpressistic/bridgistic-claude-marketplace/releases/latest"><img src="https://img.shields.io/github/v/release/Wordpressistic/bridgistic-claude-marketplace?label=release&color=2563eb" alt="Latest release"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-GPL--2.0--or--later-blue" alt="License: GPL-2.0-or-later"></a>
  <img src="https://img.shields.io/badge/WordPress-6.4%2B-21759b?logo=wordpress&logoColor=white" alt="WordPress 6.4+">
  <a href="https://www.npmjs.com/package/bridgistic-mcp-server"><img src="https://img.shields.io/npm/v/bridgistic-mcp-server?label=npm" alt="npm: bridgistic-mcp-server"></a>
</p>

<p align="center">
  <a href="https://bridgistic.app">Website</a> ·
  <a href="https://github.com/Wordpressistic/bridgistic-claude-marketplace/releases/latest">Download</a> ·
  <a href="https://github.com/Wordpressistic/bridgistic/blob/main/docs/CONNECT_BRIDGISTIC.md">Connection guide</a> ·
  <a href="https://github.com/Wordpressistic/bridgistic">Source repository</a>
</p>

---

This is the **official marketplace listing repository** for [Bridgistic](https://bridgistic.app). It holds the Claude Code plugin marketplace listing that `/plugin marketplace add Wordpressistic/bridgistic-claude-marketplace` installs from. Each listing sync here is a version snap of [Wordpressistic/bridgistic](https://github.com/Wordpressistic/bridgistic), the source repository of the WordPress plugin.

> Development, issues and pull requests live in **[Wordpressistic/bridgistic](https://github.com/Wordpressistic/bridgistic)**.

## What Bridgistic does

Bridgistic lets Claude, ChatGPT, OpenAI Codex, Gemini CLI or any other MCP client work on a WordPress site without an administrator password. You install the free WordPress plugin and create a least-privilege key. Every request is HMAC-signed and checked against that key's scopes. Destructive operations can be dry-run, held for your approval and snapshotted first, and every request is recorded in the audit log. The MCP server provides 54 tools for posts, media, users, plugins, options, files, the database, WooCommerce, playbooks, schedules and snapshots.

## Install

**First, the WordPress plugin.** Download `bridgistic-wordpress-plugin.zip` from the [latest release](https://github.com/Wordpressistic/bridgistic/releases/latest) or from [bridgistic.app](https://bridgistic.app). Upload it under **Plugins → Add New → Upload Plugin** and activate it. Then create a **Read-only** key under **Bridgistic → AI / MCP Connections**.

**Claude Desktop (one-click, no Node.js).** Download [`bridgistic.mcpb`](https://github.com/Wordpressistic/bridgistic/releases/latest/download/bridgistic.mcpb) and double-click it. When prompted, enter your site URL, Key ID and Secret.

**Claude Code (plugin marketplace).**

```text
/plugin marketplace add Wordpressistic/bridgistic-claude-marketplace
/plugin install bridgistic@bridgistic-marketplace
```

Then set `BRIDGISTIC_SITE_URL`, `BRIDGISTIC_KEY_ID` and `BRIDGISTIC_KEY_SECRET` in your environment.

**Other MCP clients.** Run `npx -y bridgistic-mcp-server` with the same three environment variables. Remote-only clients such as ChatGPT can connect through Bridgistic Cloud (public beta) from **WP Admin → Bridgistic → Bridgistic Cloud**.

Verify any client by asking it to run `bridgistic_get_site_info`.

## What's in this repository

| Path | Listing |
| --- | --- |
| [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) | Claude Code plugin marketplace (`bridgistic-marketplace`) |
| [`plugins/bridgistic`](plugins/bridgistic) | Claude Code plugin: bundled MCP server, example configs and install scripts |

## Free and Pro

The plugin and MCP server are free and open source. Bridgistic Pro is available on [bridgistic.app](https://bridgistic.app) as a $49.99 Lifetime Deal welcome offer (1 license, 1 site; until 31 December 2026, 100 licenses only), or for $12/month or $99/year (1 license, 5 sites), billed through Paddle. See the site for current pricing and terms.

## Support and security

- Questions and bugs: [Wordpressistic/bridgistic issues](https://github.com/Wordpressistic/bridgistic/issues)
- Security reports: **hello@insightistic.com** (see [SECURITY.md](SECURITY.md)); please don't open public issues for them
- Purchases and refunds: support@wpistic.com

## License

[GPL-2.0-or-later](LICENSE).

---

<p align="center">
  Built by <strong>WordPressistic LLC</strong>, 1209 Mountain Road PL NE, STE N, Albuquerque, NM 87110, United States<br>
  <a href="https://bridgistic.app">bridgistic.app</a> ·
  <a href="https://github.com/wordpressistic">GitHub</a> ·
  <a href="https://x.com/wordpressistic">X</a> ·
  <a href="https://www.linkedin.com/company/wordpressistic">LinkedIn</a> ·
  <a href="https://www.youtube.com/@wordpressistic">YouTube</a>
</p>
