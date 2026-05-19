# Teaching Atlas, CentralAZ

A static site containing three versions of the Teaching Atlas report:

- **V1**: Retrospective audit (262 sermons, 5 years)
- **V2**: Audit + national peer landscape (15 churches)
- **V3**: Audit + Phoenix-metro peer landscape (9 churches) + proposed 2026-27 calendar

## File structure

```
/
├── index.html              # Landing page linking to all three versions
├── atlas-v1/index.html     # V1 dashboard
├── atlas-v2/index.html     # V2 dashboard
├── atlas-v3/index.html     # V3 dashboard
├── fonts/                  # Aeonik Pro font files go here
└── README.md
```

## Adding Aeonik Pro

The site references Aeonik Pro as its primary font with Fraunces/Inter Tight as fallbacks. To activate Aeonik Pro:

1. Get your Aeonik Pro `.woff2` files from CoType (or convert from `.otf` using [transfonter.org](https://transfonter.org/)).
2. Rename them to match these exact filenames and drop them in the `fonts/` folder:
   - `AeonikPro-Regular.woff2`
   - `AeonikPro-Medium.woff2`
   - `AeonikPro-Bold.woff2`
   - `AeonikPro-RegularItalic.woff2`
   - `AeonikPro-MediumItalic.woff2` (used only in V1/V2/V3, not the landing page)

If filenames differ, edit the `@font-face` blocks at the top of each `.html` file's `<style>` section.

If the font files aren't present, the site falls back to Fraunces (headlines) and Inter Tight (body), which is what it currently renders as.

## Deploying to GitHub Pages

1. Create a new repository (e.g. `teaching-atlas`) on github.com. Make it public if you want anyone to be able to view it; make it private if you want only you and collaborators.
2. Upload the entire contents of this folder to the repo root. (Click "Add file" → "Upload files" → drag the whole folder).
3. Repo Settings → Pages → "Source" → Deploy from a branch → `main` / root → Save.
4. Wait 1-2 minutes. The site will be live at `https://<your-username>.github.io/teaching-atlas/`.

## Custom domain (optional)

If you want this on a custom subdomain (e.g. `atlas.centralaz.com`):

1. In GitHub Pages settings, add the custom domain.
2. In your DNS provider, add a `CNAME` record pointing the subdomain to `<your-username>.github.io`.
3. GitHub Pages will provision an SSL certificate within 24 hours.

## Updating

When new versions of the Atlas are produced, replace the relevant `atlas-vX/index.html` file. The landing page (`index.html`) only needs editing if the V's metadata changes.

## License & access

This is intended for internal use by the Central Adult Services Message Planning team. If you make the repo public, the URL is publicly accessible by anyone who has the link.
