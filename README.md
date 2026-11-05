# Album Tracker
A React app to search albums, preview tracks, keep a personal listening log
(status, rating, notes) and get LLM-powered recommendations based on your
saved albums and ratings.
![Screenshot](docs/screenshot.png)
**Live:** https://album-tracker-weld.vercel.app/
## Features- Search albums and artists (iTunes Search API)- Album page with 30-second previews and a persistent mini player- Collection with status, 1-5 star rating, notes, filter and sort (saved in your browser)- Optional full-album playback through Deezer's embedded player- Recommendations from Google Gemini based on your saved albums and ratings
## Tech stack
React, Vite, Context API, iTunes API, Deezer API, Gemini API, Vercel serverless functions
## Run locally
git clone https://github.com/chervivillaflor-cell/album-tracker.git
cd album-tracker
npm install
# create .env.local containing: GEMINI_API_KEY=your-key
npm run dev
## Limitations- Previews are 30 seconds (all the iTunes API provides)- The collection is stored only in this browser (localStorage)- Deezer needs you to be logged in (and a suitable plan) for full tracks
## Privacy
The Recommendations feature sends your saved albums' titles, artists, ratings and
statuses to Google's Gemini API. Your notes are not sent.
## Disclaimer
Learning project. Not affiliated with Apple, Spotify, Deezer or Google. Music data,
artwork and audio belong to their owners.
