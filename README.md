# Stewart Lab website

A small multi-page site. Each tab is its own file, so clicking a tab opens a new page
(no long scrolling). No build tools or plugins needed.

## Files
- index.html ............ Home
- research.html ......... Research (the science story)
- publications.html ..... Publications (plain-language summaries + links)
- people.html ........... People
- join.html ............. Join the lab
- styles.css ............ ALL styling and colors (shared by every page)
- images/ ............... put photos here

## Adding photos
Upload image files to the **images/** folder using these names and they appear automatically:
- images/mikaela-stewart.jpg  (People)
- images/brca1-palb2.jpg      (Research, approach one)
- images/celegans.jpg         (Research, approach two)
Until a file exists, that spot shows a labeled placeholder. JPG or PNG; ~1200px wide is plenty.

## Changing words
Open the page you want (e.g. research.html) in any text editor and type. Look for `EDIT`
comments where helpful. To add a publication, copy one `<div class="pub">...</div>` block in
publications.html. To add a team member, copy one `<li>...</li>` in people.html.

## Changing colors
Open **styles.css**. At the top, the `:root` block lists every color once. Change a hex value
(e.g. `--purple`) and it updates across all pages.

## Publishing with GitHub Pages
1. Put all files (and the images/ folder) in one repo.
2. Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
3. Live in ~a minute at https://YOURNAME.github.io/REPO/

## Pointing the old WordPress link here
The free WordPress.com plan can't auto-redirect to an outside site. Options:
- Paid: WordPress.com "Site Redirect" add-on (Upgrades -> Domains).
- Free: replace the old WordPress homepage with a short "We've moved" note and a link here.
- Best long-term: a custom domain pointed at GitHub Pages (Settings -> Pages -> Custom domain).
