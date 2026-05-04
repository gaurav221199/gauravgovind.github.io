# Gaurav Govind — Personal Website

A minimalist personal site built as a single `index.html` file. No build step, no dependencies — just open it or push it to GitHub Pages.

## Deploy to GitHub Pages

Your site will live at `https://<your-username>.github.io` once deployed.

### Step 1 — Create the repository

1. Sign in to [GitHub](https://github.com).
2. Click **New repository** (top right `+` icon → New repository).
3. Name it **exactly**: `<your-username>.github.io`
   (e.g. if your GitHub username is `gauravgovind99`, the repo must be `gauravgovind99.github.io`)
4. Set it to **Public**.
5. Do **not** initialise with a README (you already have these files).
6. Click **Create repository**.

### Step 2 — Push your files

Open a terminal in the folder containing `index.html` and run:

```bash
git init
git add index.html README.md
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

Replace `<your-username>` with your actual GitHub username (twice).

### Step 3 — Enable Pages

1. In your repo on GitHub, go to **Settings → Pages**.
2. Under **Source**, select **Deploy from a branch**.
3. Choose **Branch: main** and **Folder: / (root)**, then click **Save**.
4. Wait 1–2 minutes. Refresh the Pages settings page — you'll see a green tick and the live URL.

Visit `https://<your-username>.github.io` and your site is live.

## Updating the site

Edit `index.html` locally, then:

```bash
git add index.html
git commit -m "Update content"
git push
```

Changes appear within ~30 seconds.

## Customising

Everything is in one file (`index.html`). Common edits:

- **Colors** — change the CSS variables at the top of the `<style>` block (`--accent`, `--bg`, etc.)
- **Projects** — duplicate any `<article class="project">` block to add more.
- **Frameworks/tags** — edit the `<span class="chip">` and `<span class="tag">` elements.
- **Contact links** — find the `id="contact"` section near the bottom.

## Custom domain (optional)

If you own a domain (e.g. `gauravgovind.com`):

1. Add a file named `CNAME` in the repo root containing only your domain (no `https://`, no path).
2. In your domain registrar's DNS settings, add an `A` record pointing to GitHub's IPs:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. In **Settings → Pages**, enter your domain under **Custom domain** and tick **Enforce HTTPS**.

DNS can take up to 24 hours to propagate.
