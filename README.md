# Binovate

Real-time digit trading platform. Node.js backend, single-file frontend, Postgres persistence, Telegram bot for withdrawal approvals and referral system.

## Deploy

1. Free Postgres at https://neon.tech → copy connection string ending with `?sslmode=require`
2. Push this repo to GitHub
3. Render → New Web Service → connect repo
   - Environment: Node
   - Build: npm install
   - Start: node server.js
   - Free tier
4. Add env vars (see deploy table)
5. Open https://your-app.onrender.com/healthz — must show `"storage":"postgres"` and `"telegram":"yes"`

## Telegram bot

1. @BotFather → /newbot → token
2. Send any message to your bot
3. Visit https://api.telegram.org/bot<TOKEN>/getUpdates → copy chat id
4. Add TELEGRAM_BOT_TOKEN + TELEGRAM_CHAT_ID to Render env
5. Redeploy — webhook auto-registers

## Features

- Real-time digit trading (Even/Odd, Match/Differ, Over/Under)
- 5 volatility indices tick engine (1s)
- Auto-trading with TP/SL/Multiplier
- Smart Recovery mode
- Telegram withdrawal approval (✅ / ❌)
- Referral system (15% commission)
- Responsible Trading limits
- Account settings (password / email change)
- Light & dark theme
- PWA install support
- M-Pesa + USDT deposits
- Password reset via email
