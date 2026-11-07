# MD Barber Shop

A modern, responsive website for **MD Barber Shop**, a premium grooming business in Subang Jaya, Malaysia.

Customers can explore barber services, view haircut styles, browse grooming products, and request appointments directly through WhatsApp.

## Features

- Responsive design for desktop, tablet, and mobile.
- Modern barber shop design with smooth animations.
- Sticky navigation bar.
- 10 barber services with descriptions and tags.
- Appointment booking through WhatsApp.
- Booking time slots from 10:00 AM to 2:00 AM.
- Portfolio gallery showcasing haircut styles.
- Grooming product shop.
- Shopping cart with saved cart count.
- Form validation.
- Smooth scrolling and scroll animations.
- Basic SEO optimization.

## Business Information

- **Business Name:** MD Barber Shop
- **Opening Hours:** Daily, 10:00 AM – 2:00 AM
- **Location:** Subang Jaya, Malaysia
- **Booking Method:** WhatsApp

## Services

1. Classic Haircut
2. Skin Fade
3. Beard Trim
4. Hot Towel Shave
5. Line-Up & Edge
6. Kids Haircut
7. Wash & Style
8. Hair Colouring
9. Scalp Treatment
10. Cut + Beard Combo

## Products

The website includes a product section featuring:

- Hair Clay
- Beard Oil

More products can be added in the future.

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Google Fonts
- Unsplash Images
- WhatsApp API

No frameworks or build tools are required.

## Project Structure

```text
MD-Barber-Shop/
|
|-- index.html
|-- README.md
```

## How to Run

1. Download or clone the project.
2. Open the project folder.
3. Locate the `index.html` file.
4. Double-click `index.html` to open it in your browser.

Alternatively, run a local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## WhatsApp Booking Setup

The website uses WhatsApp to send appointment requests.

The WhatsApp number should be configured in the JavaScript section of `index.html`.

Use the international format without spaces or special characters.

Example:

```javascript
const WHATSAPP_NUMBER = "60182173415";
```

Customers can enter their details, select a service, choose a date and time, and send their booking request through WhatsApp.

Bookings must be confirmed directly by the shop.

## Opening Hours Configuration

The website operates daily from:

- Opening: 10:00 AM
- Closing: 2:00 AM (next day)

The booking system supports appointments after midnight.

## Deployment

The website is a static website and can be hosted using:

- GitHub Pages
- Cloudflare Pages
- Vercel
- Netlify

No backend or database is required.

## Future Improvements

- Add service prices and estimated durations.
- Add barber profiles.
- Add customer reviews and testimonials.
- Add a location and Google Maps section.
- Develop a complete shopping cart and checkout system.
- Add online payment integration.
- Improve product management.

## Credits

- Images: Unsplash
- Fonts: Google Fonts
- Booking: WhatsApp

---

© 2026 MD Barber Shop. All Rights Reserved.
