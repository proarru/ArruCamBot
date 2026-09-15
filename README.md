```
    ___              ___         ______      __ 
   /   |  __________(_) /_  __   / ____/___ _/ /_
  / /| | / ___/ ___/ / __ \/ /  / /   / __ `/ __ \
 / ___ |/ /  / /  / / /_/ / /  / /___/ /_/ / /_/ /
/_/  |_/_/  /_/  /_/_.___/_/   \____/\__,_/_.___/ 

        [ ARRUCAMBOT // REMOTE SURVEILLANCE UNIT ]
        [ STATUS: ONLINE ]  [ MODE: STEALTH ]  [ AUTH: PROARRU ]
```

> "Some doors are better left closed. This one isn't."

---

## `> whoami`

**ArruCamBot** — ek Telegram-controlled remote camera bot.  
Heroku pe 24/7 chalta hai, commands receive karta hai, kaam karta hai, aur chup chaap so jata hai.

Built by **ProArru** · Telegram → [@Proarru](https://t.me/Proarru)

---

## `> cat features.txt`

```
[+] Telegram Bot control (remote commands)
[+] Camera access / capture
[+] Heroku deployment ready (24/7 uptime)
[+] Environment-variable based secrets
[+] Silent mode, no logs leaked
[+] Encrypted communication
```

---

## `> ls -la`

```text
ArruCamBot/
├── app.py              # main entry
├── requirements.txt    # deps
├── Procfile            # heroku boot
├── runtime.txt         # python version
├── .env.example        # env template
└── README.md           # you are here
```

---

## `> export SECRETS`

Never hardcode. Always inject.

| Variable | Purpose | Required |
|----------|---------|----------|
| `BOT_TOKEN` | Telegram bot token | ✅ |
| `API_ID` | Telegram API ID | ✅ |
| `API_HASH` | Telegram API hash | ✅ |
| `OWNER_ID` | Admin / owner user ID | ✅ |
| `PORT` | Web port (auto on Heroku) | ❌ |

---

## `> ./run --local`

```bash
git clone https://github.com/proarru/ArruCamBot.git
cd ArruCamBot

python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

pip install -r requirements.txt

export BOT_TOKEN="xxxxx"
export API_ID="12345"
export API_HASH="xxxxxxxxxxxxxxxx"

python app.py
```

---

## `> deploy --target heroku`

```bash
# 1. Auth
heroku login

# 2. Spin up a node
heroku create arrucam-bot

# 3. Inject secrets
heroku config:set BOT_TOKEN="xxxxx"
heroku config:set API_ID="12345"
heroku config:set API_HASH="xxxxxxxxxxxxxxxx"
heroku config:set OWNER_ID="your_id"

# 4. Push payload
git add .
git commit -m "deploy: payload armed"
git push heroku main

# 5. Ignite
heroku ps:scale worker=1

# 6. Watch the wire
heroku logs --tail
```

### Procfile

```procfile
worker: python app.py
```

> ⚠️ Web dyno use kar rahe ho to `$PORT` bind karna zaroori hai. Pure bot ke liye `worker` better.

---

## `> commands --list`

| Command | Action |
|---------|--------|
| `/start` | Wake the beast |
| `/help`  | Show manual |
| `/capture` | Snapshot 📸 |
| `/status` | Bot heartbeat |
| ... | (apne actual commands daalo) |

---

## `> troubleshoot --quick`

**Crash loop?**
```bash
heroku logs --tail
```
→ missing env, galat Procfile, ya missing dependency.

**Bot dead silence?**
→ Token galat, ya local instance bhi chal raha hai (conflict).

**Web dyno 60s me bind nahi hua?**
```python
import os
app.run(host="0.0.0.0", port=int(os.environ.get("PORT", 5000)))
```

**Free tier chahiye?** Heroku pe ab nahi hai. Try:
- Railway
- Render
- Fly.io
- Koyeb

---

## `> security --notes`

```
[!] Token ko code me mat likho
[!] .env ko .gitignore me daalo
[!] Token leak hua? @BotFather -> /revoke turant
[!] Public repo? Secrets scanner laga ke rakho
```

---

## `> credits`

```
Developer : ProArru
Telegram  : @Proarru
Repo      : github.com/proarru/ArruCamBot
```

---

## `> exit`

```
[ connection closed ]
[ arrucam bot :: standing by ]
```

**License:** MIT
