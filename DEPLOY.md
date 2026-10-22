# Deploying to Cloudflare (free)

Static Vite site: build command `npm run build`, output directory `dist`. No env vars, no backend.
Single page with anchor links, so no SPA rewrite rules are needed.

## Option A — Cloudflare Pages via CLI
    npm install && npm run build
    npx wrangler login
    npx wrangler pages deploy dist --project-name agro-farm-demo
Result: https://agro-farm-demo.pages.dev

## Option B — Workers static assets (wrangler.jsonc included)
    npm run build && npx wrangler login && npx wrangler deploy
Result: https://agro-farm-demo.<account>.workers.dev

## Remove afterwards
Dashboard → Workers & Pages → project → Settings → Delete.

## Still to fill in
Phone, email, farm name, region, map coordinates (see index.html: contact section, location section).
