# FlickyStream Link addon (WuPlay / Stremio-compatible)

This is a **link-only** starter. It adds one catalog item that opens the FlickyStream website externally.

It does not:
- scrape or copy the site's movie catalog,
- extract or proxy embedded video streams,
- bypass access controls or site restrictions.

A full catalog/playback integration requires a documented interface and permission to use it. Automated reputation services have flagged the domain as suspicious, so use caution and do not download files, install extensions, or enter personal details there.

## Run locally
```bash
python -m pip install -r requirements.txt
python app.py
```
Then check:
- `http://127.0.0.1:7000/health`
- `http://127.0.0.1:7000/manifest.json`
- `http://127.0.0.1:7000/catalog/movie/flicky-home.json`

## Deploy to Render
- Build command: `pip install -r requirements.txt`
- Start command: `gunicorn app:app`
- After deployment, use `https://YOUR-SERVICE.onrender.com/manifest.json` in WuPlay.

## Important
WuPlay may not support externalUrl playback in every build. This is not a movie catalog or in-app playback integration; test it in your version of WuPlay.
