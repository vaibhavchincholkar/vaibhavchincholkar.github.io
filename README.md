# Vaibhav Chincholkar — Personal Website

A fast, dependency-free personal profile site. Single page, fully responsive,
light/dark theme, accessible, and ready to host **free** on GitHub Pages.

```
index.html    → structure & content
styles.css    → styling (light/dark themes, responsive)
script.js     → theme toggle, mobile nav, scroll reveal
```

No build step, no frameworks, no tracking.

---

## Preview locally

Just open the file:

```bash
open index.html
```

Or run a tiny local server (nice for testing relative paths):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## Deploy free on GitHub Pages

Because this folder is named `vaibhavchincholkar.github.io`, GitHub will publish it
at **https://vaibhavchincholkar.github.io** automatically.

### 1. Create the repository
1. Go to <https://github.com/new>
2. **Repository name:** `vaibhavchincholkar.github.io` (must match exactly)
3. Visibility: **Public**
4. Do **not** add a README/license (this folder already has files)
5. Click **Create repository**

### 2. Push this folder

```bash
cd vaibhavchincholkar.github.io
git init
git add .
git commit -m "Add personal website"
git branch -M main
git remote add origin https://github.com/vaibhavchincholkar/vaibhavchincholkar.github.io.git
git push -u origin main
```

### 3. Turn on Pages (usually automatic for this repo name)
1. Repo → **Settings** → **Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main` / `root` → **Save**
4. Wait ~1 minute, then open **https://vaibhavchincholkar.github.io**

> First deploy can take a couple of minutes. After that, every `git push` updates the live site.

---

## Custom domain (optional, ~$10–15/yr for the domain only)

1. Buy a domain (Namecheap, Cloudflare, Google Domains, etc.)
2. Repo → Settings → Pages → **Custom domain** → enter your domain → Save
3. At your registrar, add DNS records:
   - `A` records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - or a `CNAME` → `vaibhavchincholkar.github.io`
4. Enable **Enforce HTTPS** once DNS resolves.

---

## Easy things to customize

| Want to change | Where |
| --- | --- |
| Any wording / bullet points | `index.html` |
| Add a real profile photo | Replace the `.hero__avatar` / `VC` monogram with `<img>` |
| Brand color | `--accent` / `--accent-2` in `styles.css` |
| Default theme | `data-theme="dark"` on `<html>` in `index.html` |
| Add/remove a project | Copy a `<article class="card">` block in `index.html` |

---

## Privacy notes

- **Phone number is intentionally omitted** from the public site.
- Content is written at résumé level — no confidential or employer-internal details.
- Email is shown as a `mailto:` link; remove it from `index.html` if you'd prefer a form-only contact.
