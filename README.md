# Seema's Resort Website

Official website for **Seema's Resort & Restaurant**, on the Neral-Karjat Highway near Matheran, Maharashtra.

**Live site:** https://www.seemaresort.in

A fast, mobile-first, single-page static site built to turn visitors into direct enquiries through WhatsApp, phone and email.

---

## Features

- **Mobile-first layout** with a sticky header and a bottom action bar (Call / WhatsApp) on phones
- **Room cards with image carousels**, each with a "Book on WhatsApp" button pre-filled for that room
- **Booking form with no backend**: collects dates, guests and room preference, then opens a pre-filled WhatsApp message or email
- **Guest reviews** with a pop-up to read long reviews, linked to the resort's Google reviews
- **FAQ section** using native `<details>` elements
- **Embedded Google Map** and links to Instagram, Facebook and Google
- **SEO ready**: meta tags, Open Graph and Twitter cards, canonical URL, `LodgingBusiness` and `FAQPage` structured data, `sitemap.xml` and `robots.txt`
- **Google Analytics** for traffic tracking
- **Performance and accessibility**: lazy-loaded images, scroll-reveal animations that respect `prefers-reduced-motion`

## Tech Stack

HTML, CSS and vanilla JavaScript in a single file. No framework, no build step, no database.

## Repository Structure

```
seemaresort/
├── index.html      # The whole site: content, inline CSS and JS
├── images/         # Photos and logo used by the site
├── CNAME           # Custom domain for GitHub Pages
├── sitemap.xml     # Sitemap for search engines
├── robots.txt      # Crawler rules, points to the sitemap
├── SECURITY.md     # How to report a security issue
└── README.md       # This file
```

## Editing the Site

1. Open `index.html` in GitHub and click the pencil icon, or edit it locally.
2. Make the change (rooms, rates, FAQs, text, links).
3. Commit to `main`. GitHub Pages republishes within a couple of minutes.
4. After major changes, update the `lastmod` date in `sitemap.xml`.

**Contact details** are set in more than one place. If the phone number or email changes, update all of these in `index.html`:

- `WHATSAPP_NUMBER` and `RESORT_EMAIL` at the top of the script
- every `tel:` and `wa.me` link
- the structured data block in the `<head>`
- the contact section and footer

**FAQs:** if you change an FAQ, update the matching `FAQPage` structured data in the `<head>`.

## Images

- Keep all images in `images/`.
- Compress photos before uploading, ideally **under 250 KB each**, so the site loads fast on mobile.
- Avoid spaces in file names.
- Use descriptive alt text, for example: `Family Executive Room at Seema Resort Neral - bedroom view`.
- The link preview image (WhatsApp, Facebook) is `images/pool.jpeg`.

## Deployment

The site is hosted on **GitHub Pages** from the `main` branch.

- Custom domain: `www.seemaresort.in` (set in the `CNAME` file)
- Domain and email are managed at Hostinger. DNS records point to GitHub Pages, so do not change them unless hosting moves.
- Check publishing status under **Settings → Pages**.

To run locally, open `index.html` in any browser.

## Documentation

More guides (updating content, images, booking and contact, hosting, SEO) are in the repository **Wiki**.

## Contact

- **Phone:** +91 75594 11323, +91 77458 52323 (8 AM to 10 PM, every day)
- **WhatsApp:** +91 75594 11323
- **Email:** contact@seemaresort.in
- **Address:** Seema's Resort & Restaurant, Near Panchwati, Neral-Karjat Highway, Neral - 410101

## Security

To report a security issue, see [SECURITY.md](SECURITY.md). Please do not open a public issue.

## License

All rights reserved. The text, images and branding belong to Seema's Resort. Do not reuse without permission.
