# Heuristic Audit Tool

AI-powered UX audit tool based on Nielsen's 10 Usability Heuristics.

Upload screenshots of any site, get a full evaluation with severity ratings and redesign recommendations, then export the report as a PDF.

## Stack

- Single-file static frontend (`index.html`) — vanilla JS, no build step.
- Vercel serverless function (`api/audit.js`) that proxies requests to Anthropic's Claude API, keeping the API key server-side.

## Deploy

This project deploys automatically to Vercel on every push to `main`.

The serverless function reads `ANTHROPIC_API_KEY` from Vercel's environment variables.

## Local development

Open `index.html` in a browser to see the UI, but note the audit endpoint (`/api/audit`) only works on Vercel (or via `vercel dev`).
