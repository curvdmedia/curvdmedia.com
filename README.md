# Curvd Media — Website

Official website for **Curvd Media**, a premium creative media agency.  
Deployed via **GitHub Pages** — no build step, no dependencies.

---

## 🚀 Deploy to GitHub Pages

### Step 1 — Create the repo

1. Go to [github.com/new](https://github.com/new)
2. Name it `curvd-media` → **Public** → **Create repository**

### Step 2 — Push the files

```bash
git init
git add .
git commit -m "Initial commit — Curvd Media website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/curvd-media.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Repo → **Settings** → **Pages**
2. Source: `main` branch, `/ (root)` folder → **Save**
3. Live at `https://YOUR_USERNAME.github.io/curvd-media` in ~60 seconds

### Step 4 — Custom domain (optional)

1. In **Settings → Pages**, enter your domain e.g. `curvdmedia.com`
2. Add a `CNAME` DNS record pointing to `YOUR_USERNAME.github.io`
3. Edit the `CNAME` file in this repo with your domain

---

## 📬 Set Up the Contact Form (Formspree)

GitHub Pages is static — it can't handle forms server-side.  
The form uses **Formspree** (free, submissions go to your email).

### 1. Create a free Formspree account
Go to [formspree.io](https://formspree.io) → **Sign up free**

### 2. Create a new form
- Click **New Form**
- Name it `curvd-project-inquiry`
- Copy your **Form ID** (looks like `xpwzgkrb`)

### 3. Update index.html
Find this line:
```html
<form ... action="https://formspree.io/f/YOUR_FORM_ID" ...>
```
Replace `YOUR_FORM_ID` with your actual ID:
```html
<form ... action="https://formspree.io/f/xpwzgkrb" ...>
```

### 4. Push the change
```bash
git add index.html
git commit -m "Add Formspree form ID"
git push
```

Done — submissions will land in your Formspree dashboard and get forwarded to your email.

---

## 📁 Structure

```
curvd-media/
├── index.html    # Complete site — self-contained, no dependencies
├── CNAME         # Custom domain (edit if needed)
├── .gitignore
└── README.md
```

---

## 🎨 Brand Colours

| Role | Hex |
|---|---|
| Background | `#0D0D0D` |
| Text / Cream | `#F0EDE6` |
| Accent / Orange | `#E8520A` |

---

## ✏️ Quick Edits

| What | Where in `index.html` |
|---|---|
| Page copy | Search for the text directly |
| Email | `hello@curvdmedia.com` |
| Social links | Search `instagram.com` / `linkedin.com` |
| Logo | Replace `data:image/png;base64,...` src values |
| Colours | `:root` CSS variables at top of `<style>` |
| Form endpoint | `action="https://formspree.io/f/YOUR_FORM_ID"` |

---

© 2026 Curvd Media. All rights reserved.
