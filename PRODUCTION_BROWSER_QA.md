# Production browser QA notes

## Local project preview

The local static preview at `http://127.0.0.1:4178/` loaded the homepage successfully with the optimized hero asset and project-relative image URLs. The French page rendered the five primary navigation labels, booking CTA, four verified phone links, visible newsletter label, and all homepage sections.

The Arabic control switched the same page to Arabic successfully. The document title became `فندق سلطان | الجزائر العاصمة — ساعات العنبر`, the page content translated, and the layout mirrored to RTL. The phone numbers remained visible in numeric order within their links, and the newsletter label and placeholder translated.

## Rooms page

Direct navigation to `chambres.html` loaded successfully from the local preview and preserved the stored Arabic state. The page displayed all four translated room categories, all verified attributes, project-relative asset URLs, and visible booking CTAs. The first viewport-based click attempt on a room CTA did not visibly open the dialog, so the handler was checked separately with a programmatic activation in the next step.

The first room booking CTA was then activated programmatically in the Arabic page. The native booking dialog opened, its close control received focus, all four verified phone numbers were present, the Arabic email action was localized, and WhatsApp remained disabled with its pending label. Pressing Escape closed the dialog and returned focus to the triggering CTA.

## Gallery page

Direct navigation to `galerie.html` loaded successfully in Arabic with all eight gallery figures and project-relative `assets/...` image URLs. The page remained mirrored RTL while the masonry grid rendered in the local preview. The next check activates a figure from the scrolled grid to verify the native lightbox and Escape close.

The first Arabic gallery figure opened the native lightbox programmatically with the localized caption `ضوءُ السابعةَ عشرة` and focus on the close control. Escape closed the lightbox successfully and returned to the gallery figure grid.

## Contact page

Direct navigation to `contact.html` loaded in Arabic with the translated address, four distances, Google Maps external link, telephone CTA, mailto CTA, Instagram CTA, disabled WhatsApp button, and hours. Switching back to French restored LTR, French labels, and the pending WhatsApp state. The phone CTA remained wrapped with the verified number and the map link exposed the localized new-tab aria label.

## Experiences and 404 pages

Direct navigation to `experiences.html` loaded the French venue and event content with all four project-relative image slots. Direct navigation to `404.html` loaded the localized not-found page with working home/contact links and FR/AR controls.

## Live GitHub Pages homepage

The deployed `index.html` returned successfully with HTTP 200 through the browser. The live page rendered French navigation, project-relative `assets/hero-1440.webp`, visible booking and phone links, and the newsletter label. Switching the live page to Arabic changed the title to `فندق سلطان | الجزائر العاصمة — ساعات العنبر`, translated the page content, and mirrored the layout to RTL while retaining the phone numbers and translated newsletter controls.

## Live rooms page

The deployed `chambres.html` loaded directly and again after a fresh navigation, both with HTTP 200 and the persisted Arabic state. The live page exposed all four translated room cards, verified attributes, project-relative room assets, telephone/mail CTAs, and the visible newsletter label.

## Live experiences and gallery pages

The deployed `experiences.html` loaded directly in Arabic with all three verified venues, the event section, and project-relative hero/venue assets. The deployed `galerie.html` loaded directly in Arabic with all eight gallery figures, localized captions, and project-relative gallery assets.

## Live contact and 404 pages

The deployed `contact.html` loaded directly in Arabic with the verified address, four distances, Google Maps link, telephone and mailto booking CTAs, Instagram link, disabled WhatsApp state, and hours. The deployed `404.html` loaded directly in Arabic with the localized error title and working home/contact links.

## Live gallery lightbox

On the deployed gallery page, the first figure opened the native lightbox with the localized Arabic caption `ضوءُ السابعةَ عشرة`; the dialog was open and focus moved to `lb-close`.

Escape closed the live gallery lightbox successfully. The deployed mobile-navigation contract was then exercised programmatically: the burger changed `aria-expanded` from `false` to `true`, revealed the menu, and restored `false` with the menu hidden when closed.
