# Momizza WordPress Theme — Deployment Guide

This is a native PHP/HTML/CSS/JS WordPress theme converted from the supplied Lovable/TanStack project. It keeps the original dark charcoal + Momizza red + gold visual system, Bebas Neue/Barlow typography, sticky translucent header, responsive mobile navigation, hero, menu category chips, menu/order interactions, cards, footer, and modal-style cart experience.

## What is already updated

- Address: Shop number 31, Shivjot Enclave, near Shivjot dhaba, Guru Teg Bahadur Nagar, Kharar, Punjab 140301
- Phone: +91 96468 11102
- Google Maps: https://maps.app.goo.gl/BoK2RvrEhY4MmenB6
- Facebook: https://www.facebook.com/share/1BrG8Wyjr
- Business hours from the supplied Momizza menu booklet
- Full menu data from `Momizza_Menu_Booklet.md`
- Original supplied `Momizza-Menu.pdf` bundled at `assets/downloads/Momizza-Menu.pdf`
- Menu PDF download buttons in the header, mobile menu, menu page and footer
- Contemporary WooCommerce Cart and Checkout styling for both classic templates and WooCommerce Blocks

## Recommended plugins

The theme works without these plugins for its basic pages, but install the ones you need:

1. **WooCommerce** — products, variations, cart, checkout and orders.
2. **Elementor** / **Elementor Pro** — page editing and Theme Builder. Elementor Pro header/footer locations are registered by the theme.
3. **ACF** / **ACF Pro** — ACF Pro adds a `Momizza Settings` options page. The normal WordPress Customizer is always available as a fallback.
4. **Contact Form 7** — optional contact form on the Visit page.

## Installation

1. Zip the `momizza-wordpress` folder (a ready-made zip is included in the handoff) and upload it at **Appearance → Themes → Add New → Upload Theme**.
2. Activate **Momizza**.
3. Set a custom logo at **Appearance → Customize → Site Identity** if you want to replace the bundled logo.
4. Create pages with these slugs:
   - `home` (set this as the static homepage under **Settings → Reading**)
   - `menu`
   - `about`
   - `contact`
5. Create a Primary menu under **Appearance → Menus**. If none is assigned, the theme automatically shows Home, Menu, Our Story and Visit.
6. If WooCommerce is active, let WooCommerce create/assign Cart and Checkout pages.

## Import the full menu into WooCommerce

Go to **Products → Import** and import:

`data/momizza-woocommerce-products.csv`

The CSV contains the supplied menu as WooCommerce products. Multi-price menu items (Pizza sizes, Burger/Combo, Sandwich/Combo, Fries sizes, etc.) are imported as variable products with selectable options. Items marked `MRP` or `—` are kept as non-priced menu items and can be edited later.

After importing, the `/menu` page automatically switches from the built-in fallback menu to the WooCommerce product catalog while retaining the Momizza menu design. Add-to-cart buttons use the theme's native AJAX endpoint and feed the WooCommerce cart drawer.

## Editing without ACF

Use **Appearance → Customize**:

- Business details, phone, address, map, Facebook and hours
- Hero copy and images
- Menu page copy and PDF file
- About/Story content and image
- Contact Form 7 shortcode
- Momizza red, gold, background, card, text, muted text and border colors

## Editing with ACF Pro

When ACF Pro is active, **Momizza Settings** appears in WordPress admin. Its fields override matching Customizer values. This is useful for centralized client editing.

## Elementor / Elementor Pro

- Any page edited with Elementor automatically uses Elementor's content instead of the corresponding built-in page composition.
- Use the included **Momizza Full Width (Elementor)** page template when you want the Momizza header/footer but fully custom page content.
- Elementor Pro Theme Builder can replace the theme header and/or footer because standard Theme Builder locations are registered.

## Contact Form 7

Create a Contact Form 7 form, copy its shortcode, and paste it into:

- **Appearance → Customize → Momizza - Content & Integrations → Contact Form 7 shortcode**, or
- **Momizza Settings → Contact** when ACF Pro is active.

The form inherits the Momizza visual theme automatically.

## Product and category images

The theme contains 20 local category food-image fallbacks in `assets/images/categories/`, made from the supplied menu artwork, plus a generic product fallback. This means newly imported products still have a visual treatment even before you add final WooCommerce product photography. Replace product featured images and category thumbnails from WooCommerce whenever ready.

## Menu PDF

The supplied PDF is already bundled and every PDF Menu button points to it by default. You can replace it from the Customizer or ACF Pro without editing theme files.

## Important deployment note

The theme intentionally does **not** override WooCommerce Cart/Checkout PHP templates. It themes WooCommerce's current classic and block markup with CSS instead, so WooCommerce updates are less likely to break checkout.

## One price item to confirm before go-live

The structured booklet gives one price per pizza size, while page 1 of the supplied visual PDF shows paired pizza values such as `189/209`, `319/359`, `449/499`. The WooCommerce import uses the structured booklet's first/single values. The exact PDF is preserved unchanged for download. Confirm what the second values mean before enabling live ordering/payment; see `data/PRICE-CONFIRMATION.txt`.
