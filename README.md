# SmartKitchenDocs.com

Marketing site for **Smart Kitchen Docs** — manufacturer equipment documentation for
commercial kitchens. Static HTML, no build step, deployed to GitHub Pages.

Sibling site to [smartevguides.com](https://www.smartevguides.com); same structural
rhythm, its own visual identity (data-plate motif, porcelain/graphite palette,
gas-flame blue accent).

## Files

| File | What it is |
|---|---|
| `index.html` | The landing page. All CSS is inline in a single `<style>` block. |
| `doc.css` | Shared styling for the secondary pages only. |
| `privacy.html` | Privacy policy. **Draft — review before DNS goes live.** |
| `support.html` | Support / FAQ page. |
| `favicon.svg` | Site icon (data plate mark). |
| `CNAME` | Custom domain for GitHub Pages. |
| `robots.txt`, `sitemap.xml` | Search indexing. |
| `.nojekyll` | Stops Pages running Jekyll over the files. |

No dependencies, no build. Edit the HTML and push.

## Local preview

```bash
py -3.12 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to GitHub Pages

1. Create the repo and push:

   ```bash
   git add -A
   git commit -m "Smart Kitchen Docs marketing site"
   gh repo create SmartKitchenDocs --private --source=. --push
   ```

2. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**.

3. **Settings → Pages → Custom domain:** `smartkitchendocs.com`, then tick
   *Enforce HTTPS* once the certificate is issued (usually a few minutes).

4. DNS at your registrar — apex `A` records to GitHub Pages, plus `www` as a CNAME:

   ```
   A     @      185.199.108.153
   A     @      185.199.109.153
   A     @      185.199.110.153
   A     @      185.199.111.153
   CNAME www    <your-github-username>.github.io
   ```

   The `CNAME` file in this repo is set to the apex (`smartkitchendocs.com`), so
   `www` will redirect to it. Swap them if you'd rather `www` be canonical —
   if you do, update `CNAME`, the `<link rel="canonical">` tags, `sitemap.xml`
   and `robots.txt` to match.

## Before it goes live

- [ ] Review `privacy.html` — the retention window and processor list are drafted
      from how the app actually behaves, but they're a draft.
- [ ] Confirm the stat strip in `index.html` (43 units / 61 manuals / 2,200+ pages /
      100% cited). These came from `catalog/equipment.json`,
      `corpus/corpus_manifest.json` and the developer brief; refresh them as the
      corpus grows.
- [ ] Add an Open Graph image (`og:image`) once there are app screenshots worth
      showing — currently the cards fall back to `summary` with no image.
- [ ] Swap the illustrative hero answer and the three transcript cards for real
      captures from the app when the pilot has some.

## The maintenance section

`#maintenance` describes shipped behaviour: intervals extracted from each
manual with page citations, review-and-accept, Overdue / Today / This week
bucketing, mark-done rescheduling, and local phone notifications.

The `.next` strip at the bottom of that section ("Not there yet") names two
things that are **not built**: calendar sync (Google Calendar / Outlook) and a
completion log for health-inspection and NFPA 96 records. Both are W3 items in
Ryan's brief. **When either ships, move it out of that strip and into the
numbered flow above** — leaving it there once it's real undersells the product,
and leaving it in the flow before it's real is the one thing this site's whole
argument can't afford.

The task card is illustrative, built from real units in the pilot bakery
(Hobart HL600, True T-49F, Revent 626U) with plausible intervals. Swap in a
real screenshot when there's one worth showing.

## Content notes

- Every email link points at `dylan@smartevguides.com`.
- Entity is **DAG LLC** throughout.
- The app is pilot-stage, so there are deliberately no App Store / Google Play
  badges. The single CTA everywhere is *Book a walkthrough*. When the listings
  are live, the closing section and the nav button are the two places to add them.
