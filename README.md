# Daniel Warner — Portfolio

Personal portfolio site. Single static page (`index.html`) plus an `images/` folder. No build step, no dependencies.

## Run locally
Just open `index.html` in a browser, or serve the folder:
```bash
python3 -m http.server
# then visit http://localhost:8000
```

## Deploy on GitHub Pages
1. Put `index.html` and the `images/` folder at the **root** of your repo (this folder's contents).
2. Commit and push.
3. In the repo on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, pick your branch (e.g. `main`) and `/ (root)`, then **Save**.
4. Your site goes live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

> Tip: for a clean URL like `https://<your-username>.github.io/`, name the repo `<your-username>.github.io`.

## Structure
```
index.html        # the whole site (HTML + CSS + JS inline)
images/           # photo, project screenshots, gallery thumbnails
```
