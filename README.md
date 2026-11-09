# EveryToolHub

A static, browser-first utility website starter. It can be hosted on GitHub Pages or Cloudflare Pages without a server.

## Included working tools
- PDF merger
- PDF page extractor
- Image-to-PDF converter
- PDF re-save using PDF object streams (not a guaranteed size compressor)
- Image compressor (JPG/WebP/PNG)
- Image resizer
- QR code generator
- Word and character counter
- Text case converter
- Age calculator
- Percentage calculator
- Random name picker

## Run locally
Because this is a static site, you can open `index.html` directly. For a local server, run:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Publish on GitHub Pages
1. Create a GitHub account and a new **public** repository, for example `everytoolhub`.
2. Upload all files and folders in this project to the repository root (not the ZIP file itself).
3. Open **Settings → Pages**.
4. Under Build and deployment, select **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. Your public URL will be shown in the Pages settings, typically `https://YOUR-USERNAME.github.io/everytoolhub/`.

For a Cloudflare Pages deployment, import the GitHub repository and use the static site/root directory with no build command and no output directory beyond the repository root.

## Before public launch
- Replace the placeholder contact information in `contact.html` and `privacy.html` with a real support contact.
- Review the privacy policy and terms for your actual analytics, advertising, jurisdiction and business model.
- Test all tools in current Chrome, Firefox, Safari and mobile browsers with sample files.
- Test accessibility, file-size limits and error cases.
- Add a custom domain if desired.
- Add Google Search Console and submit a sitemap. This starter does not include a generated sitemap yet; create one using your final canonical domain before SEO launch.
- Add analytics and advertising only after updating the privacy disclosures and consent mechanisms required for your audience and applicable laws.

## Technical notes
- PDF and QR libraries are loaded from public CDNs (pdf-lib and QRCode.js). The site needs an internet connection for those tools to load.
- PDF/image files are handled in the browser by the client-side code. No EveryToolHub upload endpoint exists in this starter.
- PDF re-save may not reduce file size. True PDF compression can require image downsampling and more advanced optimization.
- PNG output is lossless and may be larger than the source. JPG/WebP are usually more suitable for lossy compression.
- This starter is not a legal or tax compliance package and does not guarantee ad-network approval or search ranking.
