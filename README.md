# Landing page

`index.html` is V2, written for US manufacturers that quote from a web RFQ form (machine shops, fabricators, molders, contract manufacturers, machinery makers). `v1.html` keeps the original general small-business version, live at `/v1` and marked noindex so it doesn't compete with the home page in search.

`index.html` is the complete page in one file: HTML with inline styles, no build step and no JavaScript. Fonts load from Google Fonts (Bricolage Grotesque, IBM Plex Sans, IBM Plex Mono) with system fallbacks.

## Replace these placeholders

Search the file for each bracketed item:

- `[Your Brand]`: nav, footer and page title
- `[your@email.com]`: footer link (appears twice: the link and its text)
- `[X]`: how many business days until you send the free scan
- `[FOUNDING PRICE]`: founding-client offer
- `[PLATFORMS YOU SUPPORT]`: FAQ answer, for example "Shopify, WooCommerce and BigCommerce"
- `[Product A]`, `[Product B]`: example insights in the leak-free store section
- `[YOUR_FORM_ENDPOINT]`: where scan requests are sent (see below)

The dollar figures, percentages and order counts in the hero card and previews are illustrative. Swap them for real numbers once you have client results.

## Connect the scan form

The form posts two fields, `store_url` and `email`. The simplest option is a form service such as Formspree, Basin or Tally: create a form there, then replace `[YOUR_FORM_ENDPOINT]` with the URL they give you. If you build the page in Webflow, Framer or similar, use that tool's native form block instead and keep the same two fields.

## Colours

- Ink: `#12151A`
- Background: `#F5F6F3`
- Accent (buttons, labels): `#2B3FCC`
- Highlight (marker effect, badges): `#F2DC4B`

To change the accent or highlight, find and replace the hex value throughout the file.

## Hosting

Any static host works: Netlify, Vercel, Cloudflare Pages or GitHub Pages. Upload `index.html` as the site's home page.

## Deploying

This repo is connected to Vercel. Every push to `main` redeploys the site automatically, so editing `index.html` and pushing is all it takes to update it. No build command or framework is needed; Vercel serves `index.html` as a static file.
