<div align="center">

```
    ___              ___         ______      __ 
   /   |  __________(_) /_  __   / ____/___ _/ /_
  / /| | / ___/ ___/ / __ \/ /  / /   / __ `/ __ \
 / ___ |/ /  / /  / / /_/ / /  / /___/ /_/ / /_/ /
/_/  |_/_/  /_/  /_/_.___/_/   \____/\__,_/_.___/ 
```

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&duration=2500&pause=600&color=00FF88&center=true&vCenter=true&width=700&lines=%5B+ARRUCAMBOT+%2F%2F+OWN-DEVICE+UNIT+%5D;%5B+PHOTO+%7C+VIDEO+%7C+AUTO+%7C+LIVE+GPS+%5D;%5B+STATUS%3A+ONLINE+%5D;%5B+AUTH%3A+PROARRU+%5D" />

<br/>

<a href="https://t.me/Proarru"><img src="https://img.shields.io/badge/Telegram-@Proarru-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/></a>
<a href="https://github.com/proarru/ArruCamBot"><img src="https://img.shields.io/badge/GitHub-ArruCamBot-181717?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

---

## `> whoami`

**ArruCamBot** — apne device ka camera + live GPS Telegram se control karo.
Auto photo/video loop, live location dashboard, sab kuch built-in.

Built by **ProArru** · [@Proarru](https://t.me/Proarru)

---

## `> features`

```
[+] /capture          → photo
[+] /video <sec>      → video (max 60s)
[+] /autocapture on   → auto loop start
[+] /autocapture off  → auto loop stop
[+] /interval <sec>   → set interval (min 10s)
[+] /autotype photo|video
[+] /location         → IP-based location
[+] /live             → live GPS dashboard
[+] Web dashboard + map
```

---

## `> bot-commands`

| Command | Action |
|---------|--------|
| `/start` | Wake the bot |
| `/capture` | Photo |
| `/video 15` | 15s video |
| `/autocapture on` | Start auto loop |
| `/autocapture off` | Stop auto loop |
| `/interval 30` | Set 30s interval |
| `/autotype photo` | Auto = photo |
| `/autotype video` | Auto = video |
| `/location` | IP location |
| `/live` | Live GPS dashboard link |
| `/status` | Heartbeat |

---

## `> setup --local`

```bash
git clone https://github.com/proarru/ArruCamBot.git
cd ArruCamBot
npm install
cp .env.example .env
# BOT_TOKEN aur OWNER_ID daalo
npm start
```

**System deps:**

| OS | Install |
|----|---------|
| Linux | `sudo apt install ffmpeg fswebcam` |
| Mac | `brew install ffmpeg imagesnap` |
| Windows | [ffmpeg.org](https://ffmpeg.org) → PATH me add |

---

## `> live-location`

1. `npm start`
2. Browser me kholo: `http://localhost:3000/live`
3. GPS permission do
4. Location har 5s me update hogi + Telegram pe bhi aayegi

> ⚠️ HTTPS zaroori hai GPS ke liye. `localhost` exempt hai. Public pe deploy karo to HTTPS use karo.

---

## `> security`

```
[!] OWNER_ID set karo — warna koi bhi use kar sakta hai
[!] Token .env me rakho
[!] Token leak? @BotFather -> /revoke
[!] Sirf apne device pe chalao
[!] Live GPS browser-based hai (VPN se affect nahi)
```

---

<div align="center">

## `> credits`

```
Developer : ProArru
Telegram  : @Proarru
GitHub    : github.com/proarru
```

**MIT License**

</div>
