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

A PostHog snippet in `<head>` loads only once `window.POSTHOG_KEY` is set to a real key (one that starts with `phc_`). Clickable elements carry `data-attr` names (`hero_book_call`, `faq_reporting`, `included_reporting` and so on) for autocapture. Keep those names unchanged.

## Pending updates

- [x] **Booking link:** all three "Book a call" buttons (header, hero, `#contact`) open the Google Calendar booking page (https://calendar.app.google/XsjKQ2XaTnitZFpUA) in a new tab.
- [x] **PostHog:** connected (US region, `us.i.posthog.com`). If the project is ever moved to EU, change `POSTHOG_HOST` to `https://eu.i.posthog.com`.
- [ ] **Open Graph tags:** add title, description and image for link previews. (The favicon is done: `favicon.svg`, `favicon.ico` and `apple-touch-icon.png`.)
- [ ] **Phone number:** add one to the footer, if wanted.
- [ ] **Stats:** "1,700+ agents" appears in the hero stats and in the About section. Update both when it changes.
