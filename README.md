# PAISS Consulting — Site Setup

Static multi-page website. No build step, no dependencies.

## Files

```
paiss-site/
├── index.html                          ← homepage
├── pmo.html                            ← Project Management Office
├── cio-office.html                     ← CIO Office
├── post-merger-integration.html        ← PMI & Carve-out
├── project-program-management.html     ← Project & Program Management
├── styles.css                          ← shared styles (edit here, all pages update)
└── README.md
```

## Step 1 — Deploy to Netlify (~3 min)

1. Go to https://app.netlify.com/drop (sign up with email or GitHub when prompted — free tier is fine)
2. Drag the entire `paiss-site` folder onto the page
3. Your site is live at something like `melodious-frog-12345.netlify.app`
4. Click **Site configuration → Change site name** and set it to `paissconsulting.netlify.app`

## Step 2 — Activate the contact form (~2 min)

The site uses **Netlify Forms**, which means:
- ✅ Your email address is **not visible anywhere** on the site or in the page source
- ✅ Submissions arrive in your Netlify dashboard and as email notifications
- ✅ Built-in spam filtering (Akismet + honeypot field)
- ✅ Free tier covers 100 submissions/month — more than enough

To turn it on:

1. In your Netlify site dashboard, go to **Forms**. You should see a form called "contact" detected automatically (Netlify finds it from the `data-netlify="true"` attribute in the HTML).
2. Click **Settings & usage → Form notifications → Add notification → Email notification**
3. Enter the email where you want enquiries delivered (e.g. `elougordon@gmail.com`)
4. Save.

That email address now lives only in Netlify's settings — **it is not in your website's HTML, not in the form action, not visible to anyone who views your page source.**

Test it: submit a message through your live site's contact form. The submission appears under **Forms → contact** in Netlify, and an email lands in the inbox you configured.

## Optional: custom domain

If you buy `paissconsulting.com` (or `.co.il`) for ~$10–15/yr, Netlify can point it at your site under **Domain configuration**. Domain and SSL certificate stay free thereafter.

## Editing later

- **Text on a page** → open that HTML file in any editor (VS Code is free), edit, save.
- **Colors, fonts, spacing globally** → edit `styles.css`. All 5 pages update at once.
- **Redeploy** → drag the folder back onto Netlify. Version history is kept.

## Design notes

- **Font:** Inter throughout — clean, contemporary sans-serif, same family used on the Lovable reference site
- **2×2 service grid:** four practice areas as clickable cards on the homepage, each linking to a dedicated page
- **No personal email** anywhere in the HTML — all contact funnels through the Netlify form
- **Color palette** is in `:root` at the top of `styles.css` — change one variable to shift the whole site
