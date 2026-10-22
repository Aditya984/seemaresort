# Seema's Resort Website

Official website for **Seema's Resort & Restaurant**, on the Neral-Karjat Highway near Panchwati, at the foot of Matheran, Maharashtra.

**Live site:** https://www.seemaresort.in

A fast, mobile-first, single-page static site built to turn visitors into direct enquiries through WhatsApp, phone and email.

---

## Features

- **Mobile-first layout** with a sticky header and a bottom action bar (Call / WhatsApp) on phones
- **Room cards with image carousels**, each with a "Book on WhatsApp" button pre-filled for that room
- **Booking form with no backend**: collects dates, guests and room preference, then opens a pre-filled WhatsApp message or sends the enquiry by email (via Web3Forms)
- **Guest reviews** with a pop-up to read long reviews, linked to the resort's Google reviews
- **FAQ section** (11 questions) using native `<details>` elements, mirrored in `FAQPage` structured data
- **Embedded Google Map** and links to Instagram, Facebook and Google
- **Technical SEO**
  - keyword-targeted `<title>`, meta description, `<h1>` and `<h2>` headings
  - Open Graph and Twitter cards, canonical URL
  - JSON-LD for `Resort` / `LodgingBusiness` / `Restaurant` (rooms, offers with INR prices, amenities, Google reviews) and `FAQPage`
  - descriptive `alt` text on every image
  - `sitemap.xml` with image entries, and `robots.txt`
- **Crawler-safe animations**: content is never hidden in the HTML/CSS. Scroll-reveal runs only in real browsers (see "Animations and SEO" below)
- **Google Analytics** for traffic tracking
- **Performance and accessibility**: lazy-loaded images, animations that respect `prefers-reduced-motion`

## Tech Stack

HTML, CSS and vanilla JavaScript in a single file. No framework, no build step, no database. The booking form's email button uses [Web3Forms](https://web3forms.com).

## Repository Structure

```
seemaresort/
├── index.html      # The whole site: content, inline CSS and JS
├── 404.html        # Friendly "page not found" page (noindex)
├── images/         # Photos, logo, favicons and the link-preview image
├── CNAME           # Custom domain for GitHub Pages
├── sitemap.xml     # Sitemap for search engines (includes image entries)
├── robots.txt      # Crawler rules, points to the sitemap
├── SECURITY.md     # How to report a security issue
├── CHANGELOG.md    # What changed and when
└── README.md       # This file
```

## Editing the Site

1. Open `index.html` in GitHub and click the pencil icon, or edit it locally.
2. Make the change (rooms, rates, FAQs, text, links).
3. Commit to `main`. GitHub Pages republishes within a couple of minutes.
4. After major changes, update the `lastmod` date in `sitemap.xml`.

### Things that live in more than one place

Keep these in sync every time you change them.

| If you change... | Also update... |
|---|---|
| **Phone number or email** | `WHATSAPP_NUMBER` and `RESORT_EMAIL` in the script, every `tel:` and `wa.me` link, the JSON-LD `telephone` / `email`, the contact section and footer |
| **Room rates** | the room card in `#rooms` **and** the matching `Offer` prices in the JSON-LD (`hasOfferCatalog` and `makesOffer`) and the `priceRange` |
| **A room name** | the room card, its WhatsApp link text, the booking-form dropdown, the JSON-LD room entries, and the image `alt` text |
| **An FAQ** | the visible `<details>` in `#faq` **and** the `FAQPage` JSON-LD (the text must match) |
| **Pool timings, check-in slots or rules** | the page text, the matching FAQ answers, and the JSON-LD `checkinTime` / `checkoutTime` |
| **Guest reviews** | the cards in `#reviews` **and** the `review` list in the JSON-LD |
| **Page title or description** | the `<title>`, `<meta name="description">`, `og:` and `twitter:` tags (the description appears three times) |
| **Address** | the contact section, map caption, JSON-LD `address` / `geo`, and your Google Business Profile |

### Headings

The `<h1>` and `<h2>` tags carry the main search keywords (resort in Neral, near Matheran and Karjat, swimming pool, cottages, couple suites, dormitories, group outings). Keep them descriptive. Do not change them back to short, vague slogans. There must be exactly one `<h1>`.

### Animations and SEO

Search engines must always see 100% of the text.

- The `<head>` script adds `html.motion` only for real browsers that allow motion. Crawlers, headless tools and `prefers-reduced-motion` users never get it.
- Only blocks below the first screen get the `.reveal-wait` fade-in, and everything is revealed after 5 seconds if nobody scrolls (`REVEAL_FAILSAFE_MS` in the script).
- **Never add `opacity:0`, `display:none` or `visibility:hidden` to page content in the static CSS.** If you add a new animated block, add its selector to the `revealTargets` list in the script instead.

## Images

- Keep all images in `images/`.
- Compress photos before uploading, ideally **under 250 KB each**, so the site loads fast on mobile. Currently over that: `D46.jpg`, `D48.jpg` (and `D42.jpg` is close).
- Avoid spaces in file names.
- Write descriptive alt text: the room or facility, what the photo shows, and the place. Pattern: `Family Executive Room bedroom at Seema's Resort Neral near Matheran & Karjat`.
- Every new photo on the page should also be added to `sitemap.xml` as an `<image:image>` entry with a descriptive `<image:title>`.
- The link preview image (WhatsApp, Facebook) is `images/og-image.jpg` (1200x630). Replace it with the same size if you change it.

## SEO Maintenance Checklist

Monthly:

1. In **Google Search Console**, check **Pages** (indexing), **Performance** (queries and clicks) and **Sitemaps** (`sitemap.xml` shows as "Success").
2. Reply to new Google reviews and add the best ones to `#reviews` and the JSON-LD.
3. Confirm rates, timings and phone numbers on the site match your Google Business Profile.
4. Test the page with Google's **Rich Results Test** and **PageSpeed Insights** after big edits.

After every change to `index.html`: update `lastmod` in `sitemap.xml`, then in Search Console use **URL Inspection → Request indexing** for `https://www.seemaresort.in/`.

## Deployment

The site is hosted on **GitHub Pages** from the `main` branch.

- Custom domain: `www.seemaresort.in` (set in the `CNAME` file)
- Domain and email are managed at Hostinger. DNS records point to GitHub Pages, so do not change them unless hosting moves.
- Check publishing status under **Settings → Pages**, and keep **Enforce HTTPS** turned on.

To run locally, open `index.html` in any browser.

## Documentation

More guides (updating content, images, booking and contact, hosting, SEO) are in the repository **Wiki**. A history of what changed and when is in [CHANGELOG.md](CHANGELOG.md).

## Contact

- **Phone:** +91 75594 11323, +91 77458 52323 (8 AM to 10 PM, every day)
- **WhatsApp:** +91 75594 11323
- **Email:** contact@seemaresort.in
- **Address:** Seema's Resort & Restaurant, Near Panchwati, Neral-Karjat Highway, Neral - 410101

## Security

To report a security issue, see [SECURITY.md](SECURITY.md). Please do not open a public issue.

## License

All rights reserved. The text, images and branding belong to Seema's Resort & Restaurant. Do not reuse without permission.
