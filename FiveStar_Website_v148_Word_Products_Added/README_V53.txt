Five Star Website - v53 updates

Updates included:
- Admin and Shop Staff order cards put the customer/order title first, then status, address, name, phone and payment details on separate lines.
- Print Slip button on each order. The print layout includes Five Star heading, itemized bill, payment type, customer contact/address and a friendly thank-you message.
- Dark page / White page toggle on Admin and Shop Staff panels.
- Customer cart shows the empty-cart callout and Explore Menu near the top, with saved orders below it.
- Saved customer orders display item summary, total, payment type, customer name, phone and address.
- Customer cancellation asks for a reason and sends it to the server.
- Checkout includes Cash on Delivery and Advance Payment choices. Advance payment deliberately asks customers to confirm the account number with the shop because the number supplied was incomplete (9 digits); do not send payment until the correct full number is confirmed.
- Server saves payment method and customer cancellation reason.

Run on Windows PowerShell from this extracted folder:
  npm install
  npm start
Then open http://localhost:3000

Note: This ZIP passed JavaScript syntax checks. Please test real order placement/cancellation and print dialog in your environment before live use. Advance payment account number must be updated when the full number is confirmed.
