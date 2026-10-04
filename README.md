# GA Compliance Pro

Marketing site for GA Compliance Pro, a done-for-you license compliance service for Georgia real estate brokerages. The site has one job: get visitors to book a 15-minute call.

Live at https://gacompliancepro.com (hosted on Vercel; the domain is registered at Squarespace).

## Structure

- `index.html` is the whole site: inline CSS and a few lines of vanilla JavaScript for the accordions. There's no build step and no dependencies other than Google Fonts.
- `assets/caitlyn-headshot.jpg` is the founder photo, resized from the 2.2 MB original to about 90 KB.

## Deploying

Vercel deploys automatically on every push to the connected branch.

## Design tokens

These are defined as CSS variables in `:root`.

| Token | Value |
| --- | --- |
| Navy | `#0F2540` |
| Gold | `#C9933A` |
| Gold light (hover, accents on navy) | `#DBA84E` |
| Gold dark (labels on light backgrounds) | `#8A6220` |
| Body text | `#17202E` |
| Secondary text | `#374151` |
| Light background | `#F5F6F8` |
| Headings, numbers, prices | Source Serif 4 |
| Body text, UI | Public Sans |

Gold buttons always use navy text.

Breakpoints are at `max-width: 979px` (tablet) and `max-width: 639px` (phone).

## Analytics

A PostHog snippet in `<head>` loads only once `window.POSTHOG_KEY` is set to a real key (one that starts with `phc_`). Clickable elements carry `data-attr` names (`hero_book_call`, `faq_reporting` and so on) for autocapture. Keep those names unchanged.

## Pending updates

- [ ] **Booking link:** once a Calendly link exists, put it in place of the `mailto:` on the "Book a 15-minute call" button in the `#contact` section. Keep `data-attr="footer_cta_book_call"`. The header and hero buttons scroll to `#contact`, so they need no change.
- [ ] **PostHog:** replace `REPLACE_WITH_POSTHOG_PROJECT_KEY` with the project key.
- [ ] **Meta tags:** add a favicon and Open Graph tags (title, description, image).
- [ ] **Phone number:** add one to the footer, if wanted.
- [ ] **Stats:** "1,700+ agents" appears in the hero stats and in the About section. Update both when it changes.
