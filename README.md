# financehubapp
A self-hosted Slack bot that answers live QuickBooks Online questions (cash position, P&amp;L, balance sheet, AR/AP aging, and more) using Claude and Supabase Edge Functions. Each install uses your accounts only — no shared credentials. Clone or download the Release zip, run bash scripts/install.sh, and follow the instructions.

# QB Finance Slack Bot

Live QuickBooks Online finance bot for Slack — ask P&L, cash, AR/AP, and get scheduled digests. Self-install with **your own** Supabase, Slack, Anthropic, and Intuit credentials.

Nothing in this repo contains the author’s API keys or company data. Each install is fully separate.

## What it does

- Answer live QuickBooks questions in Slack (`@bot what’s our cash position?`)
- Pull P&L, Balance Sheet, Cash Flow, AR/AP aging, customer/vendor data (read-only)
- Optional scheduled digests (daily / weekly / monthly) via Supabase cron
- Cash-basis reports by default (configurable)

## Requirements

| Service | Purpose |
|---------|---------|
| [Supabase](https://supabase.com) | Edge Functions + Postgres |
| [Anthropic](https://platform.claude.com/settings/keys) | Claude answers |
| [Slack app](https://api.slack.com/apps) | Bot in your workspace |
| [Intuit QuickBooks](https://developer.intuit.com) | Live company data (accounting scope) |

## Quick start

### Option A — Download Release zip

1. Download the latest **Release** zip from this repo  
2. Unzip  
3. Run:

```bash
cd qb-finance-slack-bot
bash scripts/install.sh
