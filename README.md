Got it — you want a **professional README.md** in English that explains exactly how to install, run, and use your project (including all npm dependencies and the features you’ve built, like Feed, Tasks, Tarot, Music, etc.), so a judge or reviewer can quickly set it up and understand what it does.

Here’s a full draft:

---

# VLINKS

**VLINKS** is a mindfulness-oriented progressive web application built with **React + Vite**.
It provides users with a calming digital space to manage tasks, share reflections, listen to music, and explore interactive features like Tarot-style self-reflection.

The goal of the project is to combine productivity and mental wellness into a single simple, mobile-friendly app.

---

## ✨ Features

* **Mindful Feed**

  * Post and browse short reflections or photos.
  * Clean, distraction-free UI.

* **Task Manager**

  * Create, mark complete, and reset tasks.
  * Prioritize tasks visually.

* **Music Player**

  * Minimal player UI with play, pause, skip.
  * Safe-area-aware design for mobile devices.

* **Tarot / Reflection Cards**

  * Choose cards for self-reflection.
  * Integrated with Google Gemini API for AI-generated readings.
  * Fallback local card meanings if API quota is exceeded.

* **Safety Net**

  * If risky input is detected, app displays crisis resources (e.g. Befrienders KL).

* **PWA (Progressive Web App)**

  * Installable on mobile or desktop.
  * Offline support via service worker.

---

## 🛠️ Tech Stack

* **React 18** with TypeScript
* **Vite** as bundler
* **Tailwind CSS** for styling
* **Supabase** for backend (authentication, database, storage)
* **Google Gemini API** for AI-generated readings
* **Vite Plugin PWA** for offline and installable support

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/jxon12/Meet-VLinks.git
cd Meet-VLinks
```

### 2. Install dependencies

Make sure you have **Node.js ≥ 18** installed. Then run:

```bash
npm install
```

This installs all required packages, including:

* `react`, `react-dom`
* `@vitejs/plugin-react`
* `vite`
* `vite-plugin-pwa`
* `tailwindcss`, `postcss`, `autoprefixer`
* `@supabase/supabase-js`

### 3. Configure environment variables

Create a `.env` file in the project root with the following keys:

```env
VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
VITE_GEMINI_API_KEY=your-gemini-api-key
```

* **Supabase**: Create a project at [supabase.com](https://supabase.com), copy the API URL and anon key.
* **Gemini API**: Enable the Generative Language API on Google Cloud and create an API key.

### 4. Run in development

```bash
npm run dev
```

Visit the app at:

```
http://localhost:5173
```

### 5. Build for production

```bash
npm run build
```

The output will be in the `/dist` folder.

To preview locally:

```bash
npm run preview
```

---

## 🌐 Deployment

### GitHub Pages

* Set `vite.config.ts` → `base: '/YourRepoName/'`.
* Push to GitHub and enable Pages.

### Netlify / Vercel (Recommended)

* No config changes needed (`base: '/'`).
* Connect repo → set build command `npm run build` and publish directory `dist/`.
* For Netlify, add a `public/_redirects` file:

  ```
  /* /index.html 200
  ```

---

## 📖 Usage Guide

1. **Mindful Feed**

   * Post reflections or photos.
   * Scroll to view others’ posts.

2. **Tasks**

   * Add a new to-do.
   * Mark tasks as complete.
   * Reset list when finished.

3. **Music Player**

   * Open “Music” tab.
   * Play/pause track, skip forward/back.

4. **Tarot Reflection**

   * Choose a category (e.g. Career, Self-growth).
   * Enter a personal question.
   * Select 5 cards → receive AI-based or fallback reading.

5. **Safety Net**

   * If sensitive keywords are detected, a safety message and hotline resources will be displayed.

6. **PWA**

   * Install app to home screen (mobile) or desktop (Chrome/Edge).
   * Works offline with cached assets.

---

## 📌 Notes for Judges

* Works best in **Chrome / Edge / Safari (latest)**.
* Fully mobile-responsive.
* Offline caching supported, but AI features require internet.
* Crisis safety feature demonstrates ethical design consideration.

---

## 📄 License

This project is for educational and demo purposes.


