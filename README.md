# Ramesh Marella Website

Static executive profile website for `https://rameshmarella.com/`, built from `Ramesh_Marella_Enterpise_Cloud_and_SRE_Architect.docx`.

## Files

- `index.html` - site content and SEO metadata
- `styles.css` - responsive executive-grade visual system
- `script.js` - header state and dynamic footer year
- `assets/enterprise-cloud-command-center.png` - generated hero visual
- `assets/ramesh-marella-profile-900.png` - profile photo displayed on the webpage
- `downloads/ramesh-marella-one-page-resume.pdf` - one-page resume PDF download
- `downloads/ramesh-marella-detailed-resume.pdf` - detailed resume PDF download
- `CNAME` - GitHub Pages custom domain mapping
- `netlify.toml` - Netlify static hosting configuration
- `vercel.json` - Vercel headers and apex-to-www redirect

## Local Preview

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Domain Hosting

This folder is deployed to Vercel under the `infinityinfosystems` scope.

- Production URL: `https://personal-website-app-rho.vercel.app`
- Vercel project: `personal-website-app`
- Production custom domain: `rameshmarella.com`
- Secondary custom domain: `www.rameshmarella.com` redirects to `rameshmarella.com`

Vercel has added `rameshmarella.com` and `www.rameshmarella.com` to the project, but DNS still needs to point to Vercel. Public DNS currently points to GitHub Pages:

- `rameshmarella.com` -> `185.199.108.153`
- `www.rameshmarella.com` -> `rammar876.github.io`

In Cloudflare DNS, remove or replace the GitHub Pages records and set:

```text
Type: A
Name: @
Value: 76.76.21.21

Type: A
Name: www
Value: 76.76.21.21
```

Set the proxy status to DNS only while Vercel verifies the domain. Vercel will verify the domain after the DNS records propagate.
