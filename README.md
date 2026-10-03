# Seema Resort Website

A modern, responsive, single-page static website for Seema's Resort, located on the Neral-Karjat Highway near Matheran, Maharashtra[cite: 1]. The site is designed for high performance, ease of use, and direct booking conversions via WhatsApp and Email[cite: 1].

## Project Overview

This project consists of a frontend web interface built natively with HTML, CSS, and vanilla JavaScript[cite: 1]. It serves as the digital storefront for the resort, showcasing room categories, property amenities, booking rules, location details, and guest reviews[cite: 1]. 

## Features

*   **Responsive Design:** Fully mobile-optimized layout with a sticky navigation bar, a bottom mobile action bar, and adaptive CSS Grid and Flexbox layouts[cite: 1].
*   **SEO & Discoverability:** Includes standard meta tags, Open Graph tags (for Facebook/WhatsApp previews), Twitter Cards, and comprehensive Schema.org JSON-LD structured data for both `LodgingBusiness` and `FAQPage`[cite: 1].
*   **Analytics Tracking:** Pre-configured with a Google Tag Manager (gtag.js) script for traffic monitoring[cite: 1].
*   **Interactive UI Components:** Features a custom vanilla JavaScript image carousel for room galleries, scroll-reveal animations using `IntersectionObserver`, native HTML `<details>` and `<summary>` tags for FAQs, and a native `<dialog>` modal for expanding long guest reviews[cite: 1].
*   **Direct Booking Integration:** A built-in HTML form that captures user dates, guest counts, and room preferences, then dynamically generates a pre-filled WhatsApp message or Email request without requiring a backend database[cite: 1].
*   **Performance & Accessibility:** Implements `prefers-reduced-motion` media queries for accessibility, and utilizes native lazy loading (`loading="lazy"`) and asynchronous decoding (`decoding="async"`) for optimized image delivery[cite: 1].

## File Structure

| File | Description |
| :--- | :--- |
| `index.html` | The main, single-page HTML document containing all text content, inline CSS (`<style>`), and frontend JS logic (`<script>`)[cite: 1]. |
| `robots.txt` | Standard search engine directive file explicitly allowing all user-agents to crawl the site and linking to the sitemap[cite: 2]. |
| `sitemap.xml` | An XML sitemap indicating the main URL and its change frequency to assist search engine indexing[cite: 3]. |

## Setup & Deployment

Because this is a completely static website with no backend dependencies, deployment is straightforward:

1.  **Asset Management:** Ensure all image assets referenced in the `index.html` markup (e.g., `images/pool.jpeg`, `images/LogoMainNoBG.png`, `images/hall.jpeg`) are placed in an `images/` directory at the root level alongside the HTML file[cite: 1].
2.  **Hosting:** Upload the root directory containing `index.html`, `robots.txt`, and `sitemap.xml` to any static web hosting service (such as GitHub Pages, Netlify, Vercel, or an Apache/Nginx server).
3.  **Local Testing:** Simply open the `index.html` file in any modern web browser to view and test the site locally.
