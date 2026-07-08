# Saylor & The Captains — Website

A full static band website with Decap CMS for easy content management.
Band members can update shows, quotes, and text through a simple web interface — no coding required.

---

## File Structure

```
satc-site/
├── index.html          ← The main website
├── netlify.toml        ← Netlify configuration
├── admin/
│   ├── index.html      ← CMS login page (yourdomain.com/admin)
│   └── config.yml      ← CMS field definitions (edit with care)
└── _data/
    ├── shows.json      ← Upcoming show dates ← BAND EDITS THIS
    ├── quotes.json     ← Fan/press quotes    ← BAND EDITS THIS
    ├── hero.json       ← Homepage tagline    ← BAND EDITS THIS
    ├── about.json      ← About section text  ← BAND EDITS THIS
    └── booking.json    ← Booking section     ← BAND EDITS THIS
```

---

## One-Time Setup (You Do This Once)

### Step 1 — Create a GitHub Repository
1. Go to github.com and create a free account (or log in)
2. Click **New repository**
3. Name it `saylor-and-the-captains` (or anything you like)
4. Set it to **Public**
5. Upload all files from this folder into the repo

### Step 2 — Deploy to Netlify
1. Go to netlify.com and create a free account
2. Click **Add new site → Import an existing project**
3. Choose **GitHub** and select your repo
4. Leave all build settings blank (this is a static site)
5. Click **Deploy site**
6. Netlify will give you a URL like `amazing-name-123.netlify.app`
7. Optional: connect a custom domain (e.g. `saylorandthecaptains.com`) under Site Settings → Domain Management

### Step 3 — Enable Netlify Identity (for CMS login)
1. In your Netlify dashboard, go to **Site configuration → Identity**
2. Click **Enable Identity**
3. Under **Registration**, set to **Invite only** (so only you can add users)
4. Under **Services → Git Gateway**, click **Enable Git Gateway**
5. Go to **Identity → Invite users** and enter each band member's email
6. They'll receive an email to set a password

### Step 4 — Test the CMS
1. Go to `yourdomain.netlify.app/admin`
2. Log in with your email and password
3. You should see the content editor with Shows, Quotes, and Site Content sections

---

## How Band Members Update Content

### Adding a Show
1. Go to `yourdomain.com/admin`
2. Log in
3. Click **Shows → Show Dates**
4. Click **Add shows_list item**
5. Fill in: Date, Venue Name, Location, Show Time, and optionally a Ticket URL
6. Click **Publish** (top right)
7. The site updates automatically within ~30 seconds

### Removing a Past Show
Past shows are automatically hidden on the website (the site checks today's date).
But to keep things tidy, you can also delete them manually in the CMS.

### Adding a Fan Quote
1. Click **Fan Quotes → Quotes**
2. Click **Add quotes_list item**
3. Type the quote (no quotation marks needed) and the source
4. Click **Publish**

### Updating the About Text
1. Click **Site Content → About Section**
2. Edit any of the three paragraphs, the featured quote, or its source
3. Click **Publish**

---

## What Each Band Member Needs
- Their email address (you invite them from Netlify dashboard)
- A password they set via the invite email
- The URL: `yourdomain.com/admin`
- That's it — no GitHub account, no coding knowledge required

---

## Updating the Design
Design changes (colors, fonts, layout) require editing `index.html` directly.
That's best handled by your developer (you). The band's CMS access only touches the `_data/` JSON files.

---

## YouTube Video
The live performance video embedded on the site is currently:
`https://www.youtube.com/embed/el_gY7-gFt4`
(Saylor and The Captains at Space Coast Harley-Davidson, via Space Coast Daily)

To change it, edit the `src` attribute of the `<iframe>` in `index.html`.
Future: this can be added as a CMS-editable field.

---

*Built June 2025. Spring Tide Strategies.*
