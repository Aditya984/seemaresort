# Changelog

All notable changes to the Seema's Resort website are recorded here, newest first.
Dates are written as YYYY-MM-DD. For changes before 2026-10-22, see the repository commit history.

---

## 2026-10-31 — New Year's Eve bookings live (prices final)

**Swapped in:** the full-detail version (formerly `index-nye-bookings-live.html`) is now `index.html`. The "Bookings opening soon" teaser and countdown are gone.

**Rates now match the official poster:** party entry with unlimited food ₹1,200 per person (was ₹1,199); couple booking ₹4,500 onwards (was ₹4,000 to ₹6,000); dormitory ₹2,800 to ₹3,000, triple ₹3,200 to ₹3,600 and quadruple ₹3,000 to ₹3,500 unchanged. The ribbon now says "Stay from ₹2,800 per person", and the Event JSON-LD offers use ₹1,200 and a ₹2,800 minimum with no maximum.

**Link preview:** `og:` and `twitter:` title, description and image show the live NYE offer with prices. New image `images/og-nye-live.jpg` (1200x630, "Booking starts now", party entry ₹1,200, stays from ₹2,800); the old `images/og-nye.jpg` still says "Bookings opening soon" and is no longer used. A new file name is used on purpose so WhatsApp and Facebook fetch a fresh preview. Restore the originals after 1 Jan 2027 (see the 2026-10-30 entry).

**Sitemap:** `lastmod` set to 2026-10-31.

---

## 2026-10-30 — New Year's Eve 2026-27 update (teaser mode, no prices)

**Link preview (WhatsApp, Facebook, X):** `og:title`, `og:description`, `og:image` (new `images/og-nye.jpg`, 1200x630) and the matching `twitter:` tags now show the NYE teaser. After 1 Jan 2027, restore title `Seema's Resort Neral | Best Pool Resort & Cottages Near Matheran & Karjat`, the original description (same as `<meta name="description">`) and `images/og-image.jpg`, and update the `og:image:alt`.

**Teaser mode:** until bookings open, the ribbon and `#nye` section show a "Bookings opening soon" hype message with a countdown, highlights and WhatsApp/call buttons. No prices, packages, policy or offers are shown, the dropdown has one NYE enquiry option, and the Event JSON-LD has no offers. The full-detail version is kept in `index-nye-bookings-live.html` to swap in when bookings open.


**Added (all in `index.html`, every piece wrapped in `NYE START` / `NYE END` comments):**
- Announcement ribbon above the header with a "View details" link to `#nye`.
- New `#nye` section above `#rooms`: stay packages, party entry, kids rates, gala menu, entertainment, timings, advance and cancellation policy, WhatsApp and call buttons.
- "NYE Party" link in the header navigation.
- New Year's Eve options in the booking form's room preference dropdown (works with both the WhatsApp and email buttons).
- `Event` JSON-LD for the 31 December 2026 party.
- `.nye-head` and `.nye-card` added to the `revealTargets` list (content stays visible to crawlers).
- `sitemap.xml` `lastmod` set to 2026-10-30.

**To remove after 1 January 2027:** delete everything between the `NYE START` and `NYE END` comments (CSS, ribbon, section, dropdown group, Event JSON-LD), the `NYE Party` nav link line, and `,.nye-head,.nye-card` in `revealTargets`. Then update `lastmod` again.

---

## 2026-10-22 — Technical SEO upgrade

Goal: rank higher on Google Search and Google Maps for "resort in Neral", "resort near Matheran / Karjat", weekend getaways from Mumbai and Pune, couple cottages, pool resorts and group outings.

**Not changed:** the visual design, CSS theme, room image carousels, the WhatsApp booking flow and the Web3Forms email form all work exactly as before.

### Changed — `index.html`

**Page title, description and brand**
- `<title>` is now: *Seema's Resort Neral | Best Pool Resort & Cottages Near Matheran & Karjat*
- Meta description (also used for Open Graph and Twitter cards) now names the highway, Matheran, the room types, the pool, rain dance and the AP buffet.
- `robots` meta now allows large image previews and unlimited text and video snippets: `index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1`.
- Brand name standardised to **Seema's Resort & Restaurant** (alternates: "Seema Resort", "Seema's Resort Neral") in the meta tags, structured data, logo alt text and footer.

**Headings** (search engines weight these heavily)

| Section | Old | New |
|---|---|---|
| Hero `<h1>` | Right on the highway. Best resort in Neral, near Karjat. | Seema's Resort & Restaurant, Neral — Best Pool Resort & Cottages Near Matheran & Karjat |
| Route strip | No detour required — we're right on the road | Highway-Touch Resort on Neral-Karjat Road — 1.5 to 2 Hrs from Mumbai & Pune |
| Check-in slots | Pick whichever slot fits your drive | Flexible Check-In Slots & Unlimited Buffet (AP Meal Plan) |
| Rooms | Featured rooms — plus more categories to choose from | AC Cottages, Couple Suites, Family Rooms & Dormitories in Neral |
| Amenities | Enough to fill a weekend without leaving the property | Resort with Swimming Pool, Rain Dance & Outdoor Games in Neral |
| Stays | A resort near Karjat for families, couples and groups | Family Stays, Couple Getaways & Group Outings Near Matheran & Karjat |
| Good to know | The fine print, before you book | Buffet Dining, Pool Timings & Resort Booking Policies |
| Gallery | Around the resort | Photos of Our Swimming Pool, Hill-Facing Rooms & AC Dining Hall |
| Reviews | What our guests say on Google | Guest Reviews for Seema's Resort Neral |
| Booking | Find us, then stop looking at the map | Location, Directions & Direct Room Booking — Seema's Resort Neral |
| FAQ | Frequently asked questions | Frequently Asked Questions About Seema's Resort Neral |

- The hero heading is now a two-tier heading (bigger name, smaller gold line) and the hero text box is 60px wider, so the longer text fits.

**FAQ**
- 4 new questions added, to both the visible FAQ and the `FAQPage` structured data (now 11 in total):
  distance from Neral station and Matheran, couple-friendly policy and ID, outdoor activities and games, and dormitories for groups and corporate outings.

**Getting there**
- The "Getting there" text under the booking section now covers road and train access, including the 3 km (5–10 min by auto-rickshaw) trip from Neral station.

**Image alt text**
- All 13 photos and the logo now have descriptive alt text: what the photo shows, plus "at Seema's Resort Neral near Matheran & Karjat".

### Added — structured data (JSON-LD)
- Business type is now `Resort` + `LodgingBusiness` + `Restaurant`, with `servesCuisine`.
- The 4 featured rooms (Deluxe Suite Couple Cottage, Elite Room, Couple Deluxe Premium Room, Family Executive Room) are listed as rooms with an `Offer` for the AP plan and one for room only, in INR (₹2,800 to ₹7,500).
- New amenities: Rain Dance, Kids' Pool, Kids' Play Area, Dormitories for Groups, Hill-Facing Rooms, Unlimited Veg & Non-Veg Buffet, On-site Restaurant.
- The 9 Google reviews shown on the page are included as `Review` objects (5 stars each).
- Logo, pets-not-allowed flag and more image URLs added.

### Fixed — content hidden from Googlebot
- **Problem:** about 80% of the page started at `opacity: 0` and was only revealed when scrolled into view. Crawlers that do not scroll could treat that content as hidden.
- **Fix:** nothing is hidden in the static HTML/CSS any more. A small script in `<head>` turns the fade-in animation on only for real browsers (not crawlers, headless tools or reduced-motion users), and only for blocks below the first screen. If a visitor does not scroll within 5 seconds, everything is revealed anyway.
- Tested: with a Googlebot user agent, 0 content blocks are hidden.

### Removed — test game
- The "Games" nav link, the whole `#play` section (Memory Match and Tic-Tac-Toe), its CSS and its JavaScript. This was test-only code that added weight and distracted from the page's keywords.

### Changed — `sitemap.xml`
- `lastmod` set to 2026-10-22.
- Now lists all 13 resort photos (pool, hill rooms, dining hall and every room photo) with descriptive `<image:title>` tags.

### Changed — documentation
- `README.md` rewritten: SEO features, a "keep these in sync" table, the animation rule, image and sitemap rules, a monthly SEO checklist.
- Wiki updated: Home, SEO, Images, Updating Content, and a new Change Log page.

### Known open items
- No one-day picnic FAQ yet. Add one when package details and prices are final.
- The Dasturi Naka FAQ answer gives no distance; add the exact figure from the resort if wanted.
- `D46.jpg` and `D48.jpg` are over the 250 KB image guideline; compress them.
- `images/a` (a 2-byte stray file) and `images/logo s.webp` (a space in the file name) should be cleaned up.
- Biggest remaining ranking levers are off the site: Google Business Profile, Google reviews, listings, and separate pages for rooms, dining, events and corporate outings.
