
## Publishing it as a real link (GitHub Pages — free)

1. Go to [github.com/new](https://github.com/new) and create a new
   repository. A good name is `portfolio` (or use `nipu345.github.io` if
   you want your site at the shortest possible URL — see the note below).
2. On your computer, open a terminal in this folder and run:
   ```
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/nipu345/portfolio.git
   git push -u origin main
   ```
   (Replace `portfolio` in the URL if you named the repo something else.)
3. On GitHub, open the repo → **Settings** → **Pages** (left sidebar).
4. Under "Build and deployment", set **Source** to **Deploy from a
   branch**, branch **main**, folder **/(root)**, then **Save**.
5. Wait a minute, then refresh that page — GitHub will show your live
   URL, something like:
   ```
   https://nipu345.github.io/portfolio/
   ```

**About the URL:** any repo name gives you a working link at
`nipu345.github.io/<repo-name>/`. If you specifically want your link to be
just `nipu345.github.io` with nothing after it, name the repository
exactly `nipu345.github.io` in step 1 — GitHub treats that repo name as
special and publishes it at the root domain automatically.

To update the live site later: edit files, then run
```
git add .
git commit -m "Update portfolio"
git push
```
GitHub Pages redeploys automatically within a minute or two.

## Even faster: Netlify Drop (no git required)

If you want a live link right now without setting up git, go to
[app.netlify.com/drop](https://app.netlify.com/drop) and drag this whole
folder onto the page. It gives you a working URL immediately. You can
always move to GitHub Pages later — it's the same files either way.

**Note on Weebly:** Weebly is a drag-and-drop site builder with its own
editor, not a place to upload a folder of HTML/CSS files like this one.
GitHub Pages or Netlify are the natural fit for a hand-coded site like
this; Weebly would mean rebuilding the design inside their tool instead.

## Custom domain (optional)

Both GitHub Pages and Netlify support pointing your own domain name
(like `nikhilpudtha.com`) at the site later, if you ever buy one — the
GitHub Pages "Custom domain" field is right below the settings in step 4
above.
