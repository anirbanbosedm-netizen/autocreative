# Anima.ai — AI Creative Platform for Busy Professionals

> Your social media, on autopilot. Built for doctors, lawyers, and other professionals who want to post on social media but don't have time to create content.

---

## What It Does

Anima.ai is a single-file HTML application that automates social media creative generation end-to-end:

1. **Set up your profile once** — name, clinic/business name, specialisation, logo, brand colors
2. **Connect Canva** — one-time integration
3. **Fill the calendar** — pick dates, select occasion type, write a title
4. **AI generates everything automatically** — branded poster image, caption, and 10 hashtags
5. **Approve and download** — one click saves the PNG to your device, ready to post

No editing. No design skills needed. No manual content writing.

---

## Who It's For

- Doctors and healthcare professionals
- Lawyers, CAs, and consultants
- Clinic owners and solo practitioners
- Any professional who uses social media but doesn't have time to create content

---

## Features

- **Login / Sign Up** — email + password, accounts persist in browser localStorage
- **My Profile** — name, specialisation, logo, brand colors — saved permanently per account
- **Content Calendar** — monthly view, click any date to add a post entry
- **AI Creative Generation** — branded poster (canvas, 800×800) auto-generated with your colors and logo
- **AI Caption + Hashtags** — Claude API generates professional captions tailored to healthcare/professional context
- **Review & Approve** — full post card with creative, caption, hashtags, date, platform
- **Download PNG** — one click saves the creative to your device
- **Copy Caption** — copies title + caption + hashtags to clipboard
- **Canva Integration** — connect once, creatives marked for auto-sync
- **Analytics** — overview of generated and approved creatives
- **No backend required** — everything runs in the browser

---

## Setup

### 1. Get an Anthropic API Key

Go to [console.anthropic.com](https://console.anthropic.com) and create an account. Copy your API key — it starts with `sk-ant-…`

### 2. Open the App

Download `anima-ai-platform.html` and open it in any modern browser. No server needed.

### 3. Enter Your API Key

On first launch, you'll be prompted to enter your Anthropic API key. It is stored **only in your browser's localStorage** — never sent to any server other than Anthropic's API directly.

> **No API key?** You can skip this step and the app will use fallback captions instead of AI-generated ones. Everything else works fully.

### 4. Create an Account and Start

Sign up, fill your profile, connect Canva, and add calendar entries. The AI does the rest.

---

## Privacy & Security

| Item | Detail |
|---|---|
| API Key | Stored in browser localStorage only. Never leaves your device except for direct calls to Anthropic's API. |
| User Data | All profile, calendar, and creative data stored in browser localStorage. No external database. |
| Passwords | Stored as base64 in localStorage (demo-grade). For production, use a proper auth backend. |
| No tracking | No analytics, no ads, no external scripts except Google Fonts and the Anthropic API. |

---

## Tech Stack

- Pure HTML + CSS + JavaScript — zero dependencies, zero build step
- [Anthropic Claude API](https://www.anthropic.com) — for caption and hashtag generation
- HTML5 Canvas API — for creative poster generation
- localStorage — for persistent user data
- Google Fonts — Plus Jakarta Sans + Fraunces

---

## Limitations (Open Source Version)

| Feature | Status |
|---|---|
| AI creative generation | ✅ Works — uses HTML Canvas with brand colors |
| AI caption + hashtags | ✅ Works — requires Anthropic API key |
| Download PNG | ✅ Works |
| Copy caption | ✅ Works |
| Canva auto-push | ⚠️ Indicator only — full push requires Canva Developer API (backend) |
| Instagram auto-post | 🔜 Coming soon — requires backend OAuth |
| Facebook auto-post | 🔜 Coming soon — requires backend OAuth |
| Password security | ⚠️ Base64 only — use a real auth system for production |
| Multi-device sync | ❌ localStorage is device-specific |

---

## Running Locally

```bash
# No build step needed — just open the file
open anima-ai-platform.html

# Or serve it with any static server
npx serve .
python3 -m http.server 8080
```

---

## Contributing

Pull requests welcome. Key areas for contribution:

- Backend integration (Node.js / Supabase) for real auth and multi-device sync
- Canva API integration for actual design auto-push
- Instagram / Facebook OAuth posting
- More creative templates and styles
- Mobile responsive improvements

---

## License

MIT License — free to use, modify, and distribute.

---

Made with ❤️ for busy professionals who deserve great social media without the effort.
