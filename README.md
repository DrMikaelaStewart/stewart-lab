# Stewart Lab website

A small multi-page site. Each tab is its own file, so clicking a tab opens a new page
(no long scrolling). No build tools or plugins needed.

> Logo: two versions live in `images/`. **`logo-light.png`** is the transparent, light-background
> mark — it's the hero image on the homepage and the logo in every footer, so it sits cleanly on
> the light pages with no dark box. **`logo.png`** is the original black-background artwork, kept
> only for the browser-tab favicons (`favicon-32.png`, `favicon-48.png`, `apple-touch-icon.png`,
> all generated from it). The top navigation still uses the small inline *C. elegans* worm mark —
> to restyle that one, search a page for `class="mark"`. If you re-export the logo later, keep a
> transparent PNG for on-page use and a square one for the favicons.

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
Upload image files to the **images/** folder. A few fixed names are wired into specific spots:
- images/mikaela-stewart.jpg   (In Action page, PI bio)
- images/brca1-palb2.jpg       (Research, approach one — the molecular handshake)
- images/celegans.jpg          (Research, approach two — the off switch / the worm)

Everything else lives in the **Life-in-the-lab gallery** on the In Action page (people.html).
To add a gallery photo, drop the image in images/ and copy one `<figure class="shot">` block
inside `<div class="gallery">`. New (most recent) photos go at the top:

```html
<figure class="shot"><button type="button" class="shot-btn">
  <img src="images/your-photo.jpg" alt="short description" loading="lazy"></button>
  <figcaption><span class="when">Spring 2026</span> Your caption here.</figcaption></figure>
```

The little `<span class="when">…</span>` season tag is optional — leave it off and the caption
still works. Photos ~1200–1600px wide, JPG or PNG, keep file sizes web-friendly (a few hundred KB).

## Scan-to-visit QR card
`images/qr-card.png` is the branded scan card (logo, a QR with the worm-in-orbit mark in its
center, a one-line description, the URL, and the lab tagline) that opens **stewartresearchlab.com**.
It appears as a small card in every page footer; clicking it opens an enlarged, easy-to-scan view.
`images/qr.png` is the standalone QR (worm-and-hexagon center) on its own, in case you want just
the code. To point the QR somewhere else (e.g. LinkedIn), regenerate both PNGs for the new URL.
A print-resolution version of the card is kept outside the site as `stewart-lab-qr-card.png`.

## Contact details (footer)
Every page footer shows the logo, the lab's address, a gradient **Connect on LinkedIn** button,
and the scan-to-visit QR card; the **Contact** link in the top toolbar jumps there. To edit,
search any page for `footer id="contact"` — the address (Winton Scott Hall, Suite 521) and the
LinkedIn link live right there. Copyright shows `2017–<current year>` and the year fills in
automatically.

## Changing words
Open the page you want (e.g. research.html) in any text editor and type. To add a publication,
copy one `<div class="pub">...</div>` block in publications.html. To add a team member, copy
one `<li>...</li>` in people.html.

## Changing fonts and colors
Open **styles.css**. The type system is now two workhorse faces plus one rare accent:
**Fraunces** for all headings, **Inter** for body text *and* every small label (tags, roles,
venues, photo captions, the season tags), and **Space Mono** reserved only for the `.eyebrow`
kicker that sits above section titles — the one signature accent, echoing the logo. All three
load once via the `<link>` in each page `<head>`. The `:root` block at the top of styles.css
lists every color once; change a hex value (e.g. `--purple`) and it updates across all pages.
The hero shimmer respects "reduced motion" settings and freezes to a solid color for visitors
who prefer that.

## Publishing with GitHub Pages
1. Put all files (and the images/ folder) in one repo.
2. Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
3. Live in ~a minute at https://YOURNAME.github.io/REPO/

## Pointing the old WordPress link here
The free WordPress.com plan can't auto-redirect to an outside site. Options:
- Paid: WordPress.com "Site Redirect" add-on (Upgrades -> Domains).
- Free: replace the old WordPress homepage with a short "We've moved" note and a link here.
- Best long-term: a custom domain pointed at GitHub Pages (Settings -> Pages -> Custom domain).
