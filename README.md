# VLINKS 
Track2 Student Lifestyle (Mental Health Support for students)

**VLINKS** is a mindfulness-oriented progressive web application built with **React + Vite + Supabase**.
It combines productivity and well-being tools into a single platform, designed to help users stay calm, focused, and connected.

---

## ✨ Core Features

### 📰 Mindful Feed

* Share short reflections, photos, and thoughts.
* Scroll through posts from other users.
* Minimal, calming UI designed to reduce distraction.

### ✅ To-Do Tasks

* Add, edit, and complete daily tasks.
* Task priority indicators (high, medium, low).
* Energy-level tagging for better time management.
* Built-in **Pomodoro Timer** to support focus sessions.

### 🎵 Music Player

* Play/pause, skip forward/back, seek inside tracks.
* Responsive UI designed for mobile.
* Safe-area padding so controls are not blocked by overlays.

### 🔮 Tarot & Reflection

* Select a **category** (Career, Relationship, Interpersonal, Self-growth).
* Enter a **personal question** or concern.
* Pick **5 cards** out of 24 unique images.
* **AI Reading (Gemini API)**: 3-6 sentence warm reading + 2 practical suggestions + disclaimer.
* **Fallback Reading**: If Gemini quota is exhausted, local card meanings are combined into a short reflection.

### 🛡️ Safety Net

* If user input contains sensitive/self-harm words, the app displays:

  * A clear safety notice.
  * Crisis hotline resources (e.g. Befrienders KL: 03-7627 2929).
* Users must acknowledge before returning to the app.

### 📅 Calendar & Gratitude Journal

* Daily mood tracker (😀🙂😐🙁😢).
* Gratitude journal: add multiple notes per day.
* Stored locally in browser (with option to sync to Supabase if enabled).

### 📊 Dashboard & Insights

* View simple charts of productivity, mood, and gratitude over time.
* Designed for mindful reflection, not judgment.

### 📱 Progressive Web App (PWA)

* Installable on desktop and mobile.
* Offline caching via service worker.
* App icon, splash screen, and standalone mode.

---

## 🛠️ Tech Stack

* **React 18 + TypeScript**
* **Vite** bundler
* **TailwindCSS** styling
* **Supabase** (auth, database, storage)
* **Google Gemini API** (for AI Tarot readings)
* **Vite Plugin PWA** (offline & installable support)

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/jxon12/Meet-VLinks.git
cd Meet-VLinks
```

### 2. Install dependencies

Requires **Node.js v18+**.

```bash
npm install
```

This installs all dependencies:

* React, React DOM
* Vite + @vitejs/plugin-react
* vite-plugin-pwa
* Supabase JS SDK
* Tailwind, PostCSS, Autoprefixer

### 3. Set environment variables

Create a `.env` file in the project root:

```env
VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
VITE_GEMINI_API_KEY=your-gemini-api-key
```

* Get **Supabase URL & anon key** from your Supabase project.
* Enable **Google Gemini API** in Google Cloud and copy the API key.

### 4. Run in development

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173)

### 5. Build for production

```bash
npm run build
```

Output is in `/dist`.

Preview locally:

```bash
npm run preview
```

---

## 🌐 Deployment

### GitHub Pages

* Set `vite.config.ts` → `base: '/Meet-VLinks/'`.
* Push to repo, enable GitHub Pages → Deploy from branch `/docs` or `/dist`.

### Netlify (recommended)

* Build command: `npm run build`
* Publish directory: `dist`
* Add `public/_redirects` file with:

  ```
  /* /index.html 200
  ```

### Vercel

* Build command: `npm run build`
* Output directory: `dist`

---

## 📖 User Guide

1. **Sign in / Sign up**

   * Uses Supabase authentication.

2. **Mindful Feed**

   * Post short reflections.
   * Browse and like other posts.

3. **Tasks & Pomodoro**

   * Create new tasks with priority.
   * Start Pomodoro focus sessions.
   * Reset tasks daily.

4. **Music**

   * Open Music tab → play/pause/skip tracks.
   * Works both on desktop and mobile.

5. **Tarot Reflection**

   * Select category + enter your question.
   * Pick 5 cards → AI reading (Gemini).
   * Fallback to local meanings if API quota is reached.

6. **Safety Net**

   * Triggered if unsafe/self-harm words appear in input.
   * Provides hotline info + requires acknowledgement.

7. **Calendar & Gratitude**

   * Track daily mood with emoji.
   * Add gratitude notes per day.
   * Stored locally (with option to sync).

8. **PWA**

   * Install via browser (“Add to Home Screen”).
   * Works offline with cached assets.

---

## 📌 Notes for Judges

* Chrome / Edge recommended for best PWA experience.
* Gemini API must be configured for Tarot AI to function.
* Without Gemini API, fallback local reading still works.
* Supabase is optional: feed, posts, and tasks require backend; local-only mode still supports Tarot, Music, and Gratitude Journal.

---

## 📄 License

This project is provided for 2025 CodeNection Competition.



要不要我帮你把这个 README 改成 **Markdown 文件格式（带标题、表格、代码块等）**，你可以直接放进 `README.md` 上传到 GitHub？
