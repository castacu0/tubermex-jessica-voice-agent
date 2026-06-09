<div align="center">

# 🔧 TuberMex Plomería · Jessica

### Bilingual voice AI agent for a Mexico City plumber

![status](https://img.shields.io/badge/agent-live-34d399?style=for-the-badge)
![lang](https://img.shields.io/badge/languages-EN%20%2B%20ES-3b82f6?style=for-the-badge)
![voice](https://img.shields.io/badge/voice-Jessica%20(American)-f472b6?style=for-the-badge)
![platform](https://img.shields.io/badge/built%20on-ElevenLabs%20Agents-000000?style=for-the-badge)

**A demo voice agent that answers the phone, runs a guided intake, triages emergencies, and offers a human handoff.**

[🎙️ Talk to Jessica](https://elevenlabs.io/app/talk-to/agent_8801ktq4ba78ezebznsgbmk3j6sp) · [🌐 Live demo page](https://castacu0.com/hidden-testing-live-demos/) · [📊 Open the dashboard](./index.html)

</div>

---

> [!NOTE]
> **TuberMex Plomería is a fictive brand.** Every name, price, phone number, and address is demo data for testing. Nothing here is a real business.

## 🌐 Live demo

The agent is embedded and testable here:

**👉 https://castacu0.com/hidden-testing-live-demos/**

A floating call button mounts bottom-right. Click it, allow the mic, and talk to Jessica in English or Spanish.

---

## 📦 What's in this repo

| File | Purpose |
|------|---------|
| `index.html` | Visual control panel + interactive simulator (open in any browser) |
| `README.md` | This file |
| `CLAUDE.md` | Project context + agent spec for Claude Code |

The `index.html` dashboard has 6 tabs: **Overview · Configuration · Conversation Flow · Services & Pricing · Try Jessica · Deploy & Options**. The "Try Jessica" tab mounts the real ElevenLabs voice widget *and* a scripted simulator that burns no minutes.

---

## 🤖 The agent

| Setting | Value |
|---------|-------|
| **Name** | Jessica |
| **Agent ID** | `agent_8801ktq4ba78ezebznsgbmk3j6sp` |
| **Voice** | Jessica – Playful, Bright, Warm (American accent, for expats) |
| **Voice ID** | `cgSgspJ2msm6clMCkdW9` |
| **Languages** | English (default) + Spanish (Mexican) |
| **LLM** | Claude Haiku 4.5 |
| **Temperature** | 0.6 |
| **Timezone** | America/Mexico_City |

### Conversation flow

Jessica gathers **at least 5 questions** before she ever offers a human transfer:

```
1. Language preference  (EN / ES)
2. Name
3. Location / colonia
4. Problem description
5. Clarifying follow-up
6. Urgency check
   └─► THEN: "Schedule a technician, or transfer you to a plumber?"
```

**Emergency override:** active flooding / burst pipe / sewage → skip the script, grab the address, dispatch.
**Gas smell:** redirect to the gas provider, tell caller to ventilate, offer a pipe check after.

---

## 🏢 Demo brand: TuberMex Plomería

- **Slogan (EN):** "Your trusted plumber, always on time."
- **Slogan (ES):** "Tu plomero de confianza, siempre a tiempo."
- **Phone / WhatsApp:** 55 4321 0987
- **Founded:** 2011 · 9 certified plumbers, 4 field assistants
- **Service area:** Benito Juárez, Coyoacán, Álvaro Obregón, Miguel Hidalgo, Cuauhtémoc, Tlalpan, Xochimilco, Magdalena Contreras

### Pricing (MXN, demo estimates)

| Service | Estimate |
|---------|----------|
| Diagnostic visit | $350 (credited) |
| Labor / hour | $400 – $550 |
| After-hours premium | +$200/hr |
| Drain cleaning | $600 – $900 |
| Water heater install (labor) | $1,200 – $1,800 |
| Leak detection | $800 – $1,500 |
| Toilet repair / wax ring | $350 – $600 |

---

## 🚀 Embed Jessica on any site

Drop this into an HTML block (works in WordPress / Elementor HTML widget):

```html
<elevenlabs-convai agent-id="agent_8801ktq4ba78ezebznsgbmk3j6sp"></elevenlabs-convai>
<script src="https://unpkg.com/@elevenlabs/convai-widget-embed" async type="text/javascript"></script>
```

> [!IMPORTANT]
> The agent must be set to **Public** in the ElevenLabs Widget tab for the embed to work. Whitelist your domain there to stop others from calling the agent with your ID.

---

## 🧪 Run the dashboard locally

```bash
open index.html      # macOS
# or just double-click the file
```

No build step, no dependencies. One self-contained HTML file.

---

## 🛠️ Built with

- [ElevenLabs Agents](https://elevenlabs.io) — voice + conversation engine
- Claude Code (desktop) — agent creation via MCP
- Plain HTML/CSS/JS — zero-dependency dashboard
