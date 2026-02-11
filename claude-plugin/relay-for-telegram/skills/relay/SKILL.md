# Relay for Telegram

Search, summarize, and analyze your Telegram message history using AI. This skill connects to a user's synced Telegram data via the Relay MCP server.

## When to Use

Use this skill whenever the user's request involves their Telegram messages:

- Searching messages, chats, DMs, groups, or channels
- Finding something someone said in a conversation
- Summarizing or recapping a conversation
- Extracting action items, decisions, or follow-ups
- Answering questions like "what did X say?", "who mentioned Y?"
- Reviewing or catching up on conversations

## Available MCP Tools

| Tool | Description | Parameters |
|------|-------------|------------|
| `search_messages` | Search synced Telegram messages by keyword | `query` (required), `chatId` (optional), `limit` (optional) |
| `list_chats` | Get a list of all synced Telegram chats | None required |
| `get_chat_messages` | Retrieve messages from a specific chat | `chatId` (required), `limit` (optional), `before` (optional) |

## Privacy & Data Access

- **Read-only access.** The MCP server can only search and read synced messages — it cannot send messages, delete messages, or modify chats.
- **Previously synced data only.** Only messages that have been synced to Relay's database are accessible. The server does not have live, real-time access to Telegram.
- **You control what's synced.** Free users choose which chats (up to 3) to sync. Pro users get recently active chats synced automatically.
- **Encrypted at rest.** All messages use AES-256-GCM encryption. Data is decrypted only at the point of API response.

## Setup

Authentication happens automatically via OAuth 2.1 when you first use an MCP tool. You'll be prompted to log in with your Telegram phone number and verification code. No API keys to manage.

## Free Plan Limits

- 3 chats accessible
- 25 search results max
- 500 messages per chat

Upgrade to Pro at https://relayfortelegram.com/pricing for unlimited access.
