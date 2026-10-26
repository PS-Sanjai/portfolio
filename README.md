# P.S. Sanjai · Portfolio

My personal portfolio site. I'm a sophomore cybersecurity student at Shiv Nadar University, Chennai, and I'm into security, low-level systems, robotics and motorcycles.

The whole site is one HTML file built with plain HTML, CSS and JavaScript. There are no frameworks, no build step and no dependencies to install.

**Live site:** _add your GitHub Pages or Vercel link here_

---

## Highlights

- **Scroll animations everywhere.** Content reveals as you scroll, headings roll in letter by letter, the About paragraph lights up word by word, and the skill chips fly into place.
- **Bike-themed scrolling.**
  - A tiny motorcycle rides along the top progress bar.
  - A speedometer HUD reacts to how fast you scroll, and its gear indicator shifts from N through 6 as you move between sections.
- **Pinned scenes.**
  - A headlight effect fills the screen for the "Break it. Fix it. Secure it. Ride it." motto.
  - The Interests cards slide past sideways while the section stays pinned.
- **Scroll-driven engine.** In the Garage section, a piston, connecting rod and crankshaft turn as you scroll. The engine steps through intake, compression, power and exhaust, with the valves opening and a spark firing.
- **Monochrome design.** The site is black on white and switches to white on black automatically when your system is in dark mode.
- **Accessible.** Animations turn off if you've set "reduce motion" in your OS settings, keyboard focus is always visible, and every section is readable without JavaScript tricks.
- **Responsive.** The layout works on phones; the pinned sideways scroll becomes a normal vertical list on small screens.

## Sections

| Gear | Section | What's there |
|------|---------|--------------|
| N | Home | Name, role and spinning sprockets. A bike rolls in when the page loads. |
| 1 | About | Intro, profile card and quick stats |
| 2 | Interests | Offensive security, chaos engineering, cryptography, bikes, robotics, systems, audio |
| 3 | Skills | Languages, security, core CS and tools |
| 4 | Journey | Timeline with a bike riding down it |
| 5 | Right now | What I'm currently learning |
| 6 | Garage | Four-stroke engine animation and the mechanisms I like |
| N | Contact | Email, GitHub and LinkedIn |

## Tech

- HTML, CSS and vanilla JavaScript in a single `index.html`
- [Google Fonts](https://fonts.google.com/): Bricolage Grotesque, Figtree and Martian Mono
- Inline SVG and `IntersectionObserver` for the animations, all driven by `requestAnimationFrame`

## Run it locally

```bash
git clone https://github.com/PS-Sanjai/<repo-name>.git
cd <repo-name>
```

Then open `index.html` in your browser. If you'd like a local server instead:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

**GitHub Pages**
1. Push `index.html` and `README.md` to the repo.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then pick `main` and `/ (root)`.
4. After a minute, the site is live at `https://ps-sanjai.github.io/<repo-name>/`.

Tip: if you name the repo `ps-sanjai.github.io`, the site is served at `https://ps-sanjai.github.io/`.

**Vercel**
Import the repo at [vercel.com/new](https://vercel.com/new). No configuration is needed because it's a static file.

## Customizing

Everything lives in `index.html`:

- **Colors:** the `:root` CSS variables at the top of the `<style>` block. The light theme comes first and the dark theme sits inside the `prefers-color-scheme: dark` block.
- **Text:** edit the HTML sections directly. Each one has an `id` such as `#about`, `#stack` or `#garage`.
- **Rotating role words:** the `roles` array in the script.
- **Scrolling text strips:** the `w1` and `w2` arrays.
- **Engine speed:** in `drawEngine(ep * 10 * 2*Math.PI)`, the `10` is how many crank turns happen while you scroll through the Garage.

## Contact

- Email: sanjaips1304@gmail.com
- GitHub: [@PS-Sanjai](https://github.com/PS-Sanjai)
- LinkedIn: [Sanjai P.S.](https://www.linkedin.com/in/sanjai-ps-b329aa3a6/)
