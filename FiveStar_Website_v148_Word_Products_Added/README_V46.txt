Five Star Website v46 update

Changes: contact message form aligned with contact cards; removed the separate Cancel an Order section from Contact; kept server-side 30-minute cancellation rule; shop staff login copy is English; removed staff self-service Change Password UI; added mute/unmute notification toggles to owner and staff order pages; displayed Total Payment on both order lists; improved staff logout UI handling.

Run from the folder containing package.json:
  npm.cmd install
  npm.cmd start

Owner panel: http://localhost:3000/admin-fivestar-kashmir-secure-2024
Shop staff: http://localhost:3000/staff-fivestar-kashmir-secure-2024

Important: full browser testing and real notification behavior must be verified locally. Browser tones/notifications require the page open, prior user interaction, and browser permission. The current reset notification is recorded in server data; external email/SMS/push delivery is not configured.
