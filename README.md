# MD BARBERSHOP

Website for **MD Barber Shop**, a premium barber shop in SS15, Subang Jaya, Selangor, Malaysia. Open daily, 10 AM to 2 AM.

The whole site is one self-contained file (`index.html`). There is no build step, no framework, no server and no extra folders needed. The logo, photos, videos, product pictures and review screenshots are all saved inside the file. Because of that, the file is large (about 12 MB).

## Features

- Animated loading screen with a spinning barber pole, then a hero section with gold dust particles and a live "Open now / Closed now" badge (Malaysia time)
- Shop logo in the header and as the browser tab icon
- 14 services with prices, shown as tilting cards, plus a scrolling services strip
- "The Art of the Cut" gallery with four silent looping videos and a photo. Click any tile to view it full size
- Product shop with five products and a slide-out cart. The cart is saved in the visitor's browser and can be sent as an order on WhatsApp
- Google reviews section with a "Customer Reviews" tab (review screenshots) and a "Leave a Review" tab
- Booking form that opens WhatsApp with the customer's details filled in
- Visit section with address, opening hours, Google Map, directions and social links
- Floating WhatsApp button, scroll progress bar and smooth reveal animations
- Works on phones, tablets and desktops. Animations switch off for visitors who prefer reduced motion

## Services and prices

| Service | Price |
| --- | --- |
| Hair Dry Cut | RM 30 |
| Cut and Wash | RM 40 |
| Cut, Wash & Shave | RM 50 |
| Facial | RM 50 - 150 |
| Facial Wax with Ears | RM 40 |
| Shave | RM 25 |
| Beard Design & Trim | RM 25 |
| Black Colour | RM 70 |
| Hair Colour | RM 100 - 200 |
| Silver Colour | RM 300 |
| Rebonding | RM 100 - 250 |
| Hair Perm | RM 200 - 250 |
| Hair Treatment | RM 100 - 250 |
| Oil Hair Therapy | RM 100 |

## Products

All products are RM 50.00 each.

- Wild West American Pomade
- The Silka Barber American Pomade
- Wild West American Mud
- Spider Wax
- Silka Barber Hairspray

## Contact

- **Address:** 5, Jalan SS 15/4c, SS 15, 47500 Subang Jaya, Selangor
- **WhatsApp:** 018-217 3415
- **TikTok:** https://www.tiktok.com/@mdbarberss
- **Instagram:** https://www.instagram.com/mdbarbershopss15/
- **Facebook:** https://www.facebook.com/my.daring.saloon/

## Run locally

1. Download `index.html`.
2. Double-click it to open it in your browser.

Fonts, the map and the hero background photo load from the internet, so you need to be online to see them.

## Deploy on GitHub Pages

1. Create a repository and upload `index.html` to the root (the top level, not inside a folder).
2. Go to **Settings, then Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose the `main` branch and the `/ (root)` folder, then click **Save**.
5. After a minute or two, your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

If the old tab icon still shows after an update, refresh with Ctrl+Shift+R (Cmd+Shift+R on a Mac) or open the site in a private window. Browsers keep tab icons for a long time.

## How to edit the site

Open `index.html` in a text editor. Most things you will want to change are at the top of the `<script>` section near the bottom of the file.

| What to change | Where to find it |
| --- | --- |
| Browser tab title | The `<title>` tag at the top of the file |
| WhatsApp number | `WHATSAPP_NUMBER` (use the international format, for example `60182173415`) |
| Address and map | `ADDRESS` |
| Social media links | `SOCIALS` |
| Services, descriptions and prices | `SERVICES`. Each service has a `name`, `icon`, `tag`, `desc` and an optional `price`. A price can be a number such as `30` or a range written as text
