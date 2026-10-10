# Toni Nicolas — Portfolio (GitHub Pages + Pages CMS)

A static Jekyll site. GitHub Pages builds it automatically — no build step,
no server, no hosting bill. Content lives in `_data/*.yml`; Pages CMS
gives you a visual editor over those files so you never touch code to
update your work, bio, or experience.

## 1. Push this to GitHub

1. Create a new **public** repo on GitHub, e.g. `toninicolas-portfolio`.
2. From this folder:
   ```
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/toninicolas-portfolio.git
   git push -u origin main
   ```

## 2. Turn on GitHub Pages

1. In the repo: **Settings → Pages**.
2. Under "Build and deployment", set **Source** to "Deploy from a branch".
3. Branch: `main`, folder: `/ (root)`. Save.
4. Your site will be live in a minute or two at:
   `https://<your-username>.github.io/toninicolas-portfolio/`
5. (Optional) Add a custom domain — e.g. `toninicolas.com` — in the same
   Pages settings screen, and point your domain's DNS at GitHub Pages.

## 3. Connect Pages CMS

[Pages CMS](https://pagescms.org) is a free, no-login-for-you-to-host
visual editor that reads/writes directly to your GitHub repo. The
`.pages.yml` file in this repo already defines the editable fields.

1. Go to **app.pagescms.org** and sign in with GitHub.
2. Authorize it to access the `toninicolas-portfolio` repo (you can scope
   the GitHub App to just that one repo).
3. Pages CMS will detect `.pages.yml` automatically and show you three
   editable sections: **Site Content**, **Work / Case Studies**, and
   **Experience** — each with labeled fields (no YAML visible).
4. Edit, click Save — it commits straight to `main`. GitHub Pages rebuilds
   the live site within ~60 seconds.

## File map

- `index.html` — the page template (Liquid), pulls everything from `_data/`
- `_data/site.yml` — hero text, about copy, industries, contact block
- `_data/work.yml` — the 4 case study cards
- `_data/experience.yml` — the experience timeline
- `assets/style.css` — all styling (teal/coral brand, unchanged from the
  portfolio design)
- `.pages.yml` — Pages CMS field definitions (don't need to touch this)

## Updating content without Pages CMS

You can also just edit the `_data/*.yml` files directly in GitHub's web
editor (pencil icon on any file) and commit — same result, just raw YAML
instead of a form.
