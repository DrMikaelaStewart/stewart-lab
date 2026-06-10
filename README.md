# Stewart Lab website

A small multi-page site. Each tab is its own file, so clicking a tab opens a new page
(no long scrolling). No build tools or plugins needed.

> Logo: the site mark is a little *C. elegans* worm, drawn inline as SVG in each page's
> header and footer (and as the browser-tab favicon). To restyle it, search a page for
> `class="mark"`. A standalone `logo.svg` / `logo.png` are included for slides or letterhead.

## Files
- index.html ............ Home (hero tagline has an animated shimmer)
- research.html ......... Research (the science story — two complementary approaches)
- publications.html ..... Publications (plain-language summaries + links)
- people.html ........... "In Action" tab (PI bio + life in the lab gallery)
- join.html ............. Join the lab
- styles.css ............ ALL styling and colors (shared by every page)
- images/ ............... put photos here

Note: the tab reads **In Action** but the file is still `people.html` (so existing links keep working).

## Adding photos
Upload image files to the **images/** folder using these names and they appear automatically:
- images/mikaela-stewart.jpg   (In Action page)
- images/brca1-palb2.jpg       (Research, approach one — the molecular handshake)
- images/celegans.jpg          (Research, approach two — the off switch / the worm)
- images/lab-*.jpg, conf-*.jpg (Life-in-the-lab gallery on the In Action page)
JPG or PNG; ~1200px wide is plenty.

## Contact details (footer)
Every page footer links to the lab's address and LinkedIn, and the **Contact** link in the
top toolbar jumps there. To edit, search any page for `footer id="contact"` — the address
(Winton Scott Hall, Suite 521) and the LinkedIn button live right there. Copyright shows
`2017–<current year>` and the year fills in automatically.

## Changing words
Open the page you want (e.g. research.html) in any text editor and type. To add a publication,
copy one `<div class="pub">...</div>` block in publications.html. To add a team member, copy
one `<li>...</li>` in people.html.

## Changing fonts and colors
Open **styles.css**. The site uses three typefaces only — Fraunces (headings), Inter (body),
and Space Mono (small labels) — loaded once via the `<link>` in each page `<head>`. The `:root`
block at the top of styles.css lists every color once; change a hex value (e.g. `--purple`)
and it updates across all pages. The hero shimmer respects "reduced motion" settings and
freezes to a solid color for visitors who prefer that.

## Publishing with GitHub Pages
1. Put all files (and the images/ folder) in one repo.
2. Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
3. Live in ~a minute at https://YOURNAME.github.io/REPO/

## Pointing the old WordPress link here
The free WordPress.com plan can't auto-redirect to an outside site. Options:
- Paid: WordPress.com "Site Redirect" add-on (Upgrades -> Domains).
- Free: replace the old WordPress homepage with a short "We've moved" note and a link here.
- Best long-term: a custom domain pointed at GitHub Pages (Settings -> Pages -> Custom domain).
