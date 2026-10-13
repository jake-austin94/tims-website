# Tim's window cleaning website

A one-page site in plain HTML, CSS and JavaScript. There's no build step, no framework and nothing to install. The fonts are bundled in the folder, so it doesn't rely on Google Fonts.

```
index.html          the whole page
css/styles.css      all styling
js/main.js          menu, hero window animation, quote form
assets/             fonts, favicon, phone icon, social share image
robots.txt
```

**To preview:** double-click `index.html` (Chrome or Safari). The form only sends once step 1 is done.

---

## 1. Connect the quote form (5 minutes, free)

1. Go to **web3forms.com**, type in the email address Tim wants enquiries sent to, and click *Create Access Key*.
2. The key arrives by email. It looks like `a1b2c3d4-....`
3. Open `index.html`, search for `YOUR_WEB3FORMS_ACCESS_KEY` and paste the key in its place.
4. Send a test enquiry from the live site and check it lands in Tim's inbox (and his spam folder the first time).

The free plan allows 250 enquiries a month. Each email includes the customer's name, phone, email (if given), postcode, property type, services, frequency and message. If the customer gives an email address, Tim can just hit Reply.

## 2. Business name

The business is called "Tim’s Window Cleaning". To change it later:

- Find and replace `Tim’s Window Cleaning` throughout `index.html` (title, share text, schema `name`, form email name and footer).
- Replace the short logo word in the two `<span class="brand-name">Tim’s</span>` lines (header and footer).
- Regenerate `assets/og-image.png` (the preview image shown when the link is shared on WhatsApp or Facebook), because the name is in it. Ask Claude to redo it.

The phone number appears as `07799 963390` and `447799963390`, so a find and replace handles both if it ever changes.

## 3. Check these with Tim before going live

The copy describes standard pure-water window cleaning practice. Tim should confirm he's happy to say each of these:

- Frames and sills are cleaned as part of the regular round
- Upstairs windows are done from the ground with a water-fed pole
- Customers don't need to be in, as long as there's access to the back
- He lets customers know before each visit
- He'll pop round to price a job if needed
- He reschedules only for heavy rain, high winds or frost
- Conservatory roofs are done with soft brushes, and downpipes are checked when gutters are cleared
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

The whole window starts dirty. Visitors clean it by running their mouse over the glass (or swiping across it on a phone), or click *let Tim do it* to watch the squeegee clean it top to bottom. Once the glass is clean the caption reads "That's how Tim will leave your windows every time." and a *Make it dirty again* button puts fresh grime back so they can go again. Anyone who has asked their device to reduce motion sees it without the animation.
