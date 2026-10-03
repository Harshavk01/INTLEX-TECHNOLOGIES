# Intlex Technologies — Corporate Website

Static website for Intlex Technologies, Inc. (intlextech.com). Pure HTML5, CSS3 and vanilla JavaScript — no frameworks, no build step.

## Structure

```
index.html          Home
about.html          About (overview, vision, mission, philosophy, global perspective)
services.html       Service portfolio, industries, engagement models
ai.html             AI & Enterprise AI (incl. AI beyond SAP use cases)
sap-ai.html         SAP AI
strategy.html       AI Strategy, Governance & Frameworks
analytics.html      Analytics, SAP-to-Non-SAP Analytics, Digital Transformation
insights.html       Insights index + full perspective articles
contact.html        Enquiry form, contact details, FAQ
privacy.html        Privacy & cookie policy
terms.html          Terms of use
404.html            Not-found page
css/style.css       Design tokens, components
css/responsive.css  Breakpoints (1280 / 1080 / 860 / 600)
js/navigation.js    Mobile menu, services dropdown, active states, sticky header
js/main.js          Reveals, scroll-to-top, FAQ, insights filter, form validation
assets/logos/       Logo icon (light/dark) and full logo
assets/icons/       Favicons, touch icon
assets/images/      Open Graph image
sitemap.xml, robots.txt, site.webmanifest
```

## Deploy

Upload the whole folder to any static host (Netlify, Vercel, Azure Static Web Apps, AWS S3 + CloudFront, GitHub Pages, cPanel). Point intlextech.com at it and enable HTTPS. Configure the host to serve `404.html` for missing pages.

## Before go-live — confirm these

1. **Email address** — `info@intlextech.com` is a placeholder. Change `EMAIL` throughout (search the HTML for `info@intlextech.com`).
2. **Contact form backend** — the form validates in the browser and shows a confirmation, but does not send anywhere yet. Set the endpoint on the form in `contact.html`:
   `<form class="form" data-contact-form data-endpoint="https://formspree.io/f/XXXX" novalidate>`
   Any service that accepts a multipart POST works (Formspree, Getform, Power Automate HTTP trigger, an Azure Function). The hidden `company_website` field is a spam honeypot.
3. **Office address / phone / LinkedIn** — add to `contact.html` and the footer when available.
4. **Logo source** — the logo files were cropped from the supplied PNG. Replace with SVG exports from the original artwork when available for the sharpest result.
5. **Legal pages** — `privacy.html` and `terms.html` are reasonable starting text, not legal advice; have them reviewed.
6. **Analytics** — if GA4 or similar is added, add a cookie consent banner and update the cookie section of the privacy policy.

## Notes

- Font: Inter (Google Fonts) with system-font fallback.
- All animation respects `prefers-reduced-motion`; content remains fully readable with animations disabled, and FAQ answers stay visible if JavaScript fails to load.
- Colours: primary `#1D3770`, supporting `#24478F`, `#315AA0`, `#4A6FAF`, `#EAF0F8`, `#F5F7FA`, `#111827`; footer uses logo navy `#0B2F55`.
