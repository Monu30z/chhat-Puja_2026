# 🪔 Happy Chhath Puja: Wishing Website
 
A single-page, animated website for sharing **Chhath Puja** wishes with family and friends. Visitors can write a message and send it on WhatsApp together with the website link.
 
> छठ पूजा की हार्दिक शुभकामनाएँ 🙏
 
![Status](https://img.shields.io/badge/status-live-orange)
![Stack](https://img.shields.io/badge/stack-HTML%20%7C%20CSS%20%7C%20JavaScript-gold)
![No dependencies](https://img.shields.io/badge/dependencies-none-green)
 
---
 
## ✨ Features
 
- **Animated sunrise hero:** the sun rises over a realistic river with shimmering water, ripples, mist, floating diyas and flying birds.
- **Devotees in the river:** women, a man and a crowd on the far bank offering *arghya* to the sun.
- **Hindu deity illustrations:** Surya Dev and Chhathi Maiya, drawn as inline SVG.
- **Four-day timeline:** Nahay-Khay, Kharna, Sandhya Arghya and Usha Arghya.
- **Wish composer:** type your name, pick a Hindi or English message (or edit it), then **Send on WhatsApp**, **Share** or **Copy**. The WhatsApp message includes the site link.
- **Final scene:** a woman standing in the river with a tray of diyas and prasad, next to the wish form.
- **Background song:** play/pause button with a smooth fade; the song starts from the **01:00** mark.
- **Smooth scrolling:** scroll progress bar, reveal-on-scroll sections, floating "Send a wish" button and drifting marigold petals.
- **Responsive and accessible:** works on phones and desktops, has visible keyboard focus, and respects `prefers-reduced-motion`.
- **Footer:** "Dev" logo, Instagram / LinkedIn / GitHub / Facebook links and copyright.
## 🛠️ Tech stack
 
| Part | Details |
| --- | --- |
| Markup | HTML5, inline SVG illustrations |
| Styling | Plain CSS (custom properties, grid, flexbox, keyframe animations) |
| Logic | Vanilla JavaScript (IntersectionObserver, Web Share API, Clipboard API) |
| Fonts | Google Fonts: Tiro Devanagari Hindi, Mukta |
| Build tools | None. It is one self-contained file. |
 
## 📁 Project structure
 
```
.
├── index.html     # the whole website (HTML + CSS + JS)
├── README.md
└── assets/        # optional: song file if you move it out of index.html
    └── song.mp3
```
 
> The published version keeps everything inside one HTML file, including the song as a base64 string. Rename `chhath-puja.html` to `index.html` when you add it to your repository.
 
## 🚀 Run locally
 
No installation is needed.
 
```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
# open index.html in your browser, or serve it locally:
python3 -m http.server 8000
# then visit http://localhost:8000
```
 
## 🌐 Deploy on GitHub Pages
 
1. Push `index.html` to the `main` branch.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. After a minute your site is live at `https://<your-username>.github.io/<your-repo>/`.
## 🎨 Customisation
 
**Social links:** search `index.html` for the footer and replace the placeholder links:
 
```html
<a href="https://www.instagram.com/" ...>
<a href="https://www.linkedin.com/" ...>
<a href="https://github.com/" ...>
<a href="https://www.facebook.com/" ...>
```
 
**Share link:** the WhatsApp message uses the address of the page it is opened from. To always share a fixed address, change this line in the script:
 
```js
var SITE = location.href.split("#")[0];
// e.g. var SITE = "https://<your-username>.github.io/<your-repo>/";
```
 
**Wish messages:** edit the `msgs` array in the script to add or change the ready-made wishes.
 
**Song:** the song is stored as a base64 data URI inside `new Audio("data:audio/mpeg;base64,...")`. To keep `index.html` small, save the file as `assets/song.mp3` and replace that string with `"assets/song.mp3"`. To start at a different time, trim the audio file (for example with `ffmpeg -ss 60 -i input.mp4 song.mp3`).
 
**Colours:** change the CSS variables at the top of the `<style>` block (`--night`, `--sindoor`, `--saffron`, `--gold`, `--river`).
 
## ⚠️ Music and copyright
 
The song used on the live site is a commercial recording. Only publish it if you have the right to use it. If you do not, remove the audio, or replace it with music you have permission to use or royalty-free music.
 
## 🌅 Browser support
 
Latest versions of Chrome, Edge, Firefox and Safari. Audio starts only after a tap on the play button, because browsers block autoplay.
 
## 📜 License and copyright
 
Copyright © 2026 **Monu (KINT Sultanpur)**. All rights reserved.
 
Add a `LICENSE` file if you want others to be able to reuse the code.
 
## 🙏 Acknowledgements
 
Made with devotion for the festival of **Surya Dev** and **Chhathi Maiya**. जय छठी मैया! 🌅
