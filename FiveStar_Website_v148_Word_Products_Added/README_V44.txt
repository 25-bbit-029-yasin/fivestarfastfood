FIVE STAR WEBSITE — VERSION 44

One ZIP contains the complete website, private owner Admin Panel and shop Orders-only panel.

Owner Admin Panel: http://localhost:3000/admin-fivestar-kashmir-secure-2024
Shop Orders Panel: http://localhost:3000/staff-fivestar-kashmir-secure-2024

Run from the folder that contains package.json:
  npm.cmd install
  npm.cmd start

Shop staff default login: username shop; password [set STAFF_PASSWORD in environment variables]
Password eye icon is available. Forgot Password uses a recovery code, but recovery is not configured by default. The owner/server operator must configure db.orderStaffCredentials.recoveryCode in data/store.json (and preserve the existing username/password fields) before staff password reset can work. Change the default password before sharing access.

Shop Orders panel includes order listing/actions, cancel reason prompt, recover/completed states, new-order/status browser notifications and tone controls (built-in or custom audio upload). Tone files are stored in that browser's localStorage. Browser notification permission and a user gesture may be required.

The Orders-only page is not a separate server: keep the full project/server and share only the /orders.html URL and shop login. The owner Admin Panel remains the place for products, restaurant settings, ads, videos and other site assets.
