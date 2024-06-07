Here's the Markdown documentation for the "Send Info Telegram" GitHub Actions action:

---

# 📲 Send Info Telegram Action

This action sends workflow information via Telegram, allowing you to stay informed about your GitHub Actions workflows.

## Description

The "Send Info Telegram" action sends workflow details, such as repository, branch, workflow name, run ID, run number, and run attempt, via Telegram using specified parameters.

## Inputs

- `bot_token` (required): Telegram Bot Token.
- `chat_id` (required): Telegram Chat ID.
- `parse_mode` (optional): Parse mode for the message (default: Markdown).

## Usage

```yaml
name: Send Workflow Info

on:
  push:
    branches:
      - main

jobs:
  send-info-telegram:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2

      - name: Send Info Telegram
        uses: <username>/<repository>@<version>
        with:
          bot_token: ${{ secrets.TELEGRAM_BOT_TOKEN }}
          chat_id: ${{ secrets.TELEGRAM_CHAT_ID }}
          parse_mode: markdown
```

## Example

```yaml
- name: Send Info Telegram
  uses: <username>/<repository>@<version>
  with:
    bot_token: ${{ secrets.TELEGRAM_BOT_TOKEN }}
    chat_id: ${{ secrets.TELEGRAM_CHAT_ID }}
    parse_mode: markdown
```

---

Feel free to customize the message and integrate this action into your workflows to receive updates via Telegram! If you have any questions or need further assistance, feel free to ask.