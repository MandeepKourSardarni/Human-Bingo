# 🎉 Human Bingo -- Icebreaker

Break the ice. Build the vibe.  
A single-file web app for quick, fun **Human Bingo** at work, school, workshops, and events — with **Player**, **Host**, and **Bulk printing** modes, pastel-on-dark themes, animated party lights, background music, and one-click exports.

---

## ✨ Features

- **Player mode**
  - Interactive card (3×3, 4×4, 5×5) with **Undo** & **Reset**
  - Smart achievements: line / bottom line / diagonal / house → **confetti** 🎊
  - **Download ticket as PDF** (clean, printable table layout; emoji-free text)

- **Host mode**
  - **Draw Next** prompt from a 50-card deck (no repeats)
  - Live feed of drawn cards
  - **Export drawn cards to CSV** (Excel-friendly: _Serial Number_, _Card_) in draw order

- **Bulk download**
  - Generate **20 / 30 / 40 / 50** tickets, any grid (3×3 / 4×4 / 5×5)
  - **Printable PDF** with **2 tickets per page** (ready to cut and use)
  - Selections are visibly highlighted before generating/printing

- **Look & feel**
  - **Themes:** Blue / Green / Purple (persists via localStorage)
  - Soft neon **string lights** around the viewport
  - Pastel-dark UI, projector-friendly typography
  - Fully responsive (phone / laptop / big screen)

- **Quality of life**
  - **Music selector** (local MP3s), separate **On/Off** control
  - No build tools, no frameworks — just **HTML + CSS + vanilla JS**
  - **jsPDF** under the hood for crisp vector PDFs



---

## 🎨 Customization

- **Themes:** landing page → **Theme** dropdown (Blue / Green / Purple).  
  Stored in `localStorage` as `hb_theme`.
- **Music:** place additional `.mp3` files in `assets/` and add options to the `<select id="musicMode">`.
- **Prompts:** edit the `PROMPTS` array in `index.html` (search `/* Prompts (50) */`).

---

## 🧾 Exports

- **Player → Download PDF:** one ticket per page, clean table grid; emojis are stripped for printer compatibility.
- **Bulk → Download / Print:** two tickets per A4 page (2-up), perfect for cutting.
- **Host → Download Excel (CSV):** columns: _Serial Number_, _Card_ (in the sequence drawn).

---

## 🔧 Tech

- Vanilla **HTML / CSS / JavaScript**
- **jsPDF** for vector PDFs

No bundlers or frameworks required.

---

## 🔒 License & audio

- Code: **MIT License** (feel free to use/modify with attribution).
- Audio: ensure you have the right to use any tracks you add.  
  The app loads local MP3s from `assets/` — swap/replace as needed.

---

## ✅ Accessibility & performance

- High-contrast text on dark gradients
- Large targets for buttons on mobile
- Lightweight, single page — quick loads even offline

---

## 🗺️ Roadmap (nice-to-haves)

- Save/restore player card state between reloads
- Custom prompt sets (upload/import)
- Live host display link for projectors

---

Made with ✨ and a dash of neon.





---


MIT License
Copyright (c) 2025 MandeepKourSardarni
Permission is hereby granted, free of charge, to any person obtaining a copy...

