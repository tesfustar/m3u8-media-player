# m3u8-player

Minimal full-screen HLS (`.m3u8`) video player. Just the video with the browser's native controls.

## Usage

Open `index.html` with the stream URL as a query param:

```
index.html?url=https://example.com/stream/playlist.m3u8
```

`?src=` and `?m3u8=` also work. URL-encode the stream link if it has its own query string.

- Uses [hls.js](https://github.com/video-dev/hls.js) in Chrome/Firefox/Edge, native HLS in Safari/iOS.
- Autoplays with sound. If the browser blocks sound (it does until a viewer has interacted with the site), it plays muted with a "Tap for sound" button; the first click/tap/key press anywhere unmutes and enters fullscreen.
- Connects to the stream server and fetches the playlist while hls.js is still loading, for a faster start.

## Run locally

```
npx serve .
```

Works on any static host (e.g. GitHub Pages).
