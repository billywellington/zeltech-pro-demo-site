# Zeltech Pro — Website Redesign Overview

## 🎯 Purpose of This Document

This document outlines the changes required to transform the current Zeltech Pro website (new.zeltechpro.com) into the redesigned version. It serves as a high-level overview for the developer/web designer — the full technical specifications are in the accompanying **[Developer Spec Sheet](https://docs.google.com/document/d/1R6YLvSDCRR5ulLGyVsTGGBSaygnGVEug/edit?usp=sharing&ouid=112170131302431664109&rtpof=true&sd=true)**.

A **live demo site** has been built to illustrate exactly what the final website should look and feel like. All pages are functional and interconnected.

---

## 🔗 Demo Site

> **https://zeltech-pro-demo-site.pages.dev/**
>
> This demo is for illustration purposes. The developer should recreate these layouts in WordPress/Bricks using the spec sheet as the technical reference.

---

## 📄 Pages Covered

| Page | Demo Link | Status |
|------|-----------|--------|
| Homepage | [View Demo](https://zeltech-pro-demo-site.pages.dev/zeltech-homepage.html) | ✅ Complete |
| About Us | [View Demo](https://zeltech-pro-demo-site.pages.dev/zeltech-about.html) | ✅ Complete |
| Contact Us | [View Demo](https://zeltech-pro-demo-site.pages.dev/zeltech-contact.html) | ✅ Complete |
| Terms & Conditions | [View Demo](https://zeltech-pro-demo-site.pages.dev/zeltech-terms.html) | ✅ Complete |
| Privacy Policy | [View Demo](https://zeltech-pro-demo-site.pages.dev/zeltech-privacy.html) | ✅ Complete |
| Cookie Policy | [View Demo](https://zeltech-pro-demo-site.pages.dev/zeltech-cookies.html) | ✅ Complete |
| Hygiene Solutions | — | ⏳ To be designed |
| Consumables | — | ⏳ To be designed |
| Industrial Chemicals | — | ⏳ To be designed |
| Cleaning Services | — | ⏳ To be designed |
| Pest Control | — | ⏳ To be designed |
| Warranty | — | ⏳ To be designed |

---

## 🔑 Key Changes Summary

### Brand & Identity
- Company name standardised to **"Zeltech Pro"** everywhere (not "ZelTech", not "ZelTech Pro Cleaning")
- Trading hours corrected to **08:00 – 16:00** (was 17:00)
- **Logo is clickable** — clicking the logo on ANY page should redirect to the Homepage

### Design System (applies to ALL pages)
- Font changed to **Poppins** (Google Fonts) — weights 400, 500, 600, 700, 800
- Primary colour: **#01AAFF** (Bright Cyan Blue)
- All buttons are **pill-shaped** (border-radius: 50px) with cyan background and glow shadow
- Cards use **#F7FAFC** background with **#E2E8F0** borders and **14px** border-radius
- Icon circles: **64px** cyan gradient circles with white SVG icons
- Social media icons: **40px cyan circles** (Facebook, LinkedIn, WhatsApp only — Instagram removed)
- Consistent hover effects: cards lift up, buttons shift down, links turn cyan

### Heading Hierarchy (fixed across all pages)
- **H1**: One per page (page banner only) — was incorrectly H3 on all pages
- **H2**: Section headings — was incorrectly H3 on all pages
- **H3**: Card titles and sub-sections

### Navigation
- Sticky nav on scroll
- **Logo clicks → Homepage** (on every page)
- Login/user icon **removed**
- "Get A Quote" button links to Contact Us page
- "Products & Services" is **unclickable** until those pages are built
- Active page highlighted in cyan
- Mobile hamburger menu at 768px

### Footer
- 4-column layout on light grey (#F7FAFC) background
- Social icons: Facebook, LinkedIn, WhatsApp (Instagram removed, LinkedIn added)
- All links properly connected to their pages
- Copyright: "© 2026 Zeltech Pro. All Rights Reserved. Built by Infinity CDS"

---

## 🖼️ Images Used Per Page

All stock images are from free sources. The developer should download high-resolution versions from the links below and optimise them for web (compress, serve WebP where possible).

### Homepage
| Placement | Description | Source |
|-----------|-------------|--------|
| Hero background | Yellow gloves scrubbing floor with soap bubbles | [Unsplash](https://unsplash.com/photos/a-person-in-yellow-gloves-and-blue-gloves-cleaning-a-floor--dc38HdQR1M)  |
| CTA background | Squeegee cleaning glass | [Pexels](https://www.pexels.com/photo/anonymous-person-drying-mirror-with-squeegee-4239147/)  |

### About Us
| Placement | Description | Source |
|-----------|-------------|--------|
| Page banner | Colourful mop, sponges, spray bottles on blue background | [Freepik — Cleaning Service Concept](https://www.freepik.com/free-photo/colorful-composition-with-mop-sponges-rags-gloves-detergents-general-cleaning-cleaning-service-concept-background_13413431.htm) |
| CTA background | Same squeegee image as homepage CTA |[Pexels](https://www.pexels.com/photo/anonymous-person-drying-mirror-with-squeegee-4239147/)  |

### Contact Us
| Placement | Description | Source |
|-----------|-------------|--------|
| Page banner | Blue cleaning supplies — dustpan, cloth, spray bottle | [Freepik — Housekeeping Concept](https://www.freepik.com/free-photo/housekeeping-concept-with-space-left_1347774.htm) |

### Terms & Conditions / Privacy Policy / Cookie Policy
| Placement | Description | Source |
|-----------|-------------|--------|
| Page banner | Solid dark navy background (#1B2431) | No image needed |

### Image Formatting Notes
- **Hero/CTA images**: Use as `background-image` with `background-size: cover; background-position: center`
- **All banner images**: Apply dark overlay — `linear-gradient(160deg, rgba(27,36,49,0.72-0.82), rgba(27,36,49,0.52-0.65))`
- **Overlay opacity**: Hero = 0.72→0.52, About/Contact banners = 0.78→0.58, CTA = 0.82→0.65
- **Optimise all images**: Compress to <200KB, serve WebP with JPEG fallback

---

## 🏷️ Logo & Favicon Assets

| Asset | Google Drive Link | Usage |
|-------|-------------------|-------|
| Logo (for nav & footer) | **https://drive.google.com/drive/folders/1Jf4Dw4mHY2o5adBrvfblQxrghX2UIrtt?usp=drive_link** | Nav bar and footer — use transparent PNG, height 50px |

**Important:** The logo is **clickable on every page** and should always redirect to the Homepage.

---

## 📝 Changes Per Page

### Homepage
| What Changed | Details |
|---|---|
| Hero headline | Changed from "Smart Hygiene. Professional Cleaning. Trusted Results." to "The Western Cape's Trusted Cleaning & Hygiene Partner" |
| Hero subtitle | "Serving businesses, homeowners, and property managers / with 5+ years of 5-star service." |
| Hero tagline | "Smart Hygiene..." moved to small text above H1 |
| Hero image | New stock photo (floor scrubbing with yellow gloves) |
| Hero buttons | Two buttons: "Get A Quote" (cyan) + "Browse Products & Services" (transparent) |
| Services section | Heading changed to "Our Products & Services", subtitle removed |
| Services layout | Changed from 5-in-a-row to 3 top + 2 centred below |
| Services descriptions | All 5 card descriptions rewritten to be more specific |
| Services buttons | Changed to solid cyan pills (was text links) |
| Hygiene button text | Changed to "View Products" (was "Explore Hygiene Products") |
| Why Choose section | Placeholder subtitle removed, "Expertise" duplicate description fixed |
| Testimonials heading | Changed to "What People Are Saying" |
| Testimonials | Now shows 3 at a time in a carousel with auto-rotate (5.5s), 18 total reviews |
| About section | **Removed entirely** from homepage |
| Products section | **Removed entirely** from homepage |
| New: Clientele | Added "Our Trusted Clientele" auto-scrolling marquee (11 clients) |
| New: Partners | Added "Our Partnered Services" auto-scrolling marquee (4 partners) |
| CTA | New section with different image (squeegee), "Get A Quote" + "WhatsApp Us" buttons |

### About Us
| What Changed | Details |
|---|---|
| Banner | New cleaning supplies image (was same as homepage) |
| "Our Story" heading | Changed to "Who We Are" |
| Story text | SEO-enhanced with Western Cape location keywords, no bold |
| Team photo | Removed |
| New: Stats bar | Dark navy bar with animated counters: 5+ Years, 5.0 Rating, 100+ Clients (scroll-triggered, 3 seconds) |
| Mission section | Kept 4 values (Quality, Health, Trust, Sustainability) with subtitle |
| Values section | Kept 4 values (Excellence, Reliability, Professionalism, Responsibility) |
| "Why Choose" | Reworked as "What Sets Us Apart" — 6 cards in 3x2 grid, different heading |
| CTA | "Ready to Work With Us?" (different from homepage) |

### Contact Us
| What Changed | Details |
|---|---|
| Banner | New blue cleaning supplies image |
| Form layout | Form on top (full-width card), contact info below |
| Contact info | 4 info cards (Address, Phone, WhatsApp, Email) with clickable links |
| New: Hours bar | Dark navy strip showing "Monday – Friday, 08:00 – 16:00" |
| Map | Google Maps embed — 10 Van Ryneveld Street, Strand, Cape Town, 7130 |
| Social section | 3 branded pill buttons (Facebook, LinkedIn, WhatsApp) |
| FAQs | Rewritten and expanded to 8 questions with accordion animation |
| Typo fixed | "5-Star Rates Service" → "5-Star Rated Service" |

### Terms & Conditions
| What Changed | Details |
|---|---|
| Banner | Solid dark navy (was image) |
| Heading hierarchy | Fixed: H1 banner → H2 sections → H3 sub-sections |
| Company name | "Zeltech Pro Cleaning, Hygiene & Maintenance" → "Zeltech Pro" |
| Lists | Custom cyan bullet dots |

### Privacy Policy & Cookie Policy
| What Changed | Details |
|---|---|
| Same structural fixes as Terms | Heading hierarch, styling, solid dark navy banner |

---

## 🎨 Assests Still Yet To Be Provided

| Asset |
|---|
| Client logos (11) | 
| Partner logos (4) |

---

## 📎 Reference Files

| File | Description |
|---|---|
| [Developer Spec Sheet](https://docs.google.com/document/d/1R6YLvSDCRR5ulLGyVsTGGBSaygnGVEug/edit?usp=sharing&ouid=112170131302431664109&rtpof=true&sd=true)  | Complete technical spec with every detail |
| [Demo Site](https://zeltech-pro-demo-site.pages.dev/) | Live demo of all 6 pages |

---
