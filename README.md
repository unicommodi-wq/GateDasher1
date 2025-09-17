# Airport Gate Delivery (Netlify + Square)

A minimal Next.js app that lets passengers scan a QR, choose items, and pay via **Square-hosted checkout**. Your runner walks the order to the gate.

## Deploy on Netlify (no Git required)
1. Zip this folder (or use the ZIP provided).
2. Go to https://app.netlify.com/drop and drag the ZIP.
3. After deploy, open **Site settings → Build & deploy → Environment → Edit variables** and add:
   - `SQUARE_ACCESS_TOKEN` — your Square token (Sandbox or Production)
   - `SQUARE_LOCATION_ID` — your location ID
   - `SQUARE_ENVIRONMENT` — `sandbox` or `production`
   - `SQUARE_API_VERSION` — e.g. `2024-06-20`
4. Trigger a redeploy (Deploys → Trigger deploy → Clear cache and deploy site).

## Test
Open your site with optional query params: `/?airport=DTW&gate=A12` and place a test order using the Square sandbox card `4111 1111 1111 1111`.

> **Security:** never commit tokens. Keep them only in environment variables. Rotate tokens before going live.
