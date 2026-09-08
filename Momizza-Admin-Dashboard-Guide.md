# Momizza Admin Dashboard — Operator Guide

This guide is for the updated Momizza WordPress theme v1.2.0.

## Daily use

After login, open **Momizza** in the left menu. If the user has the **Momizza Manager** role, WordPress automatically opens the Momizza dashboard and hides most technical WordPress menus.

### Dashboard
- Today's order count and sales
- Orders that still need attention
- Menu product count
- Restaurant open/closed status
- Quick buttons for menu, orders, opening hours, ordering pause, payments, and business information

### Orders
- Filter by status or search by order/customer details
- Open an order to see items, quantities, totals, customer contact, address, order mode and payment method
- Change order status and add an internal note
- Call the customer directly from the order screen
- Print the order for the kitchen/counter

### Menu Products
- Add or edit food items
- Assign one or more categories
- Upload/change product image
- Enter a single price, or create options such as Regular / Medium / Large or Item / Combo
- Mark each option Available or Sold out
- Hide an item from the website without deleting it
- Mark the whole item sold out
- Move an item to Trash when it is no longer needed

### Categories
- Add/edit/delete menu categories
- Add a category description/note
- Upload/change category image
- The WooCommerce default category is protected from deletion

### Business Info
Manage brand name, phone, WhatsApp, email, full address, Google Maps, Facebook, Instagram, Google review URL, and GSTIN.

Instagram is preconfigured as:
https://www.instagram.com/momizza2026?utm_source=qr

### Opening Hours
Turn each day on/off and choose opening and closing times.

### Website & Design
Change the logo, hero copy and image, menu page copy, downloadable menu PDF, About content/image, Contact Form 7 shortcode and Momizza colours.

### Ordering
- Pause/resume all online ordering
- Enable/disable Takeaway, Dine-in and Delivery
- Optionally stop online orders automatically outside opening hours
- Set typical preparation time
- Set a minimum online order value
- Add a delivery note

### Payments / Razorpay
1. Install and activate the official **Razorpay for WooCommerce** plugin.
2. Open **Momizza → Payments**.
3. Paste your **test Key ID** and **test Key Secret** there.
4. Enable Razorpay and keep **Authorize and Capture** selected for the normal restaurant workflow.
5. Place a full test order on the website.
6. Confirm the order appears in WooCommerce and the payment appears in Razorpay.
7. When going live, replace the test keys with your live keys.

**Do not send your Key Secret in chat.** Enter it directly in WordPress. The saved secret is not shown back in the Momizza control panel.

## One-time administrator tasks
- Install WooCommerce
- Install Razorpay for WooCommerce
- Configure shipping/delivery zones and charges if delivery is enabled
- Configure GST/taxes if applicable
- Configure transactional email delivery/SMTP
- Create staff users with the **Momizza Manager** role
- Make a backup before updating plugins/themes or switching Razorpay to live mode
