Five Star Website v57 — regression fixes

Changes in this update:
- Kept the existing project structure and COD-only checkout.
- Removed the raw Status/Placed timestamp line from admin and staff order cards; daily order grouping remains.
- Restored TODAY'S ORDERS and YESTERDAY'S ORDERS grouping on the staff Orders page as well as the admin panel.
- Replaced the White page/Dark page text toggle with a sun/moon icon while preserving the existing theme preference key.
- Fixed customer cancellation reason inputs so the 5-second status polling does not constantly rebuild the order cards; typed text, focus, and cursor position are preserved when an update does require rendering.
- Added a map-based delivery location picker using OpenStreetMap/Leaflet with reverse geocoding and optional current-location selection. Customers can still type the address manually.
- Kept shop closing/reopening-time controls and server-side blocking for website orders when the shop is closed.
- Kept the existing cart checkout buttons above the saved customer orders.

Run from this folder (the folder containing package.json):
  npm.cmd install
  npm.cmd start

Map features require an internet connection. Current-location selection requires the browser's location permission. Syntax checks were run; a full live browser/end-to-end test has not been performed.
