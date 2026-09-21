# Happy Birthday, Oluwafolabomi 💗

An interactive birthday storybook — an 11-page flipbook you turn by dragging,
swiping, or using the arrow keys.

## Contents

| File | What it is |
| --- | --- |
| `index.html` | The whole site: markup, styles, script, and every photo/video embedded as base64. No build step, no dependencies. |
| `media/love-me-jeje.mp3` | The soundtrack — Tems, *Love Me JeJe*. Kept as a separate file so it streams instead of delaying the page. |
| `vercel.json` | Vercel config (`cleanUrls`). |

## Viewing it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Music

Browsers will not start audio on their own, so the track begins on the first
gesture that opens the book and fades up under the pages. The note in the top
corner mutes it, and that choice is remembered on the next visit. Music ducks
while the video is playing and pauses when the tab is hidden.

To use a different song, replace `media/love-me-jeje.mp3` — no code changes.

## Publishing

Because it's a single static file, any static host works:

- **Vercel** — import this repo at [vercel.com/new](https://vercel.com/new); no framework, no build command, output directory `.`.
- **GitHub Pages** — Settings → Pages → deploy from the branch root.

## Note

`index.html` is ~16 MB because the photos and the video live inside it as
base64 data URIs. That keeps the project to one portable file, but it means the
whole page downloads before anything renders. To speed it up, the media can be
split into an `assets/` folder and referenced by URL instead.
