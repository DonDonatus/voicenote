# 🎙️ Voice-to-Checklist Notes App

> **"Say your day, get your checklist, get nudged at the right time."**

A voice-first Progressive Web App (PWA) that transforms spoken thoughts and daily schedules into structured, actionable checklists with timely push notification reminders.

---

## 🌟 What is VoiceNote?

Typing out daily tasks on a phone is slow and tedious, while static checklists are easily forgotten without proactive reminders. **VoiceNote** bridges the gap between natural speech and follow-through:

1. **Speak Naturally**: Talk about your day without worrying about manual formatting.
2. **AI-Structured Checklists**: Automatic extraction of tasks, subtasks, due times, and priority levels.
3. **Review & Confirm**: A quick draft screen keeps you in control before anything is saved.
4. **Server-Dispatched Reminders**: Timely web push notifications arrive on your phone or desktop right when tasks are due.
5. **Installable Anywhere**: Built as a cross-platform PWA that installs directly to your home screen on iOS, Android, and desktop.

---

## 🚀 Live Starter Preview

The repository includes a responsive landing page and visual starter checklist. You can preview it right now by opening [`index.html`](index.html) in your browser.

- **Foundational Roadmap**: The interactive starter section highlights the core build sequence from foundation to first reminder.
- **Design & Layout**: Pure semantic HTML with custom, responsive styling in [`styles.css`](styles.css).

---

## ⚙️ How It Works

```
[ 🎙️ Speak Plan ] 
       │
       ▼
[ 📝 Fast STT ] ─────────► Transcribes audio to text in near-realtime
       │
       ▼
[ 🤖 AI Parsing ] ───────► Extracts tasks, priorities, & converts times to UTC
       │
       ▼
[ ✏️ Human Review ] ─────► Confirm or tweak draft before saving
       │
       ▼
[ 🔔 Web Push Alert ] ───► Server sends push notification at exact due time
```

---

## 🛠️ Tech Stack at a Glance

| Layer | Technology | Role |
|---|---|---|
| **Frontend** | Next.js / PWA | Installable app shell, offline caching, Service Worker |
| **Styling** | Vanilla CSS | Modern, lightweight, responsive styling |
| **Backend** | FastAPI (Python 3.11+) | Async API gateway & reminder scheduler |
| **Database** | PostgreSQL | Relational storage for users, plans, tasks, and reminders |
| **Push Engine** | Web Push API (VAPID) | Cross-platform notifications (iOS 16.4+, Android, Desktop) |
| **AI / STT** | Whisper + Gemini / OpenAI | Audio transcription & structured JSON task parsing |

---

## 📚 Complete Technical Documentation

For the full architectural breakdown, PostgreSQL schemas, API specifications, push notification lifecycle, and phased delivery roadmap, see:

👉 **[Technical Implementation Plan (IMPLEMENTATION_PLAN.md)](IMPLEMENTATION_PLAN.md)**

---

## 🗺️ Build Roadmap

- [ ] **Phase 0: Setup Shell** — Installable PWA shell, FastAPI skeleton, PostgreSQL setup.
- [ ] **Phase 1: Thin Slice** — Mic recording, speech-to-text, structured AI extraction, 1 scheduled test push.
- [ ] **Phase 2: Full MVP** — Interactive review screen, offline storage (IndexedDB), server scheduler, iOS onboarding.
- [ ] **Phase 3: Version 2** — Push action buttons (Done/Snooze), morning briefing, voice commands, recurring tasks.
- [ ] **Phase 4: Launch & Hardening** — Instant audio deletion for privacy, rate limits, delivery telemetry.

---

## 🏃 Getting Started

### Previewing the Landing Page
Simply open `index.html` in any modern web browser or serve it with a local static server:
```bash
# Using python
python -m http.server 3000

# Or using npx serve
npx serve .
```
Visit `http://localhost:3000` to view the landing page and starter checklist.

---

## 📝 License & Credits
- **Project Lead**: @Donatus
- **Document Date**: October 28, 2026
