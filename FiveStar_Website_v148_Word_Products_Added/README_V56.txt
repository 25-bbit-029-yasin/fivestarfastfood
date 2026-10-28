Five Star Website v56 - UI fixes and shop closing

Changes:
- Cart now displays selected cart items first, checkout/order buttons immediately beneath them, and saved website orders underneath the checkout actions.
- Admin order actions are kept on one row: Print slip, Make Complete, Cancel. Cancelled orders retain their existing recovery action.
- Shop & Restaurant settings tab makes the shop closing controls easier to find. Admin can set Shop is closed and an expected reopening time.
- Customer cart displays a red SHOP CLOSED notice and reopening information. Checkout submission is blocked in the browser while closed, and the server independently rejects new website orders while closed.
- Existing product selection and Cash on Delivery behavior retained.

Run from this folder (the folder containing package.json):
  npm.cmd install
  npm.cmd start

Note: source syntax checks were run with Node.js. A live browser/end-to-end test was not performed.
