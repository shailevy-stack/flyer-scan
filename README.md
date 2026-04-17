# Flyer Scan

A minimal PWA that reads event flyers with Claude vision and outputs formatted text that iOS recognises as a tappable calendar date.

## Setup

1. Open `index.html` and replace `YOUR_API_KEY_HERE` with your Anthropic API key (line ~180)
2. Push to GitHub Pages (or any static host)
3. On iPhone: open in Safari → Share → Add to Home Screen

## Usage

1. Tap the app from home screen
2. Drop a flyer image, use Camera, or pick from Gallery
3. Tap **Scan Event**
4. Long-press the date in the result to create a calendar entry natively in Apple Calendar

## Notes

- The app uses `claude-opus-4-5` for best vision accuracy — swap to `claude-haiku-4-5` to save on cost if you scan a lot
- No data is stored; images are sent directly to the Anthropic API and discarded
- Works offline only after initial load (no service worker — keep it simple)

## Files

```
index.html     — the entire app
manifest.json  — PWA manifest for home screen install
icon-192.png   — home screen icon (add your own)
icon-512.png   — large icon (add your own)
```
