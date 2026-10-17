# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users
Homeowners (and some small shops and offices) in and around Newmarket, Suffolk, out to Cambridge: Newmarket, Exning, Kentford, Burwell, Soham, Fordham, Bottisham, Fulbourn, Cherry Hinton, Cambridge. Most arrive on a phone, often from a Google search, a Facebook group recommendation or a flyer/van. Their job: find a reliable local window cleaner, judge quickly whether he's trustworthy and covers their street, and get a price with as little effort as possible (call, WhatsApp or a short form).

## Product Purpose
A one-page site for T M Professional Window Cleaning, a sole-trader window cleaning round. It exists to turn a local visitor into a quote request. Success = more calls, WhatsApps and form submissions from people inside the service area.

## Positioning
Pure-water, water-fed-pole cleaning: glass, frames and sills scrubbed and rinsed with filtered water from the ground, no ladders, no chemicals, dries spot-free. A local, named person (Tim) on a regular 4- or 8-weekly round, not a faceless franchise.

## Operating Context
- Services: windows, frames and sills (the core round); conservatory roofs; gutters and fascias. Nothing else is offered at the moment.
- Frequency: every 4 weeks, every 8 weeks, or one-off.
- Contact: phone 07799 963390 (tel +447799963390), WhatsApp on the same number, quote form posting to Web3Forms (access key still to be added, see README).
- Confirmed by Tim: frames and sills cleaned on the regular round; upstairs done from the ground with a water-fed pole; customers needn't be in if there's access to the back; he lets customers know before each visit; he'll pop round to price if needed; reschedules only for heavy rain, high winds or frost; conservatory roofs done with soft brushes and downpipes checked when gutters are cleared; WhatsApp works on 07799 963390.

## Capabilities and Constraints
- Plain static HTML/CSS/JS, no build step, no framework, self-hosted fonts (no third-party font/CDN calls). Hosted on a free static host (Cloudflare Pages / Netlify). Must work by double-clicking index.html.
- Signature interaction: the hero window that starts dirty and the visitor cleans by hovering/swiping, or "let Tim do it" squeegees it. Must be kept and improved. Must respect reduced motion.
- Quote form: name, phone, optional email, postcode (with soft out-of-area hint), property type, services (multi), frequency, message; honeypot; client-side validation.
- Mobile quick-contact bar (Call / WhatsApp / Free quote).
- LocalBusiness schema, OG image (assets/og-image.png contains the business name).

## Brand Commitments
- Business name: "T M Professional Window Cleaning". The name stays.
- Complete visual rebrand authorised (logo, palette, type all open).
- Standing preference (2026-10-15): the category standard done at premium craft. Classic window-cleaning blues (deep navy, clear blue, sky, white). An OS-map concept with orange/magenta was tried and rejected as too bright and garish; no bold concept worlds or loud accent colours.
- Voice: plain, friendly, British, first-person plural ("we"), short sentences, no hype, no exclamation-mark salesmanship.

## Evidence on Hand
None yet: no reviews, no photos of work, no insurance details, no years-in-business figure. Do not invent any of these. A commented-out reviews block exists in index.html for later. Design should feel trustworthy without fake proof, and leave obvious slots for real reviews/photos when they arrive.

## Product Principles
1. One job: get a local person to ask for a price. Every section ends in a way to do that.
2. Show, don't claim: demonstrate the pure-water result (the window) rather than asserting quality.
3. Honest by construction: no fabricated proof, no stock-photo strangers.
4. Phone-first: most visitors are on a phone, often one-handed.
5. Local and personal: Tim is a real person on a real round in named villages.

## Accessibility & Inclusion
WCAG 2.2 AA. Keyboard-operable, visible focus, reduced-motion respected (the hero window must work without animation), large tap targets. Audience skews older homeowners: generous text size and contrast.
