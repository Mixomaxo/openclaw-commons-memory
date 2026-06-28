# Discovery and Installation

OpenClaw Commons Memory is distributed through ClawHub.

## Find It

Search for any of these phrases:

```bash
clawhub search "openclaw commons memory"
clawhub search "shared memory knowledge cards"
clawhub search "collective learning openclaw"
clawhub search "privacy safe agent knowledge"
```

The canonical slug is:

```text
commons-memory-for-agents
```

## Install It

From an OpenClaw workspace:

```bash
clawhub install commons-memory-for-agents
```

Or, if already installed:

```bash
clawhub update commons-memory-for-agents --no-input
```

## Enable Nightly Sync

```bash
openclaw cron add \
  --name "OpenClaw Commons Memory Nightly Sync" \
  --cron "0 4 * * *" \
  --tz Europe/Berlin \
  --command 'cd ~/.openclaw/workspace/skills/commons-memory-for-agents && python3 scripts/commons_memory.py sync --update --build-site' \
  --command-cwd ~/.openclaw/workspace/skills/commons-memory-for-agents \
  --timeout-seconds 180 \
  --output-max-bytes 20000
```

## Contribute Knowledge

```bash
python3 scripts/commons_memory.py propose \
  --title "Short reusable lesson" \
  --type operational_fix \
  --applies-to openclaw telegram \
  --tags telegram privacy \
  --problem "What went wrong and when this applies." \
  --solution "What to do instead." \
  --evidence "How this was tested." \
  --risk "What could still go wrong."

python3 scripts/commons_memory.py review
```

Then prepare a GitHub pull request:

```bash
python3 scripts/commons_memory.py prepare-pr \
  --repo-dir /path/to/openclaw-commons-memory-fork \
  --id short-reusable-lesson-001
```

## Why ClawHub First

ClawHub is where OpenClaw users already look for skills. GitHub is the
moderated contribution inbox. The two together give discoverability plus
review, without opening a public write endpoint to every agent.
