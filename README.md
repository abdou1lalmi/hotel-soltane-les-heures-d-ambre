# Hôtel Soltane — Les heures d’ambre

This package contains the static Hôtel Soltane website foundation and five page files: `index.html`, `chambres.html`, `experiences.html`, `galerie.html`, and `contact.html`. The pages share `tokens.css`, `base.css`, `typography.css`, and `utils/i18n.js`. The implementation is dependency-light and can be served from any static host.

> **Production note:** The canonical domain `hotel-soltane.dz` remains the pending custom production domain; GitHub Pages is the current preview host. Replace it before launch if the final domain differs.

## Run locally

From the project root, start any static server. For example:

```bash
python3 -m http.server 4173
```

Then open `http://127.0.0.1:4173/index.html`. The pages rely on ES modules, so do not open them directly from `file://` in a browser.

## Pages and shared files

| File | Purpose |
| --- | --- |
| `index.html` | Homepage with hero, story, hotel facts, gallery preview, contact CTA, and phone numbers. |
| `chambres.html` | Four room cards: Twin, grand lit, suite junior, and suite sénior. |
| `experiences.html` | Restaurant Kortoba, Cafétéria Sidi Abderrahmane, Hammam Lala Amira, and événementiel. |
| `galerie.html` | Eight-image asymmetric gallery with native dialog lightbox. |
| `contact.html` | Verified address, distances, booking channels, Google Maps, and hours. |
| `utils/i18n.js` | Shared French/Arabic dictionary, persisted language, document direction, and localized accessibility labels. |
| `tokens.css`, `base.css`, `typography.css` | Phase A design tokens, global accessibility/reset rules, and fluid typography. |
| `sitemap.xml`, `robots.txt` | Search-engine discovery files using the current GitHub Pages preview URL. |
| `404.html` | Localized GitHub Pages not-found document with FR/AR toggle. |
| `QA_REPORT.md` | Final structural, accessibility, interaction, and Lighthouse results. |

## How to replace images

Place optimized assets in `assets/` and keep the filenames referenced by the page markup. Each image slot includes intrinsic width/height attributes, lazy loading where appropriate, and a gradient fallback only for an unexpected load failure. Every currently referenced slot is included as a project-local WebP derivative so its production request returns HTTP 200; replace those derivatives with final hotel photography when supplied.

Do not overwrite a photo with an unlicensed image. Keep the same subject and approximate aspect ratio for each slot so the editorial layout remains stable. After replacing files, verify the five pages at desktop, tablet, and mobile widths and confirm that every image has either a descriptive `alt` value or `alt=""` when it is purely decorative and already explained by adjacent text/captions.

## How to update the domain

Search the project for the GitHub Pages preview host and replace it with the confirmed `hotel-soltane.dz` domain only after official approval. Update all of the following together:

1. The canonical URL in each HTML head.
2. The `hreflang` alternate URLs.
3. `og:url` and social image URLs.
4. Hotel JSON-LD URLs if a URL field is added later.
5. `sitemap.xml` `<loc>` values and alternate links.
6. `robots.txt` sitemap URL.

After the replacement, validate the XML sitemap and submit its final URL in Google Search Console. Validate the JSON-LD in Google Rich Results Test after the production URL is live.

## How to enable WhatsApp

The WhatsApp CTA is intentionally disabled because the official WhatsApp number is not verified. Once the hotel supplies written confirmation, update the disabled button in `contact.html`, `chambres.html`, and any other page that uses the shared booking CTA:

```html
<a
  class="btn btn-ghost"
  href="https://wa.me/213XXXXXXXXX"
  target="_blank"
  rel="noopener noreferrer"
  data-i18n="bookWhatsapp"
>WhatsApp</a>
```

Replace `213XXXXXXXXX` with the confirmed international number without spaces or punctuation. Update the French and Arabic `bookWhatsapp` strings in `utils/i18n.js`, remove the `[À CONFIRMER — WHATSAPP]` comments only after written confirmation, and test the link on mobile and desktop.

## How to add analytics

Use a privacy-reviewed analytics provider and obtain client approval before adding tracking. Place the provider’s script in the `<head>` of all five pages, or add it through the static host’s approved injection mechanism. Do not add a tracking identifier until the hotel provides it. If consent is required, load analytics only after the visitor’s consent and document the retention policy. Keep outbound booking clicks measurable without capturing message contents or personal form data.

A minimal implementation should record page views, language changes, telephone CTA clicks, mailto CTA clicks, Instagram clicks, Google Maps clicks, and lightbox opens. Do not submit the newsletter form to a backend unless a verified provider and privacy notice are supplied; the current form is intentionally non-destructive.

## Asset request list

The following approved hotel photography is requested. All files should be delivered as WebP where possible, with no embedded text, logos, watermarks, or unlicensed third-party material.

| Asset | Recommended dimensions | Use |
| --- | ---: | --- |
| `hero-1440.webp` | 1440 × 900 px, landscape | Homepage hero. Keep the main focal subject away from the text-safe area. |
| `story-1080.webp` | 1080 × 1350 px, portrait | Homepage section 01 image. |
| `room-twin-1080.webp` | 1080 × 810 px, landscape | Twin room card. |
| `room-king-1080.webp` | 1080 × 810 px, landscape | Grand-lit room card. |
| `suite-junior-1080.webp` | 1080 × 810 px, landscape | Junior suite card. |
| `suite-senior-1080.webp` | 1080 × 810 px, landscape | Senior suite card. |
| `rooms-hero-1440.webp` | 1440 × 900 px, landscape | Rooms page hero. |
| `kortoba-1440.webp` | 1440 × 960 px, landscape | Restaurant Kortoba venue block. |
| `sidi-1080.webp` | 1080 × 1350 px, portrait | Cafétéria Sidi Abderrahmane venue block. |
| `lala-1440.webp` | 1440 × 960 px, landscape | Hammam Lala Amira venue block. |
| `events-1440.webp` | 1440 × 960 px, landscape | Événementiel section. |
| `exp-hero-1440.webp` | 1440 × 900 px, landscape | Experiences page hero. |
| `gal-1-1440.webp` to `gal-8-1440.webp` | 1440 × 900 px, landscape | Gallery images 01–08, subject to the masonry crop. |
| `gal-2-1080.webp`, `gal-3-1080.webp`, `gal-7-1080.webp` | 1080 × 1350 px, portrait | Optional portrait exports for the existing gallery strata. |
| `gallery-hero-1440.webp` | 1440 × 900 px, landscape | Gallery page hero. |
| `contact-hero-1440.webp` | 1440 × 900 px, landscape | Contact page hero. |

For the homepage hero, keep the final optimized file at or below **300 KB** if visual quality permits. Otherwise provide an appropriately compressed WebP and a fallback strategy approved by the client.

## Photo authorization template

Use `PHOTO_AUTHORIZATION_TEMPLATE.md` as a starting point for written authorization. The signed document should identify the photographer or rights holder, the hotel, the exact assets, permitted channels, territory, duration, edits/crops, credit requirements, and whether model/property releases are included.

## QA checklist

The final audit should be repeated after final approved photography and the custom production domain are in place; the current GitHub Pages preview audit is recorded in `QA_REPORT.md`.

| Check | Status in this package |
| --- | --- |
| Five HTML pages present | Passed. |
| Shared FR/AR language and RTL direction | Passed structurally and in browser smoke tests. |
| Phone numbers use `<bdi>` where displayed | Passed in homepage and contact CTA; verify any future phone copy added to other pages. |
| Image alt values are present or intentionally empty | Passed structurally; replace placeholder alt text only when approved photos require descriptive text. |
| Newsletter forms have visible labels | Passed after final QA adjustment. |
| Native lightbox closes with Escape | Passed on gallery. |
| External links use `target="_blank" rel="noopener noreferrer"` | Passed for Google Maps and Instagram anchors. |
| Sitemap XML parses | Run `python3 -c "import xml.etree.ElementTree as ET; ET.parse('sitemap.xml')"`. |
| JSON-LD validation | Run Google Rich Results Test after the production URL is live. |
| Lighthouse | Passed on the final local preview: homepage 90/95/96/100, rooms 97/96/96/100, experiences 95/96/96/100, gallery 91/95/96/100, contact 97/96/96/100 for Performance/Accessibility/Best Practices/SEO. Rerun against the final deployed URL in both language states. |

## Deployment note

The source is deployed on GitHub Pages from the public `main` branch. The project-relative paths, sitemap, robots.txt, and preview metadata use the GitHub Pages project URL. The custom `hotel-soltane.dz` domain remains pending official confirmation and should replace the preview URL only after approval.
