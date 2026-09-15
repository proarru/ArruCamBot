<div align="center">

```
    ___              ___         ______      __ 
   /   |  __________(_) /_  __   / ____/___ _/ /_
  / /| | / ___/ ___/ / __ \/ /  / /   / __ `/ __ \
 / ___ |/ /  / /  / / /_/ / /  / /___/ /_/ / /_/ /
/_/  |_/_/  /_/  /_/_.___/_/   \____/\__,_/_.___/ 
```

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=2500&pause=600&color=00FF88&center=true&vCenter=true&width=600&lines=%5B+ARRUCAMBOT+%2F%2F+REMOTE+SURVEILLANCE+UNIT+%5D;%5B+STATUS%3A+ONLINE+%5D;%5B+MODE%3A+STEALTH+%5D;%5B+AUTH%3A+PROARRU+%5D" alt="Typing SVG" />

<br/>

<a href="https://t.me/Proarru">
  <img src="https://img.shields.io/badge/Telegram-@Proarru-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"/>
</a>
<a href="https://github.com/proarru/ArruCamBot">
  <img src="https://img.shields.io/badge/GitHub-ArruCamBot-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</a>
<a href="https://heroku.com/deploy?template=https://github.com/proarru/ArruCamBot">
  <img src="https://img.shields.io/badge/Deploy-Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white" alt="Deploy"/>
</a>

<br/>

<img src="https://komarev.com/ghpvc/?username=proarru&label=VISITORS&color=00ff88&style=for-the-badge" alt="Visitors"/>

</div>

---

<div align="center">

### `> whoami`

**ArruCamBot** — ek Telegram-controlled remote camera bot.
Heroku pe 24/7 chalta hai, commands receive karta hai, kaam karta hai, aur chup chaap so jata hai.

Built by **ProArru**

<a href="https://t.me/Proarru">
  <img src="https://img.shields.io/badge/Chat%20on-Telegram-26A5E4?style=flat-square&logo=telegram&logoColor=white"/>
</a>
<a href="https://github.com/proarru">
  <img src="https://img.shields.io/badge/Follow%20on-GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
</a>

</div>

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

<div align="center">

<a href="https://heroku.com/deploy?template=https://github.com/proarru/ArruCamBot">
  <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy to Heroku"/>
</a>

</div>

```bash
heroku login
heroku create arrucam-bot
heroku config:set BOT_TOKEN="xxxxx"
heroku config:set API_ID="12345"
heroku config:set API_HASH="xxxxxxxxxxxxxxxx"
heroku config:set OWNER_ID="your_id"

git add .
git commit -m "deploy: payload armed"
git push heroku main

heroku ps:scale worker=1
heroku logs --tail
```

### Procfile

```procfile
worker: python app.py
```

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

**Bot dead silence?**
→ Token galat, ya local instance bhi chal raha hai (conflict).

**Web dyno 60s me bind nahi hua?**
```python
import os
app.run(host="0.0.0.0", port=int(os.environ.get("PORT", 5000)))
```

---

## `> security --notes`

```
[!] Token ko code me mat likho
[!] .env ko .gitignore me daalo
[!] Token leak hua? @BotFather -> /revoke turant
```

---

<div align="center">

## `> credits`

```
Developer : ProArru
Telegram  : @Proarru
GitHub    : github.com/proarru
Repo      : github.com/proarru/ArruCamBot
```

<a href="https://t.me/Proarru">
  <img src="https://img.shields.io/badge/Telegram-@Proarru-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
</a>
<a href="https://github.com/proarru/ArruCamBot">
  <img src="https://img.shields.io/badge/GitHub-ArruCamBot-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2500&pause=600&color=00FF88&center=true&vCenter=true&width=500&lines=%5B+connection+closed+%5D;%5B+arrucam+bot+%3A%3A+standing+by+%5D" alt="Typing SVG"/>

**License:** MIT

</div>
