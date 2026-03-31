# Synthwork

Business automation consulting site for Singapore SMEs — [synthwork.app](https://synthwork.app)

## Local Development

### Prerequisites

- Ruby 3.x
- Bundler gem: `gem install bundler`

### Setup

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

## Deployment

This site deploys automatically to GitHub Pages on push to `main`. Ensure the repository is configured to deploy from the `main` branch root in **Settings > Pages**.

## CSP Header (Cloudflare)

This site produces CSP-compliant output (no inline styles, no inline scripts). To enforce the policy, add a **Response Header Transform Rule** in Cloudflare:

1. Go to your domain in Cloudflare > **Rules > Transform Rules > Modify Response Header**
2. Create a rule matching `synthwork.app/*`
3. Add header:

```
Content-Security-Policy: default-src 'self'; style-src 'self' https://fonts.googleapis.com; font-src 'self' https://fonts.gstatic.com; img-src 'self'; frame-ancestors 'none';
```

## Sister Site

SEO-first web builds for Singapore businesses: [consultant.ebiya.sg](https://consultant.ebiya.sg)
