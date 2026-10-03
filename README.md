# Shrushti MAHIRA Select — Tradition Meets Tomorrow

Shrushti MAHIRA Select is an exquisite, heritage Indian luxury fashion e-commerce storefront. The site celebrates Indian textile artistry, weaving traditions, hand-drawn Kalamkari crafts, Chanderi silks, Chikankari kurta sets, and modern silhouettes.

## Features

- **Cinematic Experience:** Atmospheric void lighting, animated curtain intro reveals, and dust particle effects powered by HTML5 Canvas and GSAP.
- **Dynamic Catalogue & Collections:** Driven by a centralized catalog model (`js/shop-data.js`) with responsive category landing pages (`/category?c=women`, `/category?c=kalakaari`), subcategory filtering (`/shop?c=women&s=sarees`), and interactive product detail views (`/product?p=ms-101`).
- **Complete Shopping Journey:** Interactive cart, address selection, payment mock flow, order placement confirmation, tracking timeline (`/track`), and email preview confirmation (`/email-preview`).
- **Client-Side State Persistence:** Fully operational cart, wishlist, address book, and order management using local storage.
- **Visual Design & Typography:** Editorial typography using Google Fonts (Playfair Display, Cormorant Garamond, Montserrat, Great Vibes) and custom vector ornamentation.
- **Authentication Flows:** Dedicated Sign In and Sign Up portals with client-side form validation and social login options.

## Technology Stack

- **Markup & Styling:** Vanilla HTML5, CSS3 with custom variables and responsive grid/flexbox layouts.
- **Animation:** GSAP 3.13, CustomEase, ScrollTrigger.
- **Deployment:** Netlify static hosting with clean URL redirection rules (`_redirects` and `netlify.toml`).

## Running Locally

To run the project locally, serve the repository root with any local HTTP server:

```bash
# Using Python
python3 -m http.server 8080

# Using Node.js (npx serve or http-server)
npx serve .
```

Open `http://localhost:8080` in your browser.
