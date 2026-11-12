# T M Professional Window Cleaning website

A one-page site in plain HTML, CSS and JavaScript. There's no build step, no framework and nothing to install. The fonts are bundled in the folder, so it doesn't rely on Google Fonts.

```
index.html          the whole page
css/styles.css      all styling
js/main.js          menu, hero window, postcode check, quote form
assets/             fonts (Manrope), favicon, app icon, social share image
robots.txt          lets search engines in and points them to the sitemap
sitemap.xml         the page list for Google
CNAME               tells GitHub Pages the site's domain
PRODUCT.md          what the business is, for design tools (Impeccable)
DESIGN.md           the visual system: colours, type, components
.impeccable/        design-tool working files (share-image source pages, review screenshots)
```

The look is deep navy and clear window blues with white, set in Manrope. The area diagram plots each village at its real map position.

**To preview:** double-click `index.html` (Chrome or Safari). 

---

## 1. How the quote form works

The form posts to an n8n workflow, **"TM Professional Window Cleaning - Website Quote Form"** (n8n project: Jake's personal project). The webhook address is at the top of the quote-form section in `js/main.js`.

For each submission, the workflow:

1. Checks for spam (a hidden trap field, forms sent in under 3 seconds, link-stuffed messages, more than 5 in an hour from one connection) and for missing details.
2. Logs every submission, including spam and invalid ones, to Supabase: the Roof & Render CRM project, table `tm_enquiries`. New leads have `lead_status = 'new'`.
3. Emails Tim a branded enquiry from tmprofessionalwindowcleaning@gmail.com, with Call / WhatsApp / Reply buttons, and marks it unread so it stands out.
4. If the customer left an email address, sends them a "thanks, your request is in" confirmation from Tim's Gmail.

The website shows "Thanks" when the email to Tim goes out. If the workflow spots a problem, the visitor sees its message. If anything fails, they're asked to call or WhatsApp 07799 963390.

To see all enquiries: Supabase → CRM project → Table editor → `tm_enquiries`.

## 2. Business name

The business is called "T M Professional Window Cleaning". To change it later:

- Find and replace `T M Professional Window Cleaning` throughout `index.html` (title, share text, schema `name`, form email name and footer).
- Replace the logo text in the two `<span class="brand-name">T M</span>` / `<span class="brand-sub">Professional Window Cleaning</span>` pairs (header and footer).
- Regenerate `assets/og-image.png` (the preview image shown when the link is shared on WhatsApp or Facebook), because the name is in it. It's a screenshot of `.impeccable/assets-src/og.html` at 1200×630; edit that page and ask Claude to re-shoot it.

The phone number appears as `07799 963390` and `447799963390`, so a find and replace handles both if it ever changes.

## 3. Check these with Tim before going live

The copy describes standard pure-water window cleaning practice. Tim should confirm he's happy to say each of these:

- Frames and sills are cleaned as part of the regular round
- Upstairs windows are done from the ground with a water-fed pole
- Customers don't need to be in, as long as there's access to the back
- He lets customers know before each visit
- He'll pop round to price a job if needed
- He reschedules only for heavy rain, high winds or frost
- Conservatory roofs are done with soft brushes, and downpipes are checked when gutters are cleared (services offered: windows, conservatory roofs, gutters and fascias)
- WhatsApp works on 07799 963390

## 4. Add trust signals when Tim has them

There are no reviews, insurance details or years in business on the site yet, on purpose, because none of it should be made up. When Tim has them:

- **Reviews:** a ready-made section is commented out in `index.html` (search `REVIEWS`). Uncomment it and add real reviews only.
- **Insurance / experience / About Tim:** ask Claude to add a short line under the hero or an About section.
- **Photos:** real before-and-after shots of Tim's work beat anything else for winning trust.

## 5. Put it online (free)

1. Buy the domain (around £10 a year) from Cloudflare, Namecheap or 123-reg.
2. Host it free on **Cloudflare Pages** or **Netlify**: create an account, choose *upload / drag and drop*, and drop this whole folder in. Then connect the domain in their settings, and HTTPS is automatic.
3. Once the domain is live, ask Claude to add the full web address to the page's share and search tags (it makes link previews and Google listings more reliable).
4. Set up a free **Google Business Profile** for Tim with the same name, number and service area. For a local trade it brings in more enquiries than anything else.
5. Add the site to **Google Search Console** so it gets indexed quickly.

---

### How the hero window works

The whole window starts dirty. Visitors clean it by running their mouse over the glass (or swiping across it on a phone), or click *let Tim do it* to watch the squeegee clean it top to bottom. When the glass comes clean, pure water rinses down it and dries clear, the caption reads "That's how Tim will leave your windows every time." and a *Make it dirty again* button puts fresh grime back so they can go again. Anyone who has asked their device to reduce motion sees it without the animation.

### The postcode check

The box under the headline ("Is your street on the round?") answers instantly from the list of postcode districts in `js/main.js` (`COVERED`: CB1–CB5, CB7, CB8, CB21, CB22, CB24, CB25, IP28). Anything else gets a friendly "just off our usual round, ask anyway". Edit that list if Tim's area changes, and update the town list and area diagram in `index.html` to match.

## 5. Hosting and domain

- **Live site:** https://newmarketwindowcleaner.co.uk, hosted free on GitHub Pages from the `main` branch of `jake-austin94/tims-website`. Every push to `main` updates the live site within a minute or two.
- **Domain:** registered with Wix, pointed at GitHub Pages with these DNS records (Wix: Domains → the domain → Manage DNS records):

| Type | Host | Points to |
|---|---|---|
| A | @ (root) | 185.199.108.153 |
| A | @ (root) | 185.199.109.153 |
| A | @ (root) | 185.199.110.153 |
| A | @ (root) | 185.199.111.153 |
| CNAME | www | jake-austin94.github.io |

- Don't delete the `CNAME` file. It's how GitHub Pages knows the site's domain.
- **Email:** tmprofessionalwindowcleaning@gmail.com is shown on the site, and quote-form enquiries are sent from and to it via n8n.
- Next for local SEO: set up a free Google Business Profile with the same name, phone number and area, and add the site to Google Search Console (submit `https://newmarketwindowcleaner.co.uk/sitemap.xml`).
