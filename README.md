# Brace & Mare — demo website

Unsolicited concept website for **Ristorante Brace & Mare**, Francavilla al Mare (CH), designed and developed by **Punto Due Studio**.

> This is a non-commissioned demo. It is not the restaurant's official website and does not imply a commercial relationship with the business.

## Goal

Create a polished, mobile-first sales demo using only public, verifiable business information. The visual direction is intentionally different from the other Punto Due Studio demos: **fire and Adriatic sea are treated as two visual systems that collide and merge**.

The site is static, framework-free and ready to deploy on Netlify.

## Verified public information used

### Business
- Name: **Ristorante Brace & Mare**
- Category: restaurant
- Address: **Viale Alcione 73A, 66023 Francavilla al Mare (CH)**
- Primary phone used in the demo: **+39 085 422 5743**
- Instagram: **@braceemare**
- Facebook: `https://www.facebook.com/profile.php?id=61583529892938`
- TheFork: `https://www.thefork.it/ristorante/ristorante-brace-mare-r857267`

### Cuisine / concept
Public sources support a menu built around both **Abruzzese grill / arrosticini** and **seafood**. TheFork lists the cuisine as Abruzzese and groups the menu under arrosticini and fish. LocaliPescara also describes the restaurant around the pairing of grill and Adriatic seafood.

### Chef
TheFork lists **Luciana Di Stefano** as chef (menu last updated 17 February 2026).

### Menu items used in the demo
From the public TheFork menu, last update shown as 17 February 2026:
- Antipasti della casa — €9
- Tagliere del territorio — €9
- Arrosticini — €1.20
- Arrosto misto — €18
- Spaghetti alle vongole — €12
- Spaghettone cozze e pecorino — €12
- Mezze maniche agli scampi — €12
- Frittura scampi e calamari — €14

The site explicitly tells visitors that availability and prices can change and links to the live menu.

### Ratings / public reputation
At research time (14 September 2026):
- TheFork displayed **8.9/10** with **79 reviews**.
- Restaurant Guru, updated August 2026, reported **Google 4.7/5 from 52 ratings**.

Review counts are time-sensitive and are therefore presented only as contextual proof, not as permanent claims.

### Opening hours used
Restaurant Guru was the freshest detailed source found (updated 16 August 2026):
- Monday: closed
- Tuesday: 11:30–15:00
- Wednesday–Saturday: 11:30–15:00 / 19:00–00:00
- Sunday: 11:30–15:00 / 19:00–23:30

The demo labels these as public hours and tells users to verify before visiting.

## Conflicting public data found

Public directories are not fully aligned. Instead of silently inventing a definitive answer, the demo follows the freshest sources and records the conflict here.

### Phone
- Restaurant Guru (updated Aug 2026) and the current structured business listing returned **085 422 5743**.
- LocaliPescara (Mar 2026) lists **085 810488** and **347 106 3125**.

The demo uses **085 422 5743** because it is supported by the most recent sources. The older numbers were intentionally not mixed into the public-facing site.

### Hours
- Restaurant Guru provides the detailed schedule used in the demo.
- Another July 2026 directory lists Tue–Sat 12:30–15:00 / 20:00–24:00 and Sunday lunch only.
- The structured business result returned lunch hours only, which appears incomplete compared with the restaurant/review platforms.

Because the sources disagree, the site does not present the schedule as guaranteed and includes a verification note.

### Address formatting
TheFork displays `Viale Alcione, 73`; Restaurant Guru, LocaliPescara and the business listing use **73A**. The demo uses **73A** because it is the more specific and repeatedly corroborated format.

## Research sources

- TheFork — restaurant/menu: https://www.thefork.it/ristorante/ristorante-brace-mare-r857267/menu
- Restaurant Guru — current listing/reviews/hours: https://restaurantguru.it/Ristorante-Brace-and-Mare-Francavilla-al-Mare
- LocaliPescara — profile/social/contact context: https://www.localipescara.it/francavilla-al-mare/ristorante-brace-mare-ristorante-francavilla-al-mare/
- OrariDiApertura24 — secondary hours/email cross-check: https://www.oraridiapertura24.it/filiale/Francavilla%2520al%2520Mare-Brace%2520%2526%2520Mare-5285902M.html

Research date: **14 September 2026**.

## Visual direction

The page is designed around the literal tension in the brand name:

- **Brace:** coal, ember red, terracotta, black, sharp geometry.
- **Mare:** deep teal, oxidized blue, foam, sand, curved wave forms.
- The hero is split into two worlds with the headline at the collision point.
- The menu itself is split into a fire side and a sea side.
- The chef section visually merges horizon and coal.
- Original CSS artwork is used instead of re-hosting third-party restaurant photography without permission.

This avoids a generic restaurant template and gives the demo a recognizable identity even without licensed venue photography.

## Functional scope

- Responsive one-page website
- Sticky header
- Mobile navigation with Escape support
- Mobile action dock
- Telephone CTA
- TheFork booking CTA
- Instagram / Facebook links
- Google Maps directions
- Selected verified menu + prices
- Current public hours with caveat
- JSON-LD `Restaurant` structured data
- Meta description + Open Graph basics
- SVG favicon
- Custom 404 page
- Reduced-motion support
- Progressive-enhancement reveal animations: content remains visible if JS is unavailable
- Netlify security headers

## Intentionally omitted

The demo does **not** invent or imply:
- WhatsApp availability
- ownership/founding history
- exact capacity
- private-event packages
- awards not verified by a primary/current source
- ingredients not supported by the published menu
- fixed availability of fresh catch
- a proprietary booking system
- payment/POS integrations
- loyalty/CRM systems
- user accounts
- legal business details not publicly verified

No fake contact form or fake reservation backend is included. Reservations go to the real public TheFork listing; phone links call the current public number used by the freshest sources.

## Privacy / cookies

The demo does not install analytics, advertising pixels or non-essential cookies, so no fake cookie banner was added. If tracking or embeds are introduced for production, the legal/privacy implementation must be reviewed with the business before launch.

## Files

```text
.
├── index.html
├── styles.css
├── script.js
├── 404.html
├── _headers
├── netlify.toml
├── robots.txt
└── assets/
    └── favicon.svg
```

## Netlify deployment

Import this repository into Netlify with:

- Base directory: empty
- Build command: empty
- Publish directory: `.`
- Functions directory: empty

`netlify.toml` already sets the publish directory to the repository root.

## Production checklist after a live URL exists

Before treating the project as an official production website:
1. Confirm current phone, opening hours, address and social links directly with Brace & Mare.
2. Confirm whether the older phone numbers are still active.
3. Replace or expand visual assets only with restaurant-owned / licensed photography.
4. Add canonical URL and `og:url` using the final production domain.
5. Add a suitable licensed `og:image`.
6. Add `sitemap.xml` and its final absolute URL to `robots.txt`.
7. Re-check live menu prices and remove stale prices if the restaurant does not want them maintained.
8. Review privacy/cookie/legal requirements if analytics, forms or third-party embeds are added.
9. Run a final live-browser QA pass after Netlify deployment.

## Punto Due Studio

Demo concept by **Punto Due Studio** — https://puntoduestudio.it/
