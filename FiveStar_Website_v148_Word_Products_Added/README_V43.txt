FIVE STAR WEBSITE — VERSION 43

Changes:
- Order details appear before ringtone settings in the owner Admin Panel.
- Per-event built-in/custom audio tone choices and Test controls. Custom audio is saved in the browser that selected it.
- Separate Orders-only staff page at /orders.html with a separate login; it does not display owner menu/settings/videos/ads controls.
- Default shop staff login: username shop, password [set STAFF_PASSWORD in environment variables] Change this in server.js function orderStaffCredentials before sharing a deployed site.
- Keep the full owner ZIP private. Share the live /orders.html URL and shop credentials only. Do not send the full project ZIP to shop staff.

Run: extract ZIP, enter the v42 folder, run npm.cmd install then npm.cmd start. Owner panel: http://localhost:3000/admin-fivestar-kashmir-secure-2024. Shop orders page: http://localhost:3000/staff-fivestar-kashmir-secure-2024.

Note: custom tones are browser/device-specific. Change the default shop password before deployment. Full browser testing has not been performed.
