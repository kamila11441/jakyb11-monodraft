# Jakub Kowalski — @jakyb11 Photography Portfolio

A dark, editorial title page with a photo-first gallery. The gallery is loaded from `content/gallery.json`, so the creator can update the collection through the CMS once authentication is configured. Visitors can only view and filter photos.

## Preview locally
Because the gallery loads JSON with `fetch`, run this through a local web server rather than opening `index.html` directly. For example, with Python installed, run `python3 -m http.server 8000` from this folder, then open `http://localhost:8000`.

## Publish on GitHub Pages
1. Create a GitHub repository and upload all files.
2. In repository settings, enable GitHub Pages from the main branch and root folder.
3. Replace the placeholder repository in `admin/config.yml`.

## Creator editing / CMS
The editor lives at `/admin/`. It can add, remove, reorder, categorize and caption images. Configure an OAuth provider for Decap CMS before relying on the GitHub backend; GitHub Pages by itself does not provide secure CMS login. The CMS config is a starter configuration, not a turnkey authenticated login. If you prefer simpler setup, host the repository on Netlify and configure its Git Gateway, updating the backend config accordingly.

## Gallery image format
Each item in `content/gallery.json` has `image`, `alt`, and `category` fields. Supported categories: `people`, `places`, `fashion`, `other`. You can use hosted image URLs or upload images to the repository and reference their relative path.
