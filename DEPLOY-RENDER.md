# Atlantic Waves — Render deployment

Use this package as the project root when deploying to Render.

## Render settings
- Runtime: Node
- Build command: `npm install`
- Start command: `npm start`

## Environment variables
- `NODE_ENV` = `production`
- `SESSION_SECRET` = generate a long random value (Render can generate this)
- `DERIV_CLIENT_ID` = your Deriv OAuth client ID
- `DERIV_REDIRECT_URI` = `https://atlanticwaves-8kf7.onrender.com/oauth/callback`

## Verification URLs
After deployment, these should work:
- `https://atlanticwaves-8kf7.onrender.com/health` → JSON `{ "ok": true, ... }`
- `https://atlanticwaves-8kf7.onrender.com/oauth/callback` → it should NOT be a Render 404; without an OAuth state it may say `Invalid or expired OAuth state.`

Do not put OAuth access tokens, passwords, PATs, or client secrets into the browser or chat.
