# Type Page

A free online typewriter that runs entirely in your browser. Write on vintage A4 paper with real typewriter fonts, ink colors, key sounds, and Bangla phonetic typing. No sign-up, no backend, no tracking.

**Live site: https://rifat440.github.io/typewriter/**

## Features

- **A4 sheets.** Every sheet is a fixed A4 page. When a page fills up, typing continues on a new sheet. Use Prev sheet and Next sheet to move between them.
- **Vintage paper.** Aged cream, yellowed letter, ledger, onion skin, and clean sheet.
- **Typewriter fonts.** Courier Prime, Special Elite, a worn "1942 Report" look-alike, Cutive Mono, IBM Plex Mono, Source Code Pro, and a Mixed mode that changes font on every letter.
- **Ink colors.** Eight ink colors plus a custom color picker.
- **Bangla typing.** Phonetic input with automatic conjuncts, plus eight Bangla fonts (and a Mixed mode). Letters never overlap, and word spacing is kept.
- **Word-like cursor.** Click anywhere to place the cursor. Arrow keys, Home, End, Delete, Page Up and Page Down work as expected. Enter splits a line and pushes the rest down. Backspace at the start of a line joins it back.
- **Insert or Overstrike.** Insert pushes text right like a word processor. Overstrike types over existing letters like a real typewriter. The Insert key switches between them.
- **Erase options.** Backspace can erase letters or just move back, and an Eraser tool wipes any letter you click or drag across.
- **Auto capitals** at the start of a line and after `.`, `!` and `?`.
- **Sound.** Key clicks, carriage return, and a margin bell, with a volume control.
- **Copy and paste.** Copy all typed text, or paste text in and have it typed onto the page.
- **Export.** Download the current sheet as a JPEG image, or save everything as a `.txt` file.
- **Private autosave.** Your writing is saved in your own browser (localStorage) and is never uploaded.

## Bangla typing guide

Choose **বাংলা (phonetic)** in the Language menu, then type with English letters.

| Type | Result | Type | Result |
| --- | --- | --- | --- |
| `ami` | আমি | `kh` | খ |
| `bangla` | বাংলা | `Ng` | ঙ |
| `Dhaka` | ঢাকা | `ng` | ং |
| `kot` | কত | `T` / `D` / `N` | ট / ড / ণ |
| `kto` | ক্ত | `.` | । |

Consonants join automatically (`kt` gives ক্ত). Type `o` between two consonants to keep them apart (`kot` gives কত).

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| Enter | Split the line at the cursor (Insert mode) or move to the next line (Overstrike) |
| Backspace | Erase the letter before the cursor, or join with the line above at the start of a line |
| Delete | Erase the letter at the cursor |
| Arrow keys, Home, End | Move the cursor |
| Page Up, Page Down | Previous or next sheet |
| Ctrl/Cmd + Home | Jump to the start of the first sheet |
| Ctrl/Cmd + C, Ctrl/Cmd + V | Copy all text, paste text |
| Insert | Switch between Insert and Overstrike |

## Run locally

It is a single static page. No build step or dependencies.

```bash
git clone https://github.com/rifat440/typewriter.git
cd typewriter
# open index.html in your browser, or serve the folder:
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

The site is hosted with GitHub Pages. To publish your own copy:

1. Push `index.html` and `favicon.svg` to a repository, with `index.html` at the top level.
2. Open Settings, then Pages.
3. Under Build and deployment, choose Deploy from a branch, pick `main` and the `/ (root)` folder, and save.

It also works unchanged on Vercel, Netlify, and Cloudflare Pages.

## Project structure

```
index.html    the whole app (HTML, CSS and JavaScript)
favicon.svg   site icon
robots.txt    crawler rules
vercel.json   security headers (used only on Vercel)
```

## Tech

Plain HTML, CSS and JavaScript. Pages are drawn on HTML canvas, sound uses the Web Audio API, and fonts are loaded from Google Fonts (Courier Prime, Special Elite, Cutive Mono, IBM Plex Mono, Source Code Pro, Noto Sans Bengali, Noto Serif Bengali, Hind Siliguri, Tiro Bangla, Anek Bangla, Baloo Da 2, Galada and Atma), all under open font licenses.

## Privacy

Everything you type stays on your device. Nothing is sent to a server. Autosave uses your browser's local storage, and Clear all removes it.

## License

Add a `LICENSE` file to choose how others may use this code (for example MIT).
