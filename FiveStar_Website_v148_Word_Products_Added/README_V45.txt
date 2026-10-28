FIVE STAR WEBSITE — VERSION 45

One ZIP contains the complete website, private owner Admin Panel and shop Orders-only panel.

Owner Admin Panel: http://localhost:3000/admin-fivestar-kashmir-secure-2024
Shop Orders Panel: http://localhost:3000/staff-fivestar-kashmir-secure-2024

Run from the extracted folder that directly contains package.json:
  npm.cmd install
  npm.cmd start

Initial shop staff login (only if no custom credentials were already saved):
  Username: shop
  Password: [set STAFF_PASSWORD in environment variables]

Change the initial password from the Shop Orders page after login. Forgot Password uses a private recovery code; it is deliberately not displayed on the public login page. The owner/server operator must configure db.orderStaffCredentials.recoveryCode in data/store.json before staff password reset can work. Store that code privately and give it only to the owner. Existing saved shop credentials remain in effect, so the initial login may not apply if credentials were previously changed.

The Shop Orders page uses the same order card/detail/action layout as the Admin Panel Orders tab, including cancellation reason, recover order, mark completed, notifications and tone controls. Log out destroys the current session. Tone choices/custom audio are stored in that browser's localStorage; browser notification permission and a user gesture may be required.

The staff page is Orders-only. Owner products, prices, ads, videos, restaurant settings and other owner controls remain in the owner Admin Panel.
