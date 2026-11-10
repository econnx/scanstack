# ScanStack

Phone photos of your notebook → one clean PDF, ready to submit to Moodle, Google Classroom or any LMS.

**Try it:** https://econnx.github.io/scanstack/

- **Clean scan**: removes shadows and uneven lighting, whitens the paper, keeps pencil readable
- **Black & white** mode for the smallest files, **Original** if you want the photo as is
- Reorder (drag or ← →), rotate, remove pages
- A4 pages, three size presets (≈150 / 200 / 300 dpi); six pages are usually 1–3 MB
- Runs entirely in your browser. Nothing is uploaded, there is no server.

## How the clean scan works

For every page it estimates the brightness of the bare paper: the photo is shrunk to 40 px wide (thin ink lines vanish, the lighting stays), a 3×3 max filter lifts dense writing, and the result is scaled back up smoothly. Each pixel is then divided by that estimate, so a shadow that darkens both the paper and the ink by 30% cancels out. A contrast curve makes faint grid lines fade and ink go dark.

## Run locally

It is one HTML file. Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```

`index.html?demo` loads three synthetic pages with a fake phone shadow, handy for testing.

## License

MIT
