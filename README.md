# IT STRATEGIX static site – Deploy on Netlify

## Deploy

1. **Create a new site** on <https://app.netlify.com/> ("Add new site" → "Import an existing project").
2. Point Netlify to this folder (drag‑and‑drop or connect the Git repository).
3. Netlify will auto‑detect a static site. No build command needed, publish directory is `./`.

## Netlify Form

The contact form in `index.html` is already configured with:

```html
<form name="contact" method="POST" data-netlify="true" …>
```

Submissions will appear in **Site settings → Forms**.

## Custom domain

1. Buy `itstrategix.com` (or the domain of your choice) from a registrar (Namecheap, OVH, IONOS…).
2. In Netlify dashboard → **Domain settings** → **Add custom domain** → enter `www.itstrategix.com`.
3. Netlify shows DNS records:
   - **CNAME** `www` → `your-site-id.netlify.app`
   - Or **A records** if you prefer apex (`itstrategix.com`).
4. Go to your registrar’s DNS panel, add the records exactly as provided by Netlify.
5. Wait for DNS propagation (few minutes to 24 h).
6. Back in Netlify, click **Verify**. When verified, enable HTTPS (Let’s Encrypt) – one click.

That's it! Your site is live on `https://www.itstrategix.com` with SSL.
