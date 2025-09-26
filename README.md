# 🎉 Human Bingo — Icebreaker

Break the ice. Build the vibe.  
A single-file web app for quick, fun **Human Bingo** at work, school, workshops, and events — with **Player**, **Host**, and **Bulk printing** modes, themes, animated party lights, background music, and one-click exports.

---

## 🔗 Live demo

**https://mandeepkoursardarni.github.io/Human_Bingo/**

### 📱 Scan to open
![Open Human Bingo](https://api.qrserver.com/v1/create-qr-code/?size=220x220&data=https%3A%2F%2Fmandeepkoursardarni.github.io%2FHuman_Bingo%2F)


---
## ✨ Features

- **Player mode**
  - Interactive card (3×3, 4×4, 5×5) with **Undo** & **Reset**
  - Smart achievements: line / bottom line / diagonal / house → **confetti** 🎊
  - **Download ticket as PDF** (clean, printable table layout; emoji-free text)

- **Host mode**
  - **Draw Next** from a 50-card deck (no repeats)
  - Live feed of drawn cards
  - **Export drawn cards to CSV** (Excel-friendly): _Serial Number_, _Card_ in draw order

- **Bulk download**
  - Generate **20 / 30 / 40 / 50** tickets, any grid (3×3 / 4×4 / 5×5)
  - **Printable PDF** with **2 tickets per page** (ready to cut)
  - Selections are visibly highlighted before generating/printing

- **Look & feel**
  - **Themes:** Blue / Green / Purple (persists via localStorage)
  - Neon **string lights** around the viewport
  - Pastel-dark UI, projector-friendly typography
  - Fully responsive (phone / laptop / big screen)

- **Quality of life**
  - **Music selector** (local MP3s), separate **On/Off** control
  - No build tools, no frameworks — just **HTML + CSS + vanilla JS**
  - **jsPDF** for crisp vector PDFs

---

## 🚀 Quick start

1. Download or clone the repo.
2. Ensure these files are present:
```

index.html
assets/
cute.mp3
unbreakableresolve.mp3
bensound-ukulele.mp3

````
3. Open `index.html` in your browser. That’s it.

> Browsers block autoplay—click **Music On/Off** once to start audio.

---

## 🔊 Audio setup (assets/ paths)

If your music isn’t playing after moving files into `assets/`, update both the **HTML dropdown** and the **JS defaults** to point to the new path.

**HTML → music dropdown**
```html
<select id="musicMode" class="select" title="Music">
<option value="assets/cute.mp3">Cute (MP3)</option>
<option value="assets/unbreakableresolve.mp3">Unbreakable Resolve (MP3)</option>
<option value="assets/bensound-ukulele.mp3">Bensound Ukulele (MP3)</option>
</select>
````

**JS → defaults** (two places)

```js
// 1) In resetAll()
$('#musicMode').value = 'assets/bensound-ukulele.mp3';
setTrack('assets/bensound-ukulele.mp3');

// 2) In DOMContentLoaded init
setTrack('assets/bensound-ukulele.mp3');
```

**Troubleshooting**

* Folder must be **assets/** (exact spelling; GitHub Pages is case-sensitive).
* After changing paths, click **Music On/Off** once (requires user gesture).
* Optional: show an alert if audio fails:

  ```js
  audio.addEventListener('error', () => {
    alert('Audio file not found. Check the Music dropdown path and that the MP3 exists in assets/.');
  });
  ```

---

## 🌐 Deploy on GitHub Pages

Your live site is already here:
**[https://mandeepkoursardarni.github.io/Human_Bingo/](https://mandeepkoursardarni.github.io/Human_Bingo/)**

If you change repos later:

* Repo → **Settings → Pages**
* **Build and deployment**: *Deploy from a branch*
* Branch: `main`, Folder: `/ (root)`

---

## 🗂️ Project structure

```
Human_Bingo/
├─ index.html
└─ assets/
   ├─ cute.mp3
   ├─ unbreakableresolve.mp3
   └─ bensound-ukulele.mp3
```

---

## 🎨 Customization

* **Themes:** landing page → **Theme** dropdown (Blue / Green / Purple).
  Stored in `localStorage` as `hb_theme`.
* **Music:** add more `.mp3` files under `assets/` and add options to `<select id="musicMode">`.
* **Prompts:** edit the `PROMPTS` array in `index.html` (search `/* Prompts (50) */`).

---

## 🧾 Exports

* **Player → Download PDF:** one ticket per page; emojis stripped for printer safety.
* **Bulk → Download / Print:** two tickets per A4 page (2-up).
* **Host → Download Excel (CSV):** columns: *Serial Number*, *Card*.

---

## 🔧 Tech

* Vanilla **HTML / CSS / JavaScript**
* **jsPDF** for vector PDFs

---

## 🔒 License & audio

* Code: **MIT License** (feel free to use/modify with attribution).
* Audio: ensure you have the right to use any tracks you add.
  The app loads MP3s from `assets/`.

---

Made with ✨ and a dash of neon.

```
