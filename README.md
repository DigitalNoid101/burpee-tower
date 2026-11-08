# Burpee Tower

A single-file HTML5 canvas tower climber. Do burpees (Down, Down, Up, Up) to launch higher; Space is a quick jump.
On a phone: swipe down/down/up/up, hold the left or right side of the screen in mid-air to move, tap for a jump.

## Run locally
Open `public/index.html` in a browser, or run `npx wrangler dev`.

## Deploy (Cloudflare Workers, static assets)
`npx wrangler deploy` uses `wrangler.jsonc` to serve everything in `public/`.
Or connect this repo under Workers & Pages > Create > Import a repository (no build command; deploy command `npx wrangler deploy`).

## Notes
- The leaderboard only works inside Claude (it uses the artifact database and user capabilities). Anywhere else the game plays normally and the leaderboard panel stays hidden. Replacing it with Supabase or Cloudflare D1 is the planned next step.
- `GAME_URL` in `public/index.html` is the link put in the "Copy result" text. Change it to the live site address.
