# Relay for Telegram — Claude Code Plugin

Search, summarize, and analyze your Telegram message history directly from Claude.

## What it does

This plugin connects Claude to your synced Telegram messages via the [Relay](https://relayfortelegram.com) MCP server. Once connected, you can:

- Search across all your Telegram chats by keyword
- Summarize conversations or extract action items
- Retrieve messages from specific chats
- Answer questions about what was discussed and when

## Installation

```bash
/plugin install relay-for-telegram
```

## How it works

1. The plugin connects to Relay's MCP server at `https://relayfortelegram.com/mcp`
2. On first use, you'll be prompted to authenticate with your Telegram phone number via OAuth 2.1
3. After authentication, Claude can search and read your synced messages using MCP tools

No API keys to manage — authentication is handled automatically via OAuth.

## MCP Tools

| Tool | Description |
|------|-------------|
| `search_messages` | Search synced messages by keyword |
| `list_chats` | List all synced Telegram chats |
| `get_chat_messages` | Get messages from a specific chat |

## Privacy

- **Read-only** — cannot send, delete, or modify messages
- **Synced data only** — no live access to Telegram
- **Encrypted at rest** — AES-256-GCM encryption on all stored messages
- **User-controlled** — you choose which chats to sync

## Links

- Website: https://relayfortelegram.com
- Developer docs: https://relayfortelegram.com/developers
- Full SKILL.md: https://relayfortelegram.com/skill.md
