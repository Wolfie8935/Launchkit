# Deploying the LaunchKit Pro site to Vercel (5 minutes)

## Before you deploy — 3 edits in index.html

Search and replace these placeholders:

1. `https://YOUR_GUMROAD_PRO_LINK` — your Gumroad/Lemon Squeezy product URL for Pro (appears twice: pricing card + you may also want the two "Get LaunchKit Pro" header/hero buttons to point there instead of #pricing)
2. `https://YOUR_GUMROAD_STARTER_LINK` — your Starter product URL
3. `YOUR_EMAIL_HERE` in the footer — your support email (use a dedicated one, e.g. launchkit.support@gmail.com, not your personal inbox)

## Deploy — Option A (fastest, no git)

1. Go to https://vercel.com → sign in with your GitHub (Wolfie8935)
2. "Add New → Project" → drag and drop this folder
3. Done. You get launchkit-pro.vercel.app (rename the project for a clean URL)

## Deploy — Option B (recommended: updates via git push)

```bash
cd launchkit-site
git init && git add . && git commit -m "LaunchKit Pro site"
gh repo create launchkit-site --private --push   # or create on github.com and push
```
Then Vercel → Add New Project → import the repo → deploy. Every future `git push` redeploys automatically.

## After deploy

- Buy a domain if you want ($10/yr, e.g. launchkitpro.dev) and add it in Vercel → Domains. A real domain meaningfully improves trust at a $399 price point.
- Put the live URL in your Gumroad listing as "Live demo + full API reference".
- Add the URL to your X bio and the GitHub demo repo README.

## What this site is

A zero-build static page: one index.html, no framework, no dependencies, nothing to break. The terminal animation, API explorer (19 real endpoints with actual response JSON from the product), comparison table, and pricing are all self-contained.
