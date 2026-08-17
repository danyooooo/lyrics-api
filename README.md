# Lyrics API

A fast, lightweight serverless API built on Cloudflare Workers for searching songs, retrieving plain & synchronized (LRC) lyrics, translations, top charts, and music metadata.

It features automated guest token management with in-memory caching and high-concurrency mutex deduplication for reliable, sub-second responses.

---

## Base URL

```text
https://lyrics1.api-danidev.workers.dev
https://lyrics2.api-danidev.workers.dev
https://lyrics3.api-danidev.workers.dev
```

> **Note:** Visiting the Base URL directly opens the documentation with live request testers and parameter tables.

---

## Available Endpoints

| Endpoint | Method | Description | Example |
|---|---|---|---|
| `/search` | `GET` | Search tracks, artists, or albums | `/search?query=24k%20magic&country=MY&limit=5` |
| `/lyrics` | `GET` | Get full lyrics & synchronized LRC timestamps | `/lyrics?slug=bruno-mars-24k-magic` |
| `/metadata` | `GET` | Get artist, album, genre, or track metadata | `/metadata?reqtype=artistdata&artistid=slug:bruno-mars` |
| `/charts` | `GET` | Get top charting tracks or artists | `/charts?reqtype=trackcharts&country=MY&limit=10` |
| `/translation` | `GET` | Get translated lyrics | `/translation?slug=bruno-mars-24k-magic&lang=es` |
| `/lyriciq` | `GET` | Sentiment, emotion, and content filter analysis | `/lyriciq?slug=eminem-rap-god` |