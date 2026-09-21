# Happy Birthday, Oluwafolabomi 💗

An interactive birthday storybook — an 11-page flipbook you turn by dragging,
swiping, or using the arrow keys.

## Contents

| File | What it is |
| --- | --- |
| `index.html` | The whole site: markup, styles, script, and every photo/video embedded as base64. No build step, no dependencies. |
| `vercel.json` | Vercel config (`cleanUrls`). |

## Viewing it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publishing

Because it's a single static file, any static host works:

- **Vercel** — import this repo at [vercel.com/new](https://vercel.com/new); no framework, no build command, output directory `.`.
- **GitHub Pages** — Settings → Pages → deploy from the branch root.

## Note

`index.html` is ~16 MB because the photos and the video live inside it as
base64 data URIs. That keeps the project to one portable file, but it means the
whole page downloads before anything renders. To speed it up, the media can be
split into an `assets/` folder and referenced by URL instead.
