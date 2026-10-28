Five Star website v55 updates

- Payment method is Cash on Delivery only; advance payment selection removed.
- Admin > Restaurant settings includes shop closed toggle and expected reopening time.
- Shop closed state is enforced by the server API as well as shown in the customer cart.
- Customer cancellation reason input is preserved when background order sync refreshes order cards.
- API responses are marked no-cache to help avoid stale admin/staff session views.

Run from the project folder containing package.json:
  npm install
  npm start

Note: Shop closure blocks website checkout API orders. WhatsApp handoff is also blocked by the customer UI when the current page knows the shop is closed.
