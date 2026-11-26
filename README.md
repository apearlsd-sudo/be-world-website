# BE World Company Ltd — Website

Static marketing site for BE World Company Ltd (mining · quarry mining ·
agriculture · freight forwarding). No build step, no frameworks — plain
HTML/CSS/JS with all images hosted in `assets/img/`.

## Publish with Netlify Drop (~1 minute)

1. Log in at app.netlify.com (or create the free account) and open
   **https://app.netlify.com/drop**.
2. Drag this **whole folder** onto the page. Netlify uploads it and the site
   is live within seconds at `https://<random-name>.netlify.app`.
3. Optional — cleaner URL: **Site configuration → Change site name**, e.g.
   `be-world-company` → `https://be-world-company.netlify.app`.
   HTTPS is automatic.

Updating the site later: drag the updated folder onto the existing site's
**Deploys** page — it replaces the current deploy and **keeps the same URL**.
(Dropping on app.netlify.com/drop again would create a new site with a new
URL, so use the Deploys page for updates.)

## Publish with GitHub Pages (alternative)

1. On github.com click **New repository** → name it e.g. `be-world-website`,
   set **Public**, do **not** add a README (we already have one) → **Create**.
2. On the new repo page click **uploading an existing file**, drag in ALL files
   from this folder (`index.html`, the other 7 `.html` pages, `assets/`, and the
   hidden `.nojekyll` — enable "show hidden files" in your file manager, or
   create it via Add file → Create new file, named exactly `.nojekyll`,
   left empty).
3. Click **Commit changes**.
4. Go to **Settings → Pages**, set Source = **Deploy from a branch**, Branch =
   `main` / `/(root)`, then **Save**.
5. After 1–2 minutes your site is live at:
   `https://<your-username>.github.io/be-world-website/`

With git instead of the web upload:

```bash
git init
git add .
git commit -m "BE World Company Ltd website"
git branch -M main
git remote add origin https://github.com/<your-username>/be-world-website.git
git push -u origin main
```

Then enable Pages as in step 4 above.

## Notes

- `.nojekyll` only matters for GitHub Pages (it skips Jekyll processing);
  Netlify ignores it harmlessly. Keep it in the folder.
- All links and image paths are relative, so the site works at a subpath and
  on any domain. The only external reference is the Google Maps embed on the
  contact page.
- The contact form is front-end only. Point it at Formspree/Web3Forms or your
  CRM before going live (edit the `<form>` in `contact.html`).
- Stats, phone numbers, email and address in the pages are placeholders —
  search the HTML for them and replace with real company data.
