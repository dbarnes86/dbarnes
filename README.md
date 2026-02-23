# danbarnes.com

Personal site for Daniel Barnes — General Manager, Games & Interactive Entertainment.

## Deployment to GitHub Pages

### First time setup

1. Create a new repository on GitHub named `danbarnes.github.io` (or any name — see note below)
2. Clone the repo locally or upload files directly via GitHub web interface
3. Add `index.html` and `photo.jpg` (your headshot) to the root of the repo
4. Go to **Settings → Pages**
5. Under **Source**, select `Deploy from a branch`
6. Select `main` branch, `/ (root)` folder
7. Click **Save**
8. Your site will be live at `https://danbarnes.github.io` within a few minutes

### Using a custom domain (danbarnes.com)

1. In your repo root, create a file called `CNAME` containing exactly:
   ```
   danbarnes.com
   ```
2. In your domain registrar (wherever danbarnes.com is registered), update DNS:
   - Add 4 A records pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Add a CNAME record: `www` → `danbarnes.github.io`
3. In GitHub Pages settings, enter `danbarnes.com` as your custom domain
4. Check **Enforce HTTPS** once DNS has propagated (can take up to 24 hours)

### Adding your photo

Name your headshot `photo.jpg` and place it in the root folder alongside `index.html`.

The site will automatically display it in the hero section. If the file is missing, a clean placeholder shows instead.

### Updating content

All content is in `index.html`. It is a single self-contained file with no build process, no dependencies, no framework. Open it in any text editor, make changes, save, push to GitHub. The site updates within 1-2 minutes.

## That's it

No npm. No build step. No CMS. Just one HTML file.
