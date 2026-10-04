# GA Compliance Pro

Marketing site for GA Compliance Pro, a done-for-you license compliance service for Georgia real estate brokerages. The site has one job: get visitors to book a 15-minute call.

## Structure

`index.html` is the whole site. It's a single self-contained file with all CSS inline, no JavaScript, no dependencies and no build step. The only external resource is the Inter font from Google Fonts.

## Deploying

Upload `index.html` to any static host: Vercel, Cloudflare Pages, Netlify or GitHub Pages. Then point `gacompliancepro.com` at it.

## Design tokens

Keep these consistent. They're defined as CSS variables in `:root`.

| Token | Value     |
| ----- | --------- |
| Navy  | `#0F2540` |
| Gold  | `#C9933A` |
| Font  | Inter     |

## Pending updates

- [ ] Once a Calendly link exists, replace the `mailto:caitlyn@gacompliancepro.com` CTA button in the `#contact` section with it. The footer email can stay as a secondary contact.
- [ ] Add a phone number to the footer if desired.
- [ ] Update the "Offices Served" count in the stat bar (currently `6`) as the business grows. The "1,700+ agents" figure appears both in the stat bar and in the About section.
