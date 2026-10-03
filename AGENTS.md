# AGENTS.md

## Project Architecture

Mahira Select is built as a high-fidelity, high-performance static web application designed for deployment on Netlify. It provides a multi-page luxury e-commerce experience without heavy framework overhead.

### Key Directories & Files

- `index.html`: The primary homepage featuring the cinema intro, curtain drop effect, hero banner, featured collections, best sellers, craftsmanship seals, and editorial brand story.
- `category.html`: Dynamic category landing page parameterized by query parameter `?c=` (e.g. `women`, `kalakaari`).
- `shop.html`: Filterable product listing page parameterized by category and subcategory (e.g. `?c=women&s=sarees`).
- `product.html`: Interactive product details page (`?p=ms-101`) featuring color selection, size choices, zoomable galleries, add-to-bag, and buy-now actions.
- `cart.html`: Cart management page showing line items, quantity adjustments, order summary, and checkout entry.
- `checkout.html`: Multi-step checkout workflow managing shipping address entry and mock payment options (UPI, Card, Net Banking, COD).
- `order.html`: Order confirmation screen displaying generated order identifier and itemized summary.
- `track.html`: Order tracking interface with stage progression timelines and order lookup.
- `email-preview.html`: HTML email template preview representing the post-purchase confirmation sent to customers.
- `explore.html`: The journey directory showcasing every stage of the user experience and providing demo seed/reset controls.
- `login.html` & `signup.html`: Authentication screens featuring split editorial layouts and interactive form handling.
- `css/`:
  - `styles.css`: Core design system, CSS custom properties, navigation, cinematic animation styles, typography, and footer.
  - `shop.css`: E-commerce layouts, catalog grids, filter bars, product page galleries, cart, and checkout styling.
  - `auth.css`: Authentication pages layout and styles.
- `js/`:
  - `emblem-data.js`: Vector path and SVG drawing data for brand logos and lotus emblem elements.
  - `shop-data.js`: The central data store containing categories, subcategories, product definitions, color palettes, sizing, and pricing.
  - `shop.js`: Client-side logic for rendering catalogs, product details, managing the bag/wishlist state via `localStorage`, and controlling the checkout/order flow.
  - `main.js`: Homepage animations, particle canvas, curtain open triggers, smooth navigation, and search drawer.
  - `auth.js`: Authentication form interactivity and validation logic.
- `assets/`: Optimized imagery for hero banners, collection previews, and products.
- `_redirects` & `netlify.toml`: Netlify routing rules and cache headers.

### Conventions & Decisions

1. **State Persistence:** User shopping states (bag, wishlist, orders, addresses) are preserved in the browser using the `localStorage` keys `mahira.cart`, `mahira.wishlist`, `mahira.orders`, and `mahira.addresses`.
2. **Catalog Extensibility:** All product and category data resides exclusively in `js/shop-data.js`. Adding new items or collections does not require creating new HTML files.
3. **Clean URLs:** Netlify routing rules in `_redirects` allow seamless navigation to routes like `/shop`, `/product`, and `/checkout` without displaying `.html` extensions.
