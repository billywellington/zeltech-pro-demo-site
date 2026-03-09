# Logo Upload & Navigation Setup Instructions

This project currently uses embedded (`base64`) logos in the HTML.
To make logo updates easy for **desktop** and **mobile/tablet**, use the folders below.

## 1) Upload directories

Place your logo files in:

- `assets/logos/nav/desktop/` (desktop/full logo)
- `assets/logos/nav/mobile-tablet/` (mobile + tablet logo)

Recommended file names:

- `assets/logos/nav/desktop/nav-logo.png`
- `assets/logos/nav/mobile-tablet/nav-logo.png`

> You can use `.png`, `.webp`, or `.svg` as needed.

---

## 2) Replace nav logo source in each page

In each file below, find the navbar logo image line:

- `index.html`
- `zeltech-about.html`
- `zeltech-contact.html`
- `zeltech-cookies.html`
- `zeltech-privacy.html`
- `zeltech-terms.html`

Look for:

```html
<a href="#" class="nav-logo"><img src="data:image/png;base64,..." alt="Zeltech Pro"></a>
```

Replace with:

```html
<a href="#" class="nav-logo">
  <img
    src="assets/logos/nav/desktop/nav-logo.png"
    srcset="assets/logos/nav/mobile-tablet/nav-logo.png 768w, assets/logos/nav/desktop/nav-logo.png 1024w"
    sizes="(max-width: 768px) 52px, 220px"
    alt="Zeltech Pro"
  >
</a>
```

This keeps desktop using the desktop logo, while mobile/tablet can use the mobile/tablet logo.

---

## 3) Optional: keep existing footer logo unchanged

If you only want navbar logo control for now, do not change footer logo lines.

---

## 4) Current responsive behavior summary

- Tablet/desktop nav links are tuned to avoid stacked text/wrapping.
- Mobile menu still uses the hamburger menu.
- Very small screens keep compact logo behavior.

---

## 5) Quick verification checklist

After upload + replacement:

1. Open homepage on desktop width (`>=1280px`) and verify nav items stay on one line.
2. Open tablet width (`~900px`) and verify nav is readable/non-stacked.
3. Open mobile width (`<=560px`) and verify compact logo + hamburger layout.
