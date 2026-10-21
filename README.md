# Shneinu's public pages

Plain HTML for GitHub Pages: the landing page (with the pilot signup, saved
through `pilot_signup`), the pilot's admin page, the privacy policy and the
terms (Hebrew, right-to-left, light and dark). The source lives here in the app's repo for review; the
published copy is the public repo `shneinu-site` (https://shneinu.com, a
custom domain; DNS at Cloudflare).

To publish a change: copy these files into the `shneinu-site` repo and push.

- **The pilot:** one partner signs up for the couple (full name, email, the
  couple's phones, and the Google account of every Android phone). Approve or
  turn down on `admin.html` (sign in with an admin account's email code). The
  `pilot-admin` Edge Function sends the emails through Resend: the TestFlight
  link for a couple with an iPhone, "Android starts soon" for Android, and,
  once the Android testers are in Play Console, "the Android pilot is open".
  The links are saved on the admin page. `npm run waitlist` lists signups too.
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
