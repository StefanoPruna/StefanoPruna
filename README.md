# Stefano Pruna Portfolio

A static portfolio site, ready for GitHub Pages. No build step: plain HTML and CSS.

```
index.html        the page
css/style.css     all styling (light and dark mode)
assets/clips/     put gameplay clips and screenshots here
.nojekyll         tells GitHub Pages to serve the files as they are
```

## Publish it on GitHub Pages

1. Create a new **public** repository on GitHub.
   * Name it `<your-username>.github.io` to get the address `https://<your-username>.github.io`
   * Or give it any name (for example `portfolio`) to get `https://<your-username>.github.io/portfolio`
2. Upload the contents of this folder to the repository (Add file > Upload files, drag everything in, commit).
   Make sure `index.html` sits at the top level of the repository, not inside a subfolder.
3. Go to **Settings > Pages**. Under "Build and deployment" choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. Wait a minute or two, then open the address shown at the top of the Pages settings.

Every later commit to `main` updates the live site automatically.

Optional: to use your own domain, add it under Settings > Pages > Custom domain and follow GitHub's DNS instructions.

## Before sharing it

- [ ] Record the four Oceans Palette clips (see below) and swap them in
- [ ] Confirm with Khrönmière Entertainment what can be shown publicly about Project Adam
- [ ] Add an email address and GitHub link to the Contact section
- [ ] Read through every description and fix anything inaccurate
- [ ] Add the site link to the CV, LinkedIn (Featured section) and itch.io profile

## Adding a clip

Keep clips short (15 to 60 seconds), MP4 (H.264), 1280x720 or 1920x1080, ideally under 10 MB each.
Save them in `assets/clips/`, for example `assets/clips/coral-grow.mp4`.

In `index.html`, find the placeholder for that system. It looks like this:

```html
<div class="viewport" role="img" aria-label="Placeholder for coral grow system clip">
  ...
</div>
```

Replace the whole block with:

```html
<video class="viewport" src="assets/clips/coral-grow.mp4" autoplay muted loop playsinline
       aria-label="Coral grow system: pickup, placement and growth"></video>
```

For a screenshot instead of a video use:

```html
<img class="viewport" src="assets/clips/menu.png" alt="Main menu built with MenuButtonBase widgets">
```

Suggested file names: `coral-grow.mp4`, `swimming.mp4`, `menus.mp4`, `camera.mp4`.

If a clip is over about 50 MB, upload it to YouTube instead and link to it.
