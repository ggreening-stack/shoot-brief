# Shoot Brief — Gabriel Greening Photography

Client intake page: https://book.ggreeningphotography.com (also https://ggreening-stack.github.io/shoot-brief/)

## How it works
- Static page, hosted on GitHub Pages. Every push to `main` redeploys automatically in about a minute (see `.github/workflows/pages.yml`).
- Submissions post to Formspree (`FORM_ENDPOINT` near the top of the script in `index.html`) and arrive by email at inquiries@ggreeningphotography.com with reply-to set to the client.
- Custom domain is set in the repo's Settings → Pages; DNS is a CNAME at Namecheap: `book` → `ggreening-stack.github.io`.

## Updating sample photos
1. Export web-size JPGs (about 1600px on the long edge, under 400 KB) into `samples/`.
2. List them in the `SAMPLES` block in `index.html` by shoot type, e.g.
   `product:[{file:"latte-art.jpg", caption:"Pour & latte art", exif:"85mm · f/2.8"}]`
3. Commit and push. Types with no photos keep the color-study placeholders.

## Changing copy, pricing or the email
Everything is in `index.html`: `RATES` (starting prices shown to individual clients), `BUDGETS`, `USAGE`, and the email address appears twice in the markup.
