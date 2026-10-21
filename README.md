# Shneinu's public pages

Plain HTML for GitHub Pages: the landing page (with the pilot signup, saved
through `join_pilot`), the privacy policy and the terms (Hebrew, right-to-left,
light and dark). The source lives here in the app's repo for review; the
published copy is the public repo `shneinu-site` (https://shneinu.com, a
custom domain; DNS at Cloudflare).

To publish a change: copy these files into the `shneinu-site` repo and push.

- **Pilot signups:** `npm run waitlist` lists them with the phone (iPhone →
  TestFlight, Android → the Google Play closed test, by that Gmail address).
- **At launch:** put the two store links in `STORES` at the top of the script
  in `index.html`. The forms turn into download buttons (a phone sees its own
  store first). Then reword the FAQ and its copy in the JSON-LD at the top,
  which still talk about the pilot.
- **Phones:** nothing may stick out sideways. In right-to-left pages the
  browser scrolls to whatever sits past the left edge, so a phone could zoom
  out into empty space. Hide things in place (see `.trap`), never with
  `left: -10000px`; `style.css` also clips sideways overflow.
- **Search:** `robots.txt`, `sitemap.xml` (update `lastmod` when a page
  changes), `og.png` (the link preview, drawn from `marketing/og/og.html`),
  and the JSON-LD in `index.html`.
- **Pictures:** `img/` are the store screenshots (`marketing/screenshots/raw`,
  600 px JPEG); `art/` are copies of `assets/art`.
