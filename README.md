# MD Barber Shop – Website

Single-page website for **MD Barber Shop, SS15, Subang Jaya**. It's one self-contained HTML file with no build step and no dependencies. Open it in a browser, or upload it to any static host.

## Files

| File | Purpose |
|------|---------|
| `md-barbershop-simplified.html` | The full site, with all images and videos embedded. This is the file to deploy. |
| `md-barbershop-code-only.html` | Same code with the media replaced by `__B64_n__` placeholders. Use it for reading and editing. |

> Edit the code-only file, then paste the media back in. Alternatively, edit the full file directly in a code editor.

## Features

- Animated hero with an open/closed status badge (Malaysia time) and a barber-pole preloader
- Services grid, generated from a list in the script
- Gallery of 4 videos and 1 photo, with a lightbox
- Product shop with a cart drawer saved in `localStorage` and ordering through WhatsApp
- Google review screenshots, plus a tab for leaving a review
- Booking form that sends the request through WhatsApp
- Google Map, directions links, and social links
- Responsive layout, keyboard accessible, respects `prefers-reduced-motion`

## Editing content

All settings are at the top of the `<script>` block.

| What | Where |
|------|-------|
| WhatsApp number | `WHATSAPP_NUMBER` (international format, no `+`, e.g. `60182173415`) |
| Address and map | `ADDRESS` |
| Opening hours | `OPEN_HOUR` and `CLOSE_HOUR` (`26` means 2 AM the next day) |
| Services and prices | `SERVICES` array (`name`, `icon`, `tag`, `price`, `desc`) |
| Social links | `SOCIALS` array |
| Text reviews | `REVIEWS` array (empty by default) |
| Google review link | `GOOGLE_REVIEWS_URL` (currently a Maps search; swap in your exact review link) |

Some text is written directly in the HTML, so change it there too:

- hero text and the "OPEN DAILY" badge
- the stats numbers (`data-count`)
- the address and hours in the **Visit** section and footer
- the booking hint, which mentions "10 AM to 2 AM"
- the status text in `updateStatus()`

### Products

Products are plain HTML `<article class="card product">` blocks. Each has a `<button>` with `data-product` (name) and `data-price` (number). Add or remove a block and the cart picks it up automatically.

### Adding a review as text

```js
const REVIEWS = [
  { name: "Reviewer Name", stars: 5, text: "Exactly what they wrote.", when: "2 months ago" }
];
```

### Replacing images and videos

Media is embedded as base64 `data:` URIs. To swap one, replace the `src` (or `poster`) value with a new data URI or a normal file path such as `images/hero.jpg`. Linking to files makes the HTML much smaller.

## Customising the look

Colours and fonts are CSS variables at the top of `<style>`:

```css
:root {
  --gold: #c8a45d;  --gold-soft: #e6c987;
  --black: #101010; --dark: #1b1b1b;
  --serif: 'Playfair Display', serif;
  --sans: 'DM Sans', sans-serif;
}
```

## Deploying

Upload the file as `index.html` to any static host (Netlify, Vercel, GitHub Pages, Cloudflare Pages, or normal web hosting). No server code is needed.

## External services

- Google Fonts (DM Sans, Playfair Display)
- Unsplash (hero background image)
- Google Maps embed
- WhatsApp (`wa.me` links)

The page still works without these, but the fonts, hero background and map won't load.

## Notes

- The cart is stored in the browser's `localStorage` under `md-barber-cart-v2`. Payment is in store, and orders are confirmed on WhatsApp.
- The booking form doesn't store anything. It opens WhatsApp with a pre-filled message, and the customer has to press **Send**.
- Booking slots run from 10 AM to 2 AM. Slots after midnight fall on the day after the chosen date.

## License

© 2026 MD Barber Shop. All rights reserved.
