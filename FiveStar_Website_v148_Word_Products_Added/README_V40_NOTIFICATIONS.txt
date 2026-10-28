Five Star v40 update
- Added public order status-only endpoint so the customer page can reflect admin cancellation reason/status and completion without exposing full order details.
- Customer order cards persist in localStorage and poll order status while the website is open; cancelled cards expire after 15 minutes and completed cards are removed from the customer card.
- Admin order polling plays a distinct tone for newly received orders and status changes, with browser notifications when permission is granted.
- Browser notifications/audio require the relevant page to be open; browser policies may require a user interaction to enable audio. WhatsApp Send confirmation still cannot be detected through a standard wa.me link; WhatsApp Business API/webhook is required for verified WhatsApp message events.
- Validation performed: ZIP integrity and JavaScript syntax only; full browser/mobile/end-to-end testing remains necessary.
