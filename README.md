[README.md](https://github.com/user-attachments/files/32175538/README.md)
# VoteFile — Overstrand

A deep-dive research profile of Overstrand Municipality, part of the **VoteFile** project — a South African local & national elections research site. Each municipality page pulls together official reports, council records, resident survey data, and news coverage into one transparent, sourced profile so residents can see what their council and ward councillors have actually delivered.

## Live site

Hosted on GitHub Pages: `https://<your-username>.github.io/<repo-name>/`

## What's in this page

- **Performance dashboard** — headline satisfaction scores and category breakdowns from the municipality's 2026 Customer Satisfaction Survey
- **Ward-by-ward profiles** — per-ward findings, flagged issues, and service delivery notes across all 14 wards
- **Capital budget & delivery tracking** — SDBIP line items, grant funding (national vs. municipal sphere), and spend targets
- **Findings & sourcing** — every claim is labeled *confirmed*, *reported*, *interpretation*, *unverified*, or *open question*, so readers can judge how solid the ground is
- **Reader survey widgets** — resident rating/feedback forms that submit to Google Forms and read results back from a published Google Sheet (fully client-side, no backend required)

## Tech stack

Single static `index.html` file — HTML, CSS, and vanilla JS, no build step or server required. This is why it works as-is on GitHub Pages:

- Survey submissions POST directly to a Google Form's response endpoint (public, unauthenticated by design — no secrets exposed)
- Survey results are read by fetching a published Google Sheet as CSV
- Optional companion file `votefile-overstrand-import.json` (if present) is fetched for imported council data — upload it alongside `index.html` if you have it, otherwise that feature just won't load data

## Running locally

Just open `index.html` in a browser — no install or build needed.

## Deploying

1. Upload `index.html` (and `votefile-overstrand-import.json` if you have it) to this repo
2. In repo Settings → Pages, set source to "Deploy from a branch" → `main` / `/ (root)`
3. GitHub publishes the site at the URL shown in Settings → Pages within a couple of minutes

## Roadmap

- Additional municipality profiles: Breede Valley, Theewaterskloof or Cape Town (comparison), Overberg District Municipality
- Ward councillor profiles with per-party performance tracking (issues raised/resolved/outstanding)
- Monthly council-minutes import with AI-assisted draft extraction of issues, motions, promises, and attendance
- Compare feature across municipalities on shared metrics (clean audits, service delivery, scandals)

## Editing on the go

This is a single flat HTML file, so small edits (copy fixes, stat updates) can be made directly via the GitHub Mobile app or github.com's web editor. Larger changes are easier done with a code editor on a laptop given the file's size.
