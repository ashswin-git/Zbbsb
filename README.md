# Telegram Forward Bot (Render edition)

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![Telethon](https://img.shields.io/badge/Telethon-1.42-26A5E4?logo=telegram&logoColor=white)

A Telegram forward/ads bot (v4.1) tuned for deployment on Render's free tier.

## Features

- Bot commands: `/start`, `/help`, `/cancel`, `/myid`
- Config read from environment variables
- Session string stored in env so it survives redeploys
- SQLite database in `/tmp` (Render's disk is ephemeral)
- Flood-wait handling

## Built with

- **Language:** Python 3.10+
- **Libraries:** [Telethon](https://github.com/LonamiWebs/Telethon), cryptography, pyaes, rsa (pyaudio optional)
- **Storage:** SQLite
- **Deployment:** Render background worker (`render.yaml`)

## Getting started

```bash
git clone https://github.com/ashswin-git/Zbbsb.git
cd Zbbsb
pip install -r requirements.txt
export API_ID=... API_HASH=... BOT_TOKEN=... ADMIN_ID=...
python bot.py
```

> **Security note:** configure `API_ID`, `API_HASH`, `BOT_TOKEN` and `ADMIN_ID` through environment variables. Never commit real credentials.
