# MD Barber Shop: Website

A single-page website for **MD Barber Shop** (SS15, Subang Jaya, Selangor). It shows services, a portfolio gallery, a product shop with a cart, Google review screenshots, a booking form, and a map. Bookings and product orders are sent through WhatsApp.

The whole site is one self-contained file, `index.html`. There is no build step and no dependencies to install.

## Features

- **Hero** with a live open/closed badge (Malaysia time), animated headline, barber-pole motif and gold-dust particles.
- **Services**: 14 services, each with an icon, price and category tag. They are generated from one list in the script.
- **Gallery**: 4 looping muted video clips and a photo. Clips play only while on screen. Clicking opens a lightbox.
- **Shop**: 5 products with a cart drawer. The cart is saved in `localStorage`. "Order on WhatsApp" sends a pre-filled order message.
- **Reviews**: tabbed section with review screenshots, optional text reviews, and links to read or write a Google review.
- **Booking form**: name, WhatsApp number, service, date and time. It opens WhatsApp with the details filled in.
- **Visit**: address, hours, social links, an embedded map, and directions and Google Maps buttons.
- **Extras**: preloader, scroll progress bar, sticky shrinking header, scroll reveal and counters, 3D card tilt, magnetic buttons, cursor glow, and a floating WhatsApp button.
- **Accessibility and motion**: respects `prefers-reduced-motion`, has a `<noscript>` fallback, keyboard-operable gallery, tabs and cart, and ARIA labels.
- **Analytics**: Google Tag Manager (container `GTM-53GVGM8K`).

## Running it

Open `index.html` in a browser. To serve it locally, run:

    python3 -m http.server 8000

then visit http://localhost:8000

It can be hosted on any static host (GitHub Pages, Netlify, Cloudflare Pages, or plain web hosting). Upload `index.html` and nothing else.

## Editing content

Most changes are in the `<script>` block near the bottom of `index.html`, under `/* ---------- Settings: edit here ---------- */`.

| What to change | Where |
|---|---|
| WhatsApp number | `WHATSAPP_NUMBER` (international format, no `+`, e.g. `60182173415`) |
| Address (used for the map and directions) | `ADDRESS` |
| Opening hours (logic) | `OPEN_HOUR` and `CLOSE_HOUR` (`26` means 2 AM the next day) |
| Services, prices, icons, tags | the `SERVICES` array. The dropdown, marquee and counter update automatically. |
| Social links | the `SOCIALS` array |
| Text reviews | the `REVIEWS` array. Leave it empty to show only screenshots or a "read on Google" card. |
| Google review link | `GOOGLE_REVIEWS_URL`. It currently opens a Maps search. Swap in your exact review link when you have it. |
| Products | the `<article class="card product">` blocks in `#shop`. Set `data-product` and `data-price` on the button. |
| Cart storage key | `CART_STORAGE_KEY` (change the version suffix to reset all saved carts) |

### Opening hours appear in several places

The hours are hard-coded as text in these places, so update them all if they change:

- the hero badge (`OPEN DAILY · 10 AM – 2 AM`)
- the "Opening hours" block
- the booking form hint
- the footer
- the stats counter (`data-count="16"` for hours open daily)
- the status text in `updateStatus()`

## Media

Images, videos and icons are embedded in the file as base64 `data:` URIs, so the page works as a single file. This makes `index.html` about **12 MB**.

- To swap a photo or video, replace the `src` of the matching `<img>` or `<video>`.
- For faster loading, move the media into files (for example an `assets/` folder) and point `src` at them.
- The hero background image and the fonts (DM Sans, Playfair Display) load from the web (Unsplash and Google Fonts).

## Notes on the booking and ordering flow

There is no backend. Both the booking form and the cart build a text message and open `https://wa.me/<number>?text=...`. The customer must press **Send** in WhatsApp for the request to reach the shop. Slots between 12 AM and 2 AM fall on the day after the selected date, as the form hint says.

## Project structure

    index.html   # the entire site: HTML, CSS and JS (media embedded)
    README.md

Inside `index.html`: `<style>` holds all CSS (sections marked with `/* ---------- Name ---------- */`), then the HTML sections (`hero`, `services`, `work`, `shop`, `reviews`, `booking`, `visit`), then one `<script>` with all behaviour.

## Changelog

- **Fix:** the Google Tag Manager script had been pasted inside the `header { ... }` CSS rule, which broke the header styling and stopped GTM from loading. The standard GTM snippet is now at the end of `<head>`, and its `<noscript>` iframe is right after `<body>`.

## Contact

WhatsApp: 018-217 3415
5, Jalan SS 15/4c, SS 15, 47500 Subang Jaya, Selangor
Open daily, 10 AM – 2 AM
