# Content TODO — Placeholder Text to Personalise

Items below need real content before this site is production-ready.

---

## 1. About Page — Lorem Ipsum (HIGH PRIORITY)

**File:** `src/app/pages/about/about.component.html`

The entire About page body is filled with Lorem ipsum placeholder text (5+ paragraphs).
Replace it with the actual restaurant story: founding date, mission, cuisine focus, team, etc.

---

## 2. Menu Data — Sparse Descriptions

**File:** `src/app/services/order-details.service.ts`

Several food item descriptions are very thin or incomplete:

| Item | Current description | Problem |
|------|---------------------|---------|
| Paneer Burger | `"panner"` | Single misspelled word — needs a real description |
| Oreo Cheesecake Ice Cream | `"Oreo ice cream"` | Too short |

All six items could benefit from more appealing copy.

---

## 3. Footer — Social Media Links

**File:** `src/app/sharepage/footer/footer.component.html`

Three social links are placeholder `#` anchors:

| Platform | Current value | Action needed |
|----------|---------------|---------------|
| Facebook | `#` | Add real Facebook page URL or remove the icon |
| WhatsApp | `#` | Add WhatsApp Business link (`https://wa.me/YOUR_NUMBER`) or remove |
| YouTube | `#` | Add YouTube channel URL or remove |

Instagram is already set to `https://www.instagram.com/benitoish/` — no change needed.

---

## 4. Brand / App Name Mismatch

The internal `package.json` project name is `cloudkitchenweb`, but the visible brand name in the
navbar and footer is `KitchenWeb`. Decide on one canonical name and apply it consistently:

- `package.json` → `"name"` field
- `src/index.html` → `<title>` tag
- Navbar brand text
- Footer brand text
- Repository name (see `RENAME_THIS_REPO.md`)

---

## 5. Contact Form — No Real Functionality

**File:** `src/app/pages/contact/contact.component.html` and `.ts`

The form renders but does nothing on submit. Before launch either:
- Wire it up to an email service (EmailJS, Formspree, or a backend endpoint), or
- Add a visible note to users that the form is not yet active.

---

## 6. Order Form — No Real Functionality

**File:** `src/app/pages/menupage/menupage.component.html` and `.ts`

The "Place Order" button on the dish detail page has no click handler. Before launch either:
- Implement order submission (backend API, WhatsApp link, or email), or
- Remove the form if ordering is not yet supported.

---

## 7. Home Hero Banner

**File:** `src/app/pages/home/home.component.html`

- The "ORDER NOW" button links to the menu page — confirm this is intentional and the link is correct.
- The banner image (`assets/img/bannerimg.jpg`) is a single file — replace with your own branded photo.

---

## Summary Checklist

- [ ] Write real About page content
- [ ] Fix Paneer Burger and Oreo Cheesecake Ice Cream descriptions
- [ ] Add or remove Facebook, WhatsApp, YouTube links
- [ ] Unify brand name across package.json, index.html, navbar, footer
- [ ] Wire up or disable the Contact form
- [ ] Wire up or disable the Order form
- [ ] Replace banner image with branded photo
