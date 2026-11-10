# P.S. Sanjai Portfolio

A single-page portfolio with a neon arcade theme: pixel fonts, a 3D voxel padlock that breaks apart and reassembles as you scroll, and game-style sections (Character sheet, Inventory, Main quest, Training grounds, Quest log, Side quests, Contact).

## Files

- `index.html` is the whole site. The styles and script are inside it.

## View it

Open `index.html` in any modern browser. You need an internet connection the first time, because two things load from the web:

- Fonts from Google Fonts (Pixelify Sans, Chakra Petch, VT323, and Silkscreen for the digit 5)
- three.js r128 from cdnjs, which draws the 3D padlock

Without a connection the page still works, with fallback fonts and no 3D scene.

## Put it online

The site is static, so any static host works. With GitHub Pages:

1. Create a repository named `PS-Sanjai.github.io` (or any repository).
2. Upload `index.html` to the root.
3. In the repository, open Settings, then Pages, and choose the `main` branch as the source.
4. The site appears at `https://ps-sanjai.github.io/` after a minute or two.

Netlify, Vercel and Cloudflare Pages also work: drag the folder in.

## Edit it

Everything is in `index.html`.

- **Text and details:** search for the section by its id: `about`, `skills`, `research`, `coursework`, `journey`, `side`, `contact`.
- **Colours:** change the tokens in the `:root` block at the top of the `<style>` tag (`--pink`, `--cyan`, `--lime`, `--gold`, `--void`).
- **Fonts:** change the Google Fonts links in the `<head>` and the `--display`, `--body` and `--term` tokens.
- **Side quest cards:** each one is an `<article class="px panel">` inside `<div class="track">`. Copy one to add another.
- **3D padlock:** the voxel layout is built in the `initGL` function in the script.

## Notes

- Animations switch off for visitors who have reduced motion turned on in their system settings.
- The phone number from the resume is deliberately left off the site.
