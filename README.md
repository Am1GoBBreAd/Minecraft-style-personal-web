# ⛏️ Personal Portfolio Template

A minimal Minecraft-style personal portfolio built with **pure HTML + CSS + JavaScript** — no frameworks, no build tools, no dependencies. Just drop your content in and ship it.

> **Author:** [Zhirui (Luis) Lyu](https://linkedin.com/in/zhirui-lyu-a0325030b)

---

## 📸 Screenshots

<!-- Replace the paths below with your actual screenshots -->

| Hero Section | Experience |
|---|---|
| ![Hero](screenshots/hero.png) | ![Experience](screenshots/experience.png) |

| Projects | Contact Chatbox |
|---|---|
| ![Projects](screenshots/projects.png) | ![Contact](screenshots/contact.png) |

---

## ✨ Features

- **Hero section** — name, tagline, skill tags, fun stats, and a personal photo frame with hover effects
- **Experience tabs** — switchable Work / Education panels
- **Project cards** — hover animations with top-bar accent color
- **Gallery carousel** — infinite auto-scroll with pause-on-hover, supports real images or placeholders
- **Contact chatbox** — fake chat UI that fires a pre-filled `mailto:` on send (no backend needed)
- **Scroll fade-in** — cards and items animate in via IntersectionObserver
- **Fixed nav** — blur backdrop, smooth scroll to all sections
- **Fully responsive** — collapses cleanly on mobile

---

## 🗂️ File Structure

```
portfolio/
├── index.html          ← everything lives here (single file)
├── photo.jpg           ← your personal photo (replace with your own)
├── screenshot1.png     ← gallery images (rename to match index.html)
├── screenshot2.png
└── ...
```

---

## 🚀 Getting Started

### 1. Clone or download

```bash
git clone https://github.com/your-username/portfolio-template.git
cd portfolio-template
```

### 2. Open locally

Just open `index.html` in your browser — no server needed.

```bash
open index.html       # macOS
start index.html      # Windows
```

### 3. Customize content

All content is in `index.html`. Search for these sections:

| What to change | Search for |
|---|---|
| Your name & bio | `Hi, I'm` |
| Skill tags | `class="tags"` |
| Fun stats | `class="hero-stats"` |
| Work experience | `id="pane-work"` |
| Education | `id="pane-school"` |
| Projects | `class="projects-grid"` |
| Gallery images | `var galleryItems` |
| Contact email | `mailto:` |
| LinkedIn / GitHub links | `linkedin.com` / `github.com` |

### 4. Add your photo

Inside the hero section, replace:

```html
<div class="photo-placeholder">
  <div class="photo-placeholder-icon">🧑‍💻</div>
  <div class="photo-placeholder-label">your photo here</div>
</div>
```

with:

```html
<img src="photo.jpg" alt="Your Name" />
```

> **Tip:** Portrait orientation (taller than wide) works best. The frame is 280×340px and crops from the top.

### 5. Add gallery images

Edit the `galleryItems` array in the `<script>` section:

```js
var galleryItems = [
  { src: 'screenshot1.png', caption: 'Caption 1' },
  { src: 'screenshot2.png', caption: 'Caption 2' },
  // add more...
];
```

Images must be in the same folder as `index.html`.

---

## 🎨 Theming

All colors are CSS variables at the top of the `<style>` block — easy to swap:

```css
:root {
  --bg:      #0f1117;   /* page background */
  --bg2:     #161a24;   /* card background */
  --stone:   #2a2f3e;   /* subtle surfaces */
  --border:  #313849;   /* borders */
  --green:   #5aab4a;   /* primary accent */
  --diamond: #44c8d8;   /* secondary accent */
  --gold:    #f0b429;   /* highlight */
  --text:    #e8eaf0;   /* body text */
  --muted:   #8a91a8;   /* secondary text */
}
```

---

## 📬 Contact Chatbox

The chatbox uses `mailto:` — no server or API needed. When a visitor hits **Send**, their email client opens with the message pre-filled.

To change the recipient email, find this line in the script:

```js
window.location.href = 'mailto:your@email.com?subject=' + subject + '&body=' + body;
```

---

## 🌐 Deploying

Works with any static host:

| Platform | How |
|---|---|
| **GitHub Pages** | Push to `gh-pages` branch or enable Pages in repo settings |
| **Netlify** | Drag and drop the folder at netlify.com/drop |
| **Vercel** | `vercel deploy` in the folder |
| **Cloudflare Pages** | Connect repo, build command: none, output: `/` |

> **Note:** If you host on Cloudflare, your email addresses will be automatically obfuscated for bot protection. This is normal — visitors still see them correctly.

---

## 🛠️ Built With

- HTML5 + CSS3 + Vanilla JS — zero dependencies
- [Syne](https://fonts.google.com/specimen/Syne) — display font
- [DM Sans](https://fonts.google.com/specimen/DM+Sans) — body font
- Google Fonts CDN

---

## 📄 License

MIT — free to use, modify, and distribute. Credit appreciated but not required.

---

<p align="center">Built with ⛏️ &nbsp;·&nbsp; Waterloo, ON</p>
