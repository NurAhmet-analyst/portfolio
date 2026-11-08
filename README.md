# Portfolio (Apple-style): update guide

Everything is in one file, `index.html` (CSS in the `<style>` block at the top, content below). Double-click it to preview; save and refresh after edits.

## Edit content
Search (Ctrl+F) for the words you want to change and edit the text between the tags.
- Headline: `<h1>` · line under it: `<p class="sub">`
- Project: label `<p class="eyebrow">`, name `<h2>`, description `<p class="desc">`, link `href="..."` on `<a class="more">`
- Services: `<h3>` + `<p>` inside `#services` · Tools: `<li>` items inside `<ul class="tools">`
- Contact links: `#contact` · Scroll sentence: `<p>` inside `<section class="statement">`
- The numbers and project names are placeholders. Replace them with your real results.

## Add a project
Copy a whole `<article class="tile"> ... </article>` block. `tile wide` = full width, `tile dark` = black. Tiles are neutral light gray by default (like Apple). To give one a color, add `style="background:#ffe3d6"` to the `<article>` tag.

## Photos and your own pictures
Each tile has a `<div class="visual">` that currently holds an SVG illustration. To show a photo (for example your real Arduino build or a screenshot of your app), replace the whole `<svg> ... </svg>` with:
```html
<img src="images/plant-watering.jpg" alt="My Arduino plant watering system on a desk" loading="lazy">
```
Create an `images/` folder next to `index.html`. Use landscape photos (about 1600 px wide, under 300 KB, JPG or WebP). Free sources for extra images: unsplash.com and pexels.com (check each licence). Real photos of your own builds look best.

## Design
`:root` at the top of the `<style>` block: `--blue` (accent), `--tile` (tile grey), `--ink` (text), `--font`.

## Animations
- Hero text rises in on load (all browsers).
- Scroll animations: hero fades away, tiles scale in, illustrations drift, and the statement sentence turns from gray to white as you scroll. These work in Chrome, Edge and Safari 26+; other browsers show the page without them.
- Everything is under `ANIMATION` at the bottom of the `<style>` block. Delete a line to remove an effect. Visitors with "reduce motion" on see no animation.
- The dashed flow lines and blinking dots in the illustrations use the `.flow` and `.pulse` classes.

## Deploy
Upload the folder (with `images/` if you added one) to Netlify Drop, GitHub Pages or Cloudflare Pages. The file must be named `index.html`.

## Editing the project illustrations
Each illustration is a small animated SVG inside `<div class="visual">`. To change words inside it (for example the sample word "salary", "Class B2 · 97%", or the chat question in the Resume Assistant), search for that text in `index.html` and edit it. Colors are hex values in the SVG: graphite `#1d1d1f`, Apple blue `#0071e3` (`#2997ff` on the dark card). Keep to these so everything stays consistent.
