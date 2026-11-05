# Album Tracker

A React app to search albums, preview tracks, keep a personal listening log
(status, rating, notes) and get LLM-powered recommendations based on your
saved albums and ratings.

## Run locally
Requires Node 20.19+ (22 LTS recommended).

    npm install
    cp .env.local.example .env.local     # then paste your Gemini key inside
    npm run dev

Open http://localhost:5173. The `api/` functions run through a dev plugin in `vite.config.js`.
Restart `npm run dev` after changing `.env.local` or `vite.config.js`.

## Deploy
Push to GitHub, import the repo in Vercel, add `GEMINI_API_KEY` under
Settings > Environment Variables (Production, Preview, Development), then redeploy.

## Limitations
- Previews are 30 seconds (all the iTunes API provides)
- The collection is stored only in your browser (localStorage)
- Deezer needs a login (and a suitable plan) for full tracks

## Privacy
Recommendations send your saved albums' titles, artists, ratings and statuses to
Google's Gemini API. Your notes are not sent.

## Disclaimer
Learning project. Not affiliated with Apple, Spotify, Deezer or Google. Music data,
artwork and audio belong to their owners.
