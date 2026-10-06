# GEO Visibility Tracker

A single-file app (`index.html`) for tracking a brand's visibility in AI search (Google AI Overviews, AI Mode, ChatGPT, Perplexity, Copilot, Gemini, Claude) and auditing GEO readiness per client.

## Features
- **Dashboard:** mention rate, citation rate, average position, share of voice, monthly trend, engine breakdown, prompt × engine heatmap, competitor mentions.
- **Prompts & checks:** a fixed prompt library per client (with language and location) and a log of what each engine answered: mentioned, cited URL, position, sentiment, accuracy and competitors.
- **Readiness checklist:** indexability, AI crawler access, content, entity/schema, local listings, Bing and measurement. Every item links to its primary source.
- Multi-client, light/dark mode, print/PDF report, CSV export, and JSON backup/restore.

## Ubersuggest import
**Data → Import Ubersuggest pull…** merges a `geo-tracker-ubersuggest/v1` JSON file. Claude generates this file from the Ubersuggest MCP's AI Search Visibility data.
- Clients are matched by domain, prompts by text, and checks by prompt + engine + run date. Re-importing updates rows instead of duplicating them, and manual checks are never touched.
- Ubersuggest covers ChatGPT, Gemini and Google AI Overviews. It reports mentions, rank, sentiment and competing brands, but not cited URLs, so those checks show "not reported" and are left out of the citation rate.
- Pull files contain client data. Keep them out of this public repo.

## Data
Everything is stored in the browser's `localStorage`. There's no backend, no API keys, and no calls to AI engines. Back up with **Data → Back up all data (JSON)**.
The "Demo Coffee Co." client is fictional sample data.

## Deploy
Turn on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**.
