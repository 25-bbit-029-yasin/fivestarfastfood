Five Star v129 — Environment passwords and private panel URLs

Panel display names remain unchanged: Admin Panel and Shop Staff Panel.
Private panel URLs:
- /admin-fivestar-kashmir-secure-2024
- /staff-fivestar-kashmir-secure-2024

Required Vercel Environment Variables (Project > Settings > Environment Variables):
ADMIN_USER=admin
ADMIN_PASSWORD=choose-a-long-unique-password
STAFF_USER=shop
STAFF_PASSWORD=choose-a-different-long-unique-password
SESSION_SECRET=choose-a-long-random-secret

Set them for Production (and Preview/Development if needed), Save, then redeploy.
Never commit .env. .env.example contains placeholders only.

Local setup:
1. npm install
2. Copy .env.example to .env and replace every placeholder with your own values.
3. npm start

Notes:
- If the existing data store already contains adminCredentials or orderStaffCredentials, those saved credentials continue to be used. Back up the data before migrating saved credentials to environment variables.
- robots.txt is only a crawler instruction, not access control. Panel routes still require login.
- This project currently writes data to a local JSON file; Vercel serverless deployments do not provide durable local-file storage. Use a persistent database/object store before relying on order persistence in production.


PANEL PRIVACY NOTES
- Admin and staff panel responses include X-Robots-Tag: noindex, nofollow, noarchive and Cache-Control: no-store.
- Panel HTML also includes a robots noindex meta tag. robots.txt disallows the private panel paths. These are indexing hints, not access control; strong authentication and passwords remain essential.
- If SESSION_SECRET is not set, the server generates a random secret at startup. Set SESSION_SECRET in deployment environment variables to keep sessions stable across restarts.

LOCAL TEST CREDENTIALS (v131 convenience setup)
Admin Panel username: admin
Admin Panel password: ChangeMe123!
Shop Staff Panel username: shop
Shop Staff Panel password: ShopOrders123!

These credentials are included in the local .env file for convenient testing. Before deploying publicly, set your own strong values in the hosting provider's environment variables. Do not commit or upload .env to a public Git repository. Existing credentials already saved in data/store.json can override these defaults; if an older store.json exists, update credentials from the panel account settings or back up and reset that file only if you understand it will reset stored site data.

Version 132 product editing fix
- Product edit form now sets section/category options in a stable order and explicitly restores visibility checkboxes, avoiding accidental hiding caused by stale form state.
- Existing image URL is preserved when no new photo is selected.
