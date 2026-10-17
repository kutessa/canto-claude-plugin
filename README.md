# Canto for Claude Code

[Canto](https://usecanto.com) records your meetings and turns them into speaker-labelled transcripts and notes.
This plugin registers Canto's MCP server so Claude Code can search every note you can see, read transcripts
page by page, list recordings and folders, check your next meetings, update titles, tags and notes, and send
the notetaker to a call.

## Install

```sh
claude plugin marketplace add kutessa/canto-claude-plugin
claude plugin install canto@canto --scope user
```

Then start Claude Code and run `/mcp` to sign in to Canto (OAuth, no API keys). Try:

> search my Canto notes for what we decided about pricing, then read the top hit

## Without the plugin

```sh
claude mcp add --transport http canto https://mcp.usecanto.com/mcp
claude mcp login canto
```

## What it can and cannot do

Nine tools: seven read-only (`search`, `fetch`, `get_transcript`, `list_recordings`, `list_folders`,
`list_meetings`, `get_audio_url`) and two writes (`update_note` for title/tags/your notes; `send_notetaker`).
It never changes the AI summary and cannot delete, share or move recordings. Disconnect any time from
Settings → Connections in Canto.

Setup guide and details: https://usecanto.com/integrations/mcp/ · Privacy: https://usecanto.com/privacy/
