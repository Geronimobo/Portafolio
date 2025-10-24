# Geronimo Botero Laverde — Portfolio

A dark, responsive, static portfolio built with **HTML + Tailwind (CDN) + vanilla JavaScript**.  
Includes sections for About, Projects, Hobbies, and a Contact form (mailto fallback or Formspree).

## ✅ Features
- Fully static (no build step, no framework required)
- Responsive layout (mobile topbar, desktop sidebar)
- Consistent image frames (no distortion, `object-contain`)
- Accessible colors and focus states
- Contact form with **mailto** fallback or **Formspree** endpoint
- Easy to host on **Vercel / Netlify / GitHub Pages**

---

## 🧭 Project Structure
```
/
├─ index.html
├─ assets/
│  ├─ headshot.jpg
│  ├─ auth0_1.png
│  ├─ weatherapp_1.png
│  ├─ juansao_1.png
│  ├─ hobby_gym.jpg
│  ├─ hobby_cycling.jpg
│  └─ hobby_reading.jpg
└─ README.md
```

> Tailwind is loaded via CDN in `index.html` (no config or node_modules required).

---

## 🛠️ Run Locally

You have multiple options; pick your favorite:

### Option 1 — VS Code (Live Server extension)
1. Open the folder in **VS Code**.
2. Install the extension **“Live Server”** (Ritwick Dey).
3. Right-click `index.html` → **Open with Live Server**.
4. Your site will open at `http://localhost:5500` (or similar).

### Option 2 — Python HTTP server (preinstalled on macOS/Linux)
```bash
# from the project root (where index.html is)
python3 -m http.server 8080
# then visit:
# http://localhost:8080
```

### Option 3 — Node http-server (if you have Node.js)
```bash
# install once
npm install -g http-server

# start server from project root
http-server -p 8080

# visit http://localhost:8080
```

> You can also double-click `index.html` to open it directly, but using a local server is recommended to mimic production and avoid path issues.

---

## ✉️ Contact Form (Formspree or mailto)
- By default, the form **falls back to mailto** if no Formspree endpoint is set.
- To use Formspree:
  1. Create a new form at Formspree and copy your endpoint URL (e.g. `https://formspree.io/f/abcd1234`).
  2. In `index.html`, replace:
     ```html
     <form action="https://formspree.io/f/TU_ENDPOINT" method="POST">
     ```
     with your endpoint.
- If `action` is missing or contains `TU_ENDPOINT`, the script will trigger:
  ```
  mailto:gerobote@hotmail.com
  ```
  with the form data.

---

## 🚀 Deploy

### Vercel (recommended if you may migrate to Next.js later)
1. Push this project to a **GitHub** repository.
2. Go to **Vercel → New Project → Import Git Repository**.
3. Framework: **Other / Static**.  
   Build command: _none_  
   Output directory: `/` (root)
4. Deploy → you’ll get `your-site.vercel.app`.

### Netlify (drag & drop)
1. Zip or select the folder that contains `index.html` and `assets/`.
2. In Netlify, **Add new site → Deploy manually** → drag & drop the folder.
3. Netlify assigns a `*.netlify.app` domain (you can customize it).

### GitHub Pages
1. Push to a GitHub repo.
2. **Settings → Pages** → “Deploy from branch” → `main` + `/ (root)`.
3. Save and wait for `https://<user>.github.io/<repo>/`.

---

## 🔧 Customization Tips
- **Accent colors**: search for `cyan` in `<style>` and replace with your palette.
- **Images**: replace files in `/assets` and keep the same filenames, or update `src` paths in `index.html`.
- **Accessibility**: verify contrast if you change colors.

---

## 📄 License
MIT (or your preferred license)
