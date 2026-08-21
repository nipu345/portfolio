# Nikhil Pudtha — Portfolio

Plain HTML/CSS, no build tools, no frameworks. Open any `.html` file in a
browser and it just works. Edit it in VS Code (or any editor) and refresh
the browser to see changes.

## Files

```
index.html      Home page
hobbies.html    Hobbies page
projects.html   Projects page
resume.html     Resume page
style.css       All styling, shared by every page
images/         Your photos go here
  profile.jpg        Hero photo (Home page)
  weightlifting.jpg  Hobbies page
  running.jpg        Hobbies page
  coding.jpg         Hobbies page
README.md       This file
```

## Editing text

Every word on the site is plain text inside the `.html` files — open the
page you want to change in VS Code, find the text, edit it, save. No
templating, no build step. For example, to change your bio, open
`index.html` and edit the sentence inside `<p class="hero-bio">...</p>`.

To change colors or fonts, edit `style.css` — the top of the file has a
`:root { ... }` block with named values like `--accent` (the purple used
for buttons and highlights) that control the whole site from one place.

## Adding your photos

Drop your own image files into the `images/` folder using these exact
names, and they'll replace the placeholder graphics automatically:

- `images/profile.jpg` — your headshot, shown on the Home page
- `images/weightlifting.jpg` — Hobbies page
- `images/running.jpg` — Hobbies page
- `images/coding.jpg` — Hobbies page

Any reasonably-sized JPG or PNG works — the CSS crops them to fit. If you'd
rather use `.png` files (or different filenames), update the matching
`src="images/..."` attribute in that page's HTML to match.

## Previewing locally

Just double-click `index.html` to open it in your browser, or in VS Code
install the "Live Server" extension, right-click `index.html`, and choose
"Open with Live Server" for auto-refresh while you edit.

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
