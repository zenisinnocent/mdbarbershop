# MD Barber Shop

A responsive, single-page website for **MD Barber Shop**, a premium grooming business open daily from **10 AM to 2 AM**. Customers can browse services, view the portfolio, add grooming products to a cart, and request appointments directly through WhatsApp.

## Features

- **Responsive design**: works on desktop, tablet and mobile
- **Sticky header** with smooth-scroll navigation
- **10 services** shown as compact, ticket-style cards with icons, tags and hover effects
- **Late-night booking**: hourly slots from 10:00 AM to 2:00 AM (slots after midnight are clearly labelled)
- **Portfolio gallery** with hover effects and lazy-loaded images
- **Product shop** (Hair Clay, Beard Oil) with a cart counter saved in `localStorage`
- **WhatsApp booking form**: validates input and opens a pre-filled WhatsApp message
- **Single source of truth for services**: one list powers both the service cards and the booking dropdown
- **Scroll-reveal animations** using `IntersectionObserver`
- **Accessibility**: semantic HTML, labelled form fields, `aria-live` status messages, visible focus outlines
- **SEO basics**: page title and meta description

## Services

| # | Service | Tag |
| --- | --- | --- |
| 01 | Classic Haircut | Signature |
| 02 | Skin Fade | Popular |
| 03 | Beard Trim | Detail |
| 04 | Hot Towel Shave | Relax |
| 05 | Line-Up & Edge | Quick |
| 06 | Kids Haircut | Under 12 |
| 07 | Wash & Style | Fresh |
| 08 | Hair Colouring | Bold |
| 09 | Scalp Treatment | Care |
| 10 | Cut + Beard Combo | Best value |

## Tech Stack

- HTML5
- CSS3 (custom properties, Grid, Flexbox, media queries)
- Vanilla JavaScript (no frameworks or build tools)
- [Google Fonts](https://fonts.google.com/): DM Sans and Playfair Display
- Images from [Unsplash](https://unsplash.com/)

## Getting Started

No installation or build step is required.

```bash
# Clone the repository
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# Open in your browser
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Configuration

### WhatsApp number (required)

Booking requests are sent to WhatsApp. In `index.html`, replace the placeholder at the top of the `<script>` section:

```js
const WHATSAPP_NUMBER = "WHATSAPP_NUMBER_HERE";
```

Use the full international number with **no** `+`, spaces or dashes. For example, for a Malaysian number:

```js
const WHATSAPP_NUMBER = "60123456789";
```

### Services

Edit the `SERVICES` list in the `<script>` section. Each entry creates a card and a booking dropdown option automatically:

```js
{ name: "Skin Fade", icon: "◐", tag: "Popular", desc: "Seamless blend, razor-clean lines, sharp finish." }
```

### Opening hours

Hourly booking slots are generated from two values in the `<script>` section (24-hour clock, where `26` means 2 AM the next day):

```js
const OPEN_HOUR = 10;   // 10 AM
const CLOSE_HOUR = 26;  // 2 AM next day
```

Also update the hero badge text (`OPEN DAILY · 10 AM – 2 AM`), the booking form hint and the meta description if you change the hours.

### Other content

| What to change | Where |
| --- | --- |
| Shop name / branding | `<title>`, `.logo`, footer |
| Products and prices | `#shop` section (`RM` currency) |
| Gallery and hero images | `<img>` tags and `.hero` background |
| Colours | CSS variables in `:root` (`--gold`, `--black`, `--dark`) |

## Project Structure

```
.
├── index.html   # Markup, styles and scripts in one file
└── README.md
```

## How Booking Works

1. The customer fills in name, WhatsApp number, service, date and time.
2. The form is validated in the browser; past dates are blocked.
3. A WhatsApp chat opens (`wa.me`) with the booking details pre-filled.
4. The customer presses **Send** to confirm with the shop.

> Bookings are not stored on a server. Confirmation happens through the WhatsApp conversation.
>
> Time slots from 12:00 AM to 2:00 AM fall after midnight, on the day after the selected date. The shop should confirm the exact date with the customer on WhatsApp.

## Deployment

Because it is a static site, it can be hosted for free on:

- **GitHub Pages**: Settings → Pages → deploy from the `main` branch (root)
- **Netlify**, **Vercel** or **Cloudflare Pages**: drag and drop, or connect the repo

### Custom domain (optional)

To use your own domain with GitHub Pages, add these DNS records at your registrar, then enter the domain under Settings → Pages → Custom domain:

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `<your-username>.github.io` |

DNS changes can take from a few minutes up to 24 hours. If you use Cloudflare, set the records to **DNS only**.

## Roadmap

- [ ] Full cart / checkout view
- [ ] Service prices and durations
- [ ] Barber profiles
- [ ] Map and location section
- [ ] Customer testimonials
- [ ] Split CSS and JS into separate files

## Credits

- Photos from [Unsplash](https://unsplash.com/) photographers
- Fonts by Google Fonts

## License

Add a license of your choice (for example, [MIT](https://choosealicense.com/licenses/mit/)) and update this section.

&copy; 2026 MD Barber Shop
