# Hôtel Soltane — GitHub Pages Production Audit

**Audited host:** [https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/](https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/)

This report records the live audit after deployment commit `807e5ad` and workflow run `32289044120`. The custom `hotel-soltane.dz` domain remains intentionally pending official confirmation; all current preview canonical, Open Graph, robots, and sitemap values use the GitHub Pages project URL.

## Required live files

| File | HTTP status | Content type | Bytes | Local source |
| --- | ---: | --- | ---: | --- |
| `index.html` | 200 | `text/html; charset=utf-8` | 40707 | Present |
| `chambres.html` | 200 | `text/html; charset=utf-8` | 32661 | Present |
| `experiences.html` | 200 | `text/html; charset=utf-8` | 29070 | Present |
| `galerie.html` | 200 | `text/html; charset=utf-8` | 31133 | Present |
| `contact.html` | 200 | `text/html; charset=utf-8` | 25930 | Present |
| `404.html` | 200 | `text/html; charset=utf-8` | 3083 | Present |
| `robots.txt` | 200 | `text/plain; charset=utf-8` | 206 | Present |
| `sitemap.xml` | 200 | `application/xml` | 3131 | Present |

**Result:** all eight required deployed files returned HTTP 200 and all eight local source files are present.

## Image request audit

| Referenced path | Local file | Dimensions | Format | File size | Live status | Live content type |
| --- | --- | ---: | --- | ---: | ---: | --- |
| `assets/hero-1440.webp` | Present | 1440×810 | WEBP | 82318 B | 200 | `image/webp` |
| `assets/story-1080.webp` | Present | 1080×1350 | WEBP | 64026 B | 200 | `image/webp` |
| `assets/gal-1-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/gal-2-1080.webp` | Present | 1080×1350 | WEBP | 64026 B | 200 | `image/webp` |
| `assets/gal-3-1080.webp` | Present | 1080×1350 | WEBP | 64026 B | 200 | `image/webp` |
| `assets/gal-4-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/rooms-hero-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/room-twin-1080.webp` | Present | 1080×810 | WEBP | 64962 B | 200 | `image/webp` |
| `assets/room-king-1080.webp` | Present | 1080×810 | WEBP | 64962 B | 200 | `image/webp` |
| `assets/suite-junior-1080.webp` | Present | 1080×810 | WEBP | 64962 B | 200 | `image/webp` |
| `assets/suite-senior-1080.webp` | Present | 1080×810 | WEBP | 64962 B | 200 | `image/webp` |
| `assets/exp-hero-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/kortoba-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/sidi-1080.webp` | Present | 1080×1350 | WEBP | 64026 B | 200 | `image/webp` |
| `assets/lala-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/events-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/gallery-hero-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/gal-5-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/gal-6-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/gal-7-1080.webp` | Present | 1080×1350 | WEBP | 64026 B | 200 | `image/webp` |
| `assets/gal-8-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |
| `assets/contact-hero-1440.webp` | Present | 1440×900 | WEBP | 77210 B | 200 | `image/webp` |

**Result:** 22 referenced image paths audited; 22 returned HTTP 200 and have local files; failures: 0.

## Placeholder scan

| Category | Result |
| --- | --- |
| `%VITE_` | No hits |
| `EXEMPLE` | No hits |
| `localhost` | No hits |
| `hotel-soltane.dz` | 11 intentional documentation/comment hits; preserved only as the pending custom-domain note |
| `[À CONFIRMER]` | No hits |
| `/manus-storage/` | No hits |
| `absolute /assets/` | No hits |

**Production HTML result:** no root-absolute `/assets/`, `/manus-storage/`, localhost, Vite, example, or stale confirmed-domain references remain. The only remaining `hotel-soltane.dz` occurrences are intentional pending-domain documentation/comments.

## Metadata and phone direction

| Page | HTML lang | dir | Canonical | Open Graph URL |
| --- | --- | --- | --- | --- |
| `index.html` | `fr` | `ltr` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/` |
| `chambres.html` | `fr` | `ltr` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/chambres.html` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/chambres.html` |
| `experiences.html` | `fr` | `ltr` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/experiences.html` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/experiences.html` |
| `galerie.html` | `fr` | `ltr` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/galerie.html` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/galerie.html` |
| `contact.html` | `fr` | `ltr` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/contact.html` | `https://abdou1lalmi.github.io/hotel-soltane-les-heures-d-ambre/contact.html` |
| `404.html` | `fr` | `ltr` | `None` | `None` |

All audited telephone anchors use `<bdi>`: 15/15.

## Navigation and source validation

Internal HTML navigation checks: 78/78 local targets resolved.

The local production validator passed required files, image existence/dimensions, visible form labels, `<bdi>` phone wrappers, external-link security attributes, JSON-LD parsing, sitemap XML parsing, and native dialog hooks. The GitHub Actions Pages deployment completed successfully.

## Live Lighthouse scores

Lighthouse 12.8.2 was run against the deployed GitHub Pages routes. The homepage score below reflects the post-deployment hero preload fix in commit `807e5ad`; the other pages were unchanged by that targeted fix.

| Page | Performance | Accessibility | Best Practices | SEO | All categories >90 |
| --- | ---: | ---: | ---: | ---: | --- |
| `index.html` | 96 | 95 | 96 | 100 | PASS |
| `chambres.html` | 98 | 96 | 96 | 100 | PASS |
| `experiences.html` | 96 | 96 | 96 | 100 | PASS |
| `galerie.html` | 97 | 95 | 96 | 100 | PASS |
| `contact.html` | 97 | 96 | 96 | 100 | PASS |

The corrected homepage run measured FCP 1.1 s, LCP 2.2 s, Speed Index 1.2 s, Total Blocking Time 120 ms, and CLS 0.092.

## Browser smoke tests

The production browser smoke test loaded the homepage, rooms, experiences, gallery, contact, and 404 pages directly. French and Arabic states were verified on the homepage and content pages; Arabic switched the document to RTL and translated the visible strings. The live booking dialog opened with Arabic content and closed with Escape. The live gallery lightbox opened with a localized caption, moved focus to its close control, and closed with Escape. The live burger contract toggled `aria-expanded` and menu visibility correctly. Contact testing confirmed phone, mailto, Instagram, Google Maps, and disabled WhatsApp behavior.

## Remaining external checks

Google Search Console sitemap submission and Google Rich Results Test require an authenticated Google account and were not executable from the sandbox. They remain client-side submission/validation steps, not deployment failures.

## Final status

The GitHub Pages deployment is technically ready for preview: all required files and referenced image requests return HTTP 200, project-relative paths resolve under the repository path, production HTML has no forbidden unresolved placeholders, all five pages exceed 90 in each Lighthouse category, and browser smoke tests pass. The custom domain and final art-directed hotel photography remain explicitly pending client confirmation.
