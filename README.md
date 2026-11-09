# Scrap-Claw Goblin v2.0

A mobile-friendly pixel-art browser game with pendulum-style claw physics, hazards, multiple biomes, upgrades, claw gacha, goblin workers, offline earnings, museum artifacts, prestige, local saves, and optional Supabase cloud saves.

## Run locally
Open `index.html` in a modern browser, or use VS Code + Live Server.

## Controls
- Desktop: Left / Right arrows to steer; Space to drop or haul.
- Mobile: Tap LEFT / RIGHT and DROP / HAUL.
- Sell your haul to convert collected scrap into gold.

## Local save
Progress automatically saves in browser `localStorage`. Local saves are device/browser-specific. Offline worker earnings are calculated when you return (up to 8 hours).

## Optional Supabase cloud save
1. Create a Supabase project.
2. In SQL Editor, run `supabase-schema.sql`.
3. Open Project Settings → API (or API Keys) and copy the Project URL and public anon/publishable key.
4. Put them in `config.js` as `url` and `anonKey`.
5. Publish all project files together. Open the game, expand Cloud Save, create an account or sign in, then choose Sync Cloud Save Now.

The browser must only contain the public anon/publishable key. NEVER expose a `service_role` or secret key. Row Level Security policies in the SQL file restrict each player's save to their own authenticated user ID.

## Publish on GitHub Pages
1. Create a GitHub repository.
2. Upload `index.html`, `config.js`, `supabase-schema.sql`, and `README.md` to the repository root.
3. Go to Settings → Pages.
4. Choose Deploy from a branch → `main` → `/(root)` → Save.
5. Wait for GitHub Pages to provide the public URL.


## Important prototype notes
- The game is a prototype. Its physics and hazards are lightweight custom Canvas mechanics, not a full rigid-body simulation.
- Have fun :p. (create by Schnitzel)