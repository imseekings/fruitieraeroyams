# Climate Mosaic World Map

A single-page, no-build web app: multi-model climate mosaic on a world map, decadal
projections, infrastructure impacts (roadways, power, built environment) and
year-by-year GIF export.

**Data note:** the model fields and "current climate" are illustrative, generated in the
browser from idealized patterns. They are not real CMIP6 output. Swap in real gridded
data before relying on any number.

## Run locally
    python3 -m http.server 8000 --directory public
    # open http://localhost:8000

## Deploy on Render (static site)
1. Put this folder in a GitHub/GitLab repo.
2. In Render: **New > Blueprint**, pick the repo, and apply. `render.yaml` sets it up.
   (Manual alternative: **New > Static Site**, Build Command `echo "Nothing to build"`,
   Publish Directory `public`.)
3. Every push to the main branch redeploys automatically.

Check Render's current docs and pricing for static sites and custom domains.

## Files
- `public/index.html`: the whole app (HTML, CSS, JS in one file, no dependencies)
- `render.yaml`: Render Blueprint for a static site
