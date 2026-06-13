# KitchenWeb

A cloud kitchen / food-ordering landing site built with Angular. Visitors can browse a menu of
Indian vegetarian dishes, view individual item details, and fill in an order form — all in a
responsive single-page app styled with Bootstrap 5.

**Live demo:** https://benitoinhiskitchen.netlify.app

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Angular 13.2 |
| Language | TypeScript 4.5 |
| Styling | CSS (global) + Bootstrap 5.1.3 (CDN) |
| Icons | Bootstrap Icons 1.8.1 (CDN) |
| Build tool | Angular CLI 13.2 |
| Hosting | Netlify |
| CI | GitHub Actions |

---

## Features

- **Home page** — hero banner ("Fresh Cooked Food At Your Door"), 3-step ordering guide, and a
  "Customers Favourites" section showing the top 4 menu items.
- **Menu page** — full grid of all dishes with name, description, price, and a Buy Now link.
- **Menu detail page** — individual dish view with an order form (name, mobile, delivery address).
- **About page** — restaurant story section *(placeholder text — see [CONTENT_TODO.md](CONTENT_TODO.md))*.
- **Contact page** — contact form with name, email, and mobile fields.
- **Navbar & footer** — shared layout with nav links and social media icons.
- **Lazy-loaded routing** — `PagesModule` is lazy-loaded for a faster initial load.
- **OnPush change detection** — applied to every component for performance.
- **Responsive design** — Bootstrap grid adapts to mobile and desktop.

---

## Local Setup

Prerequisites: Node.js 16+ and npm 8+.

```bash
# 1. Install dependencies
npm install

# 2. Start the dev server
ng serve

# Open http://localhost:4200
```

---

## Build for Production

```bash
ng build --configuration production
# Output is placed in dist/cloudkitchenweb/
```

---

## Deploy to GitHub Pages

```bash
# Install the deploy schematic once
npm install -g angular-cli-ghpages

ng build --configuration production --base-href="/cloud-kitchen-angular/"
npx angular-cli-ghpages --dir=dist/cloudkitchenweb
```

> Replace `cloud-kitchen-angular` with your actual repository name if different.

---

## Screenshots

![Home Page](docs/home.png)
![Menu Page](docs/menu.png)

*(Add screenshots to a `docs/` folder and update the paths above.)*

---

## Known Limitations

- **Contact form does not send emails.** The Submit button has no click handler and no HTTP call
  is wired up. To fix this, integrate a service such as EmailJS, Formspree, or a backend API.

- **Order form ("Place Order") does not submit orders.** The form on the menu detail page collects
  name, mobile, and address, but the Place Order button has no action attached. No order is
  recorded or transmitted.

- **Social media links are placeholders.** Facebook, WhatsApp, and YouTube links in the footer
  point to `#`. Only the Instagram link is real (`@benitoish`).

---

## Known Issues

- **Built with Angular 13 — upgrade to Angular 17+ planned.** Angular 13 reached end-of-life in
  November 2023. Upgrade path: `ng update` from 13 → 14 → 15 → 16 → 17.

---

## Project Structure

```
src/
  app/
    pages/          # Feature module (lazy-loaded)
      home/
      menu/
      menupage/     # Individual dish detail + order form
      about/
      contact/
    services/
      order-details.service.ts   # In-memory food menu data (6 items)
    sharepage/
      navbar/
      footer/
    shared/
  assets/
    img/
  environments/
```

---

## Available Scripts

- `npm start` — run the dev server with live reload
- `npm run build` — production build
- `npm test` — unit tests with Karma / Jasmine

---

## CI/CD

GitHub Actions:

- **ci.yml** — runs tests and a production build on every push/PR to `master`.
- **auto-commit.yml** — daily automated timestamped commit at 10:00 UTC.

---

## Contributing

1. Fork the repo and create a feature branch.
2. Run `npm test` before opening a PR.
3. Open a pull request against `master`.
