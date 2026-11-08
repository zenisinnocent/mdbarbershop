# MD BARBERSHOP

Website for **MD Barber Shop**, a premium barber shop in SS15, Subang Jaya, Selangor, Malaysia. Open daily, 10 AM to 2 AM.

The whole site is one self-contained file (`index.html`). There is no build step, no framework, no server and no extra folders needed. Photos, the video, the review screenshots and the logo icon are all saved inside the file.

## Features

- Animated intro with a spinning barber pole, a hero with gold dust particles and a live "Open now / Closed now" badge (Malaysia time)
- Services list with 3D tilt cards and a scrolling services strip
- "The Art of the Cut" gallery with photos and a video. Click any tile to view it full size
- Product shop with a slide-out cart. The cart is saved in the visitor's browser and can be sent as an order on WhatsApp
- Google reviews section with a "Customer Reviews" tab (review screenshots) and a "Leave a Review" tab
- Booking form that opens WhatsApp with the customer's details filled in
- Visit section with address, opening hours, Google Map, directions and social links
- Shop logo as the browser tab icon
- Floating WhatsApp button, scroll progress bar and smooth reveal animations
- Works on phones, tablets and desktops. Animations switch off for visitors who prefer reduced motion

## Contact

- **Address:** 5, Jalan SS 15/4c, SS 15, 47500 Subang Jaya, Selangor
- **WhatsApp:** 018-217 3415
- **TikTok:** https://www.tiktok.com/@mdbarberss
- **Instagram:** https://www.instagram.com/mdbarbershopss15/
- **Facebook:** https://www.facebook.com/my.daring.saloon/

## Run locally

1. Download `index.html`.
2. Double-click it to open it in your browser.

Fonts, the map and the stock photos load from the internet, so you need to be online to see them.

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
| Services and descriptions | `SERVICES` |
| Opening hours for booking slots | `OPEN_HOUR` and `CLOSE_HOUR` (hours are on a 24-hour clock, so 2 AM next day is `26`) |
| Google review links | `GOOGLE_REVIEWS_URL` and `GOOGLE_WRITE_URL` (replace with your own Google review link) |
| Written review cards | `REVIEWS` list. Each review has a `name`, `stars`, `text` and optional `when` |
| Product names and prices | The `Our Products` section in the HTML. Keep `data-product` and `data-price` on each Add to Cart button in step with the text shown |
| Opening hours text | Search for `10 AM` in the file |

### Adding a written review

Copy the review exactly as it appears on Google, with the reviewer's name, and add it to the `REVIEWS` list as an object with `name`, `stars`, `text` and `when`. Only add real reviews.

### Replacing photos, videos and the logo icon

The gallery photos, the gallery video, the review screenshots and the tab icon are embedded in `index.html` as data URIs, which is why the site works as a single file. To swap an image, replace the `src` value of that `<img>` tag with a normal path (for example `images/new-photo.jpg`) and upload that file to your repository too. For the tab icon, replace the `href` of the `<link rel="icon">` lines near the top of the file with the path to your logo (for example `logo.png`). A square image of at least 512 by 512 pixels works best.

The hero background and the two product photos are stock photos hosted by Unsplash. Replace them with your own photos when you have them.

## Built with

- HTML, CSS and vanilla JavaScript (no libraries)
- [Google Fonts](https://fonts.google.com/): Playfair Display and DM Sans
- [Google Maps](https://www.google.com/maps) embed for the location
- [Unsplash](https://unsplash.com/) stock photos for the hero and products

&copy; 2026 MD Barber Shop. Precision. Style. Excellence.
