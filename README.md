# 1QG-1 Furrow-Cleaning Robot — Demo Video

A single-page static site that plays the full-resolution field demonstration video.
Anyone with the link can watch it directly in the browser — no download required.

| File | Size | Purpose |
|---|---|---|
| `index.html` | 4.4 KB | Player page (English), responsive, fullscreen + PiP |
| `video-full.mp4` | 79.2 MB | Full-quality video, 1280×720 / 30 fps / 6.2 Mbps, `+faststart` for progressive streaming |
| `poster.jpg` | 92 KB | Cover frame shown before playback |

The video is the original H.264 stream remuxed only (`ffmpeg -c copy`), so there is **no re-encoding and no quality loss**.

## Deploy on GitHub Pages

1. Create a public repository (e.g. `qinggou-video`).
2. Push these files to the `main` branch:
   ```bash
   git init -b main
   git add .
   git commit -m "1QG-1 furrow-cleaning robot demo"
   git remote add origin https://github.com/<user>/qinggou-video.git
   git push -u origin main
   ```
3. Repository → **Settings** → **Pages** → Source: *Deploy from a branch* → `main` / `(root)` → Save.
4. After ~1 minute the site is live at `https://<user>.github.io/qinggou-video/`.

## Notes

- GitHub hard limit is 100 MB per file, so a 79 MB file must be pushed with git (the web uploader stops at 25 MB).
- GitHub Pages allows a 1 GB repository and 100 MB files; a 79 MB video is within both limits.
- If visitors in mainland China see slow loading, prepend the `gh-proxy` mirror:
  `https://gh-proxy.com/https://<user>.github.io/qinggou-video/`
