Five Star Fast Food & Kashmiri Barfi — v29 mobile menu fix

Changes:
- Mobile navigation panel is visible again and slides in from the right.
- Drawer uses content-based height (with a maximum height only for small screens), not full-screen height.
- Menu toggle stays in the top-right and becomes a white × close button while open.
- Brand/cart/header are hidden behind the drawer while open; closing restores the normal header.
- Backdrop, link close, outside click, Escape, cart behavior and desktop styling are retained.

Run from project root (folder containing package.json):
  npm.cmd install
  npm.cmd start
