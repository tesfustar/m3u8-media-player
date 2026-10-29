# m3u8-player

Minimal full-screen HLS (`.m3u8`) video player. No UI — just the video.

## Usage

Open `index.html` with the stream URL as a query param:

```
index.html?url=https://example.com/stream/playlist.m3u8
```

`?src=` and `?m3u8=` also work. URL-encode the stream link if it has its own query string.

- Uses [hls.js](https://github.com/video-dev/hls.js) in Chrome/Firefox/Edge, native HLS in Safari/iOS.
- Autoplays (muted if the browser blocks sound); click/tap/key press unmutes and enters fullscreen.

## Run locally

```
npx serve .
```

Works on any static host (e.g. GitHub Pages).
