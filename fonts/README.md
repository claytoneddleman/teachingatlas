# Aeonik Pro font files go here

Drop your `.woff2` font files in this folder. Expected filenames:

- `AeonikPro-Regular.woff2`
- `AeonikPro-Medium.woff2`
- `AeonikPro-Bold.woff2`
- `AeonikPro-RegularItalic.woff2`
- `AeonikPro-MediumItalic.woff2`

If your file names differ, edit the `@font-face` declarations at the top of:

- `../index.html` (landing page)
- `../atlas-v1/index.html`
- `../atlas-v2/index.html`
- `../atlas-v3/index.html`

Until these font files are present, the site falls back to Fraunces (headlines) and Inter Tight (body) from Google Fonts.

To convert `.otf` or `.ttf` to `.woff2`, use [transfonter.org](https://transfonter.org/).
