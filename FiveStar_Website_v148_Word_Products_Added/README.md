# Five Star Fast Food & Kashmiri Barfi

## Run locally
1. Extract this ZIP into a folder.
2. Open PowerShell in that extracted folder (the folder containing `package.json`).
3. Run `npm.cmd install`
4. Run `npm.cmd start`
5. Open `http://localhost:3000`

Admin panel: `http://localhost:3000/admin-fivestar-kashmir-secure-2024`

Default admin login (change it in Admin account security after signing in):
- Username: `admin`
- Password: `[set ADMIN_PASSWORD in environment variables]`

## Latest updates
- Cart quantity controls, remove item controls and recalculated subtotal.
- Blue scroll arrows with frosted white-glass hover state.
- About page headings, subtitles, descriptions, main image/gallery, and up to three separately editable content containers are configurable in Admin Panel > About page & images.
- Deals now have both `Show deal on website` and `Feature on Home page` controls.
- The ZIP has `package.json` at its top level so npm commands run from the extracted root folder.


Version 16 update: WhatsApp hover remains circular with a subtle zoom and higher position; removed the Sides tab/category; Dahi quantity prompt is in English and supports decimal kg quantities; scroll arrows hide while cart drawer is open; mobile navigation dropdown is strengthened for small screens.

## v87 updates (2026-10-25)
- Replaced the Home page Dahi Bhallay category tile photo with a single bowl image showing yogurt, bhallay, chutneys and garnish; the product fallback uses the same image.
- Replaced the Drinks category tile and blank-image drink product fallbacks with one classic chilled glass cola bottle image (single item, no product collage).
- Customer Orders lists in both Admin and Shop Staff pages have a bounded height and vertical scrolling so controls below remain reachable.
- Moved the Shop Staff account form from the Admin Orders section to Admin account, under the heading “Admin and Shop Staff Account”; password update functionality is retained.
- Validation: Node syntax checks and ZIP integrity check passed. Full browser end-to-end testing was not performed.


## v117 order scrolling investigation
- Root document scroll is assigned to `html`; `body.admin-body` no longer creates a competing vertical scroll container. The orders list remains independently scrollable when long.
- JavaScript syntax and ZIP integrity checks are run for this release. Browser end-to-end testing is not claimed.

## v118 updates (2026-10-26)
- Customer Orders heading, help text, refresh controls and status notice remain sticky at the top while the page scrolls through the full orders list. The orders list itself no longer creates a second vertical scroll area.
- Done label is left-aligned in the order action area.
- Pending/newer orders are grouped above customer-cancelled review orders, with completed orders grouped below active orders.
- Customer-cancelled orders show Recover and OK actions. Recover restores the order to active status; OK permanently removes the customer-cancelled order after confirmation.
- Customer-cancelled orders are automatically removed after 10 minutes unless recovered or permanently removed earlier. Cleanup is server-side and also runs periodically.
- Validation: Node syntax checks and ZIP integrity checks are run. Full browser end-to-end testing was not performed.


## v119 updates (2026-10-26)
- Customer-cancellation OK buttons use a subtle translucent black background so the underlying panel color remains visible.
- Shop Staff page now clears the staff login session whenever the page is loaded or refreshed and requires the password again. This also covers reopening the page after closing the tab/browser, rather than relying on manual logout.
- Cache-busting versions updated for changed CSS and scripts.
- Validation: Node syntax checks and ZIP integrity check run after packaging; no live browser end-to-end test was performed.


## v120 Authentication behavior fix
- Shop Staff / Shop Stocks page now checks the existing `/api/orders-staff/me` session on load, matching the Admin panel's session-check behavior.
- Refreshing or reopening the page does not proactively log out the staff session; login is shown only when the server session is not authenticated.
- The explicit Logout button still logs the staff user out.


## v121 update
- Delivery map picker interface and all map-related status/error messages are in English, including on mobile.
- Mobile cart heading now stays flush to the top edge as cart details scroll behind it.

## v122 updates
- The desktop cart heading remains sticky while cart content scrolls.
- On mobile, the browser Back button closes an open cart or navigation menu before navigating to the previous page.


## v127 update (2026-10-26)
- Admin and Shop Staff now share one ringtone chooser design per event, with built-in tones and multiple custom audio files in the same menu. Custom audio uses IndexedDB to avoid localStorage size limits. Choose a tone, test it, then save it; the menu includes “+ Add ringtone”.
- Shop Staff session check now depends only on the Shop Staff login session, not on Admin login state. Staff logout is independent of Admin logout.
- Moved the Call Us helper sentence above the phone number.
- Cache-busting versions updated for panel scripts and stylesheet.
- Validation: JavaScript syntax and ZIP integrity checked. Browser/mobile end-to-end testing has not been performed in this environment.
