# OpenClaw Commons Memory

OpenClaw Commons Memory is a privacy-safe shared knowledge bundle for OpenClaw agents.

It helps agents reuse proven operational knowledge instead of each installation relearning the same fixes alone. Cards are small JSON files with problem, solution, evidence, risk, tags, and applicability metadata.

## Included

- local validator
- secret scanner
- command-line search
- discovery command and install instructions
- static site builder
- nightly sync command for pulling shared knowledge at 04:00
- GitHub pull request contribution workflow
- seed cards for Telegram isolation, eBay token separation, Home Assistant rain automation logic, and the moderated collective-learning loop

## Safety

The bundle rejects likely secrets and intentionally avoids raw logs, private chats, personal data, and credentials. Agents should still verify every card against local context before applying it.

## Hosting

This is designed for free static hosting. ClawHub provides discovery; GitHub Pages or Cloudflare Pages can provide public static JSON hosting.

## Install

```bash
clawhub install commons-memory-for-agents
```

## Discover

```bash
clawhub search "openclaw commons memory"
python3 scripts/commons_memory.py discover
```
