# ArruCamBot

Telegram bot for camera control, deployed on Heroku.

## Deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/proarru/ArruCamBot)

## Setup

1. Clone the repo:
   ```bash
   git clone https://github.com/proarru/ArruCamBot.git
   cd ArruCamBot
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set environment variables:
   ```bash
   export BOT_TOKEN="your_token"
   export API_ID="your_api_id"
   export API_HASH="your_api_hash"
   ```

4. Run:
   ```bash
   python app.py
   ```

## Heroku Deploy (manual)

```bash
heroku login
heroku create your-app-name
heroku config:set BOT_TOKEN="your_token"
heroku config:set API_ID="your_api_id"
heroku config:set API_HASH="your_api_hash"
git push heroku main
heroku ps:scale worker=1
heroku logs --tail
```

## Commands

| Command | Description |
|---------|-------------|
| `/start` | Start the bot |
| `/help`  | Show help |

(Update with your actual commands.)

## License

MIT
