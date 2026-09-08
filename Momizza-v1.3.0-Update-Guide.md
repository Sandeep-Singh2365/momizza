# Momizza v1.3.0 Update Guide

## Install
1. Back up the WordPress database and files.
2. Go to **Appearance → Themes → Add New → Upload Theme**.
3. Upload `momizza-wordpress-theme-v1.3.0.zip`.
4. Choose **Replace current with uploaded** when WordPress detects the existing Momizza theme.
5. Clear any WordPress/cache-plugin/CDN cache after updating.

Your products, orders, Razorpay settings, Momizza settings and users remain in the database and are not replaced by the theme ZIP.

## Header text
The word beside the logo is now separate from the restaurant location.

Go to **Momizza → Business Info → Header text beside logo** and set it to `MOMIZZA`.

The separate **Location / town** field can remain `Kharar`. The header text is visible on desktop, tablet and mobile.

## Counter Favourites
Go to **Momizza → Counter Favourites**.

- Turn on the products you want on the homepage.
- Use Homepage order `1`, `2`, `3`, etc. to control their order.
- The homepage shows the first six enabled products.
- These cards no longer open WooCommerce product pages. They use the same add-to-cart / variation / quantity behaviour as the menu page while retaining the special Counter Favourites card styling.

The individual product editor also has a **Counter Favourite** toggle, but the dedicated Counter Favourites screen is the easiest place to manage the homepage set.

## Cart and menu quantities
After an item or variation is added:

- `/menu` changes its Add/variation control into a `− quantity +` stepper.
- The same product shown in Counter Favourites is synchronized automatically.
- The modal cart has its own inline `− quantity +` stepper and Remove action.
- Reducing quantity from `1` to `0` removes the item and restores the Add button on menu/home controls.

## Footer
The theme now renders the WordPress **Footer Menu** location correctly. If a footer menu is assigned, it will be used. If none is assigned, the theme automatically shows:

- Home
- Menu
- Our Story
- Visit

The footer logo now links to the homepage. Facebook and Instagram are rendered as horizontal social icons using the URLs from **Momizza → Business Info**.

## Checkout
Classic WooCommerce checkout and WooCommerce Checkout Blocks now use stronger field labels, more suitable filled-field surfaces, and gold focus states so entered information remains clearly readable against the Momizza dark theme.

## Recommended test after updating
1. Add one simple product from `/menu`, then use `+` and `−` on the menu item.
2. Add a pizza/variable product and verify each size has its own quantity.
3. Open the modal cart and change quantities there.
4. Verify the same quantity appears on a Counter Favourite if that product is also shown there.
5. Check the footer links and both social icons.
6. Fill every checkout field and verify labels remain readable.
7. Complete one Razorpay test-mode order before making the update live to customers.

If an Elementor Pro Theme Builder header or footer has been enabled separately, that Elementor template can override the theme's native header/footer. If the header/footer changes do not appear after clearing caches, check **Templates → Theme Builder** for an active replacement header/footer.
