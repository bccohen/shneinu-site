# Shneinu's public pages

Plain HTML for GitHub Pages: the landing page, the join page for invitation
links, the pilot's admin page, the privacy policy and the terms (Hebrew, right-to-left, light and dark). The source lives here in the app's repo for review; the
published copy is the public repo `shneinu-site` (https://shneinu.com, a
custom domain; DNS at Cloudflare).

To publish a change: copy these files into the `shneinu-site` repo and push.

- **The pilot (open to anyone since Nov 7, 2026):** no signup and no
  approvals. `index.html` and `join.html` show the links to every visitor:
  iPhone, TestFlight's public link; Android, the Google Group
  `shneinu-testers` (Play's closed test admits its members) and then Play's
  opt-in link. The links are written in both pages; if one changes, change it
  there and on `admin.html` (which feeds the app's update screen and the
  "new iPhone version" email to couples who signed up before).
- **The landing page is short and to be played with:** the hero, a reveal to
  try (pick an answer, see Noam's), the tree (grow it, let it wilt; the mascot drawn from
  `src/lib/tree.ts` into `art/tree/STAGE-WILT.svg` by `node scripts/site-tree.mjs`), question tiles that
  change on tap, and the download steps. No feature lists.
- **At launch:** put the two store links in `STORES` at the top of the script
  in `index.html` and `join.html`. The pilot steps turn into store buttons (a
  phone sees its own store first). Then check the FAQ and its copy in the
  JSON-LD at the top.
- **Phones:** nothing may stick out sideways. In right-to-left pages the
  browser scrolls to whatever sits past the left edge, so a phone could zoom
  out into empty space. Hide things in place, never with `left: -10000px`; `style.css` also clips sideways overflow.
- **Search:** `robots.txt`, `sitemap.xml` (update `lastmod` when a page
  changes), `og.png` (the link preview, drawn from `marketing/og/og.html`),
  and the JSON-LD in `index.html`.
- **Pictures:** `img/today.jpg` is the store screenshot of Today
  (`marketing/screenshots/raw/today.png`, 600 px JPEG); `art/` are copies of
  `assets/art`; `art/tree/` is the tree in every stage (1–7) and wilt (0–3).
