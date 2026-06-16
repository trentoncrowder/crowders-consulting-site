# Crowder's Consulting LLC — Website

Single-page static site. Two files: `index.html` and `styles.css`. No build step, no framework, no dependencies. Fonts load from Google Fonts.

## Preview locally
Open `index.html` in any browser, or from this folder run:
```
python3 -m http.server 8000
```
Then visit http://localhost:8000

## Deploy (free, pick one)

### Cloudflare Pages
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard > Workers & Pages > Create > Pages > connect the repo.
3. Build settings: framework preset "None", build command blank, output directory `/`.
4. Deploy. You get a `*.pages.dev` URL immediately.
5. Custom domain: Pages project > Custom domains > add `crowdersconsulting.com`. If the domain is registered at Cloudflare, DNS is automatic. If elsewhere, add the CNAME record Cloudflare shows you.

### Netlify
1. Push to GitHub (or drag this folder into the Netlify dashboard for instant deploy).
2. Site settings > Domain management > add `crowdersconsulting.com`.
3. Point your registrar's DNS at Netlify's nameservers, or add the records Netlify lists.

DNS changes can take from minutes to a few hours to propagate.

## Work email: consulting@crowdersconsulting.com
You need send AND receive (so application replies come from the domain). Free/cheap options:

- **Zoho Mail** — free tier supports one custom domain with full send/receive. Add the domain, verify with a TXT record, set MX records. Best free option.
- **Google Workspace** — ~$7/user/month, full Gmail on the domain. Pay for polish.

Avoid receive-only forwarding (e.g. plain Cloudflare Email Routing) as your application address, because replies would not come from the domain.

## After it's live
- Test on desktop and phone.
- Update the email address on both resume versions and LinkedIn to consulting@crowdersconsulting.com.
- Optional: add a LinkedIn link in the contact section once the profile is aligned.

## Editing copy later
All text is in `index.html`. The "How I work" section is optional — delete the whole `<section class="approach">` block if it reads as filler. Do not add free-floating metrics (vessel counts, ticket numbers); those belong on the resume where they're tied to a named role.
