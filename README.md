# PAISS Consulting — Site Setup

Static multi-page website. No build step, no dependencies — just open and edit HTML.

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

## Step 1 — Activate the contact form (one click, ~30 seconds)

The contact form is already wired to send to **elougordon@gmail.com** via Formsubmit.co (free, no signup, unlimited submissions).

The **first time** someone submits the form, Formsubmit will send a one-time confirmation email to `elougordon@gmail.com` — click the activation link inside, and every subsequent submission lands in the inbox.

To send the activation email immediately (without waiting for a real visitor), just fill out and submit the contact form yourself once after the site is live.

To change the destination email later, open `index.html` and edit this line:
```html
<form action="https://formsubmit.co/elougordon@gmail.com" method="POST">

## Step 2 — Deploy to Netlify (~3 min)

1. Go to https://app.netlify.com/drop
2. Drag the entire `paiss-site` folder onto the page
3. Your site is live at something like `melodious-frog-12345.netlify.app`
4. Click **Site settings → Change site name** to set it to `paissconsulting.netlify.app`

That's it — the site is live with HTTPS. All four practice pages, navigation, and the contact form work out of the box.

### Optional: custom domain

If you buy `paissconsulting.com` (or `.co.il`) for ~$10–15/yr, Netlify can point it at your site under "Domain settings." Domain and certificate stay free thereafter.

## Step 3 — Editing content later

- **Edit text on a page** → open that HTML file in any editor, change the text, save.
- **Change colours, fonts, or spacing globally** → edit `styles.css`. All five pages update at once.
- **Redeploy** → drag the folder back onto Netlify. Version history is kept so you can roll back.

## What to swap before going live

- [ ] Confirm "Based in: Tel Aviv" — add Stockholm if you want to signal Nordic presence
- [ ] Re-read the leadership bio on `index.html`; tweak firm names or tone

## Structure notes

- Each practice page follows the same template: hero → overview → engagements → approach → CTA → footer
- Top nav links from any practice page jump back to the matching section on the homepage
- Service cards on the homepage are full-link rows with a hover effect — feels familiar to anyone who has used a McKinsey, BCG, or Bain site
- The shared `styles.css` is the single source of truth for design — change a colour variable at the top and the whole site shifts
