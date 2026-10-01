# Hamilton Shop Starter Pack — sales page

Static sales page for the **Hamilton Shop Starter Pack**, a DIY digital template pack for
brick-and-mortar shops in Hamilton, Ontario.

**Live:** https://kunyi523.github.io/hamilton-shop-pack/

## What's in this repo

| File | Purpose |
|------|---------|
| `index.html` | The whole sales page — hero, what's inside, who it's for / not for, pricing, honesty, FAQ, 中文 blurb, footer CTA |
| `style.css` | Mobile-first styles. No build step, no framework, no JS |

That's it. Two files, no dependencies, no tracking, no ads, nothing paid.

## The product being sold

Three DIY items the buyer edits themselves:

1. One-page website template (single `index.html` + styles)
2. Printable quote / price cards
3. Google Business Profile checklist

Public prices (CAD, one-time): full pack **$49**, one-pager only **$29**, quote cards only
**$19**, Google checklist only **$15**.

The separate done-for-you one-pager service (~CAD $99) is mentioned on the page only as an
alternative for people who don't want to DIY. It is deliberately kept distinct from this pack.

## Product ZIP assets: not here yet

This repo currently holds **the sales page only**. The actual deliverable files — the template,
the card layouts, the checklist PDF — aren't built yet, and nothing on the page claims they
download automatically. Fulfilment is manual for now: a buyer emails, we reply with the total in
CAD and how to pay, then send the files by email.

When the deliverables exist, the plan is to add them under a `product/` directory (or host the
ZIP off-repo) and keep the page copy in sync.

## Payment

Buyers pay on Ko-fi: **https://ko-fi.com/xiaozhanghuchaindesk**. Every buy button on the page
points there.

Ko-fi doesn't reliably pass along which items were bought or where to send them, so the page asks
buyers to follow up by email to **likunyi020523@gmail.com** (subject `Hamilton Shop Pack — paid`)
with their shop name, what they bought, and the delivery address. Fulfilment is still manual.

`mailto:` links are otherwise used only for general questions and for asking about the separate
~CAD $99 done-for-you service. Don't add any other payment processor to the page unless an
account for it actually exists.

## Compliance ground rules

Copy on the page must keep these true:

- No guaranteed rankings, leads, customers, or revenue figures.
- No selling or soliciting fake reviews.
- Clearly a DIY template pack, not a build-it-for-you service.
- No domain purchase or DNS setup included.
- Prices stated in CAD; applicable tax confirmed by email before payment.
- Refunds: full refund before files are delivered; digital files generally non-refundable once sent.

## Local preview

Open `index.html` in a browser, or serve the directory:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/
```

## Deployment

Pages is enabled and serves from the `main` branch, root (`/`) folder. Pushing to `main`
republishes. The live URL can take a minute or two to reflect a change, and a
hard refresh clears a stale CDN copy.

`.github/workflows/pages.yml` covers the other option: if you pick **Source: GitHub Actions**
instead of a branch, that workflow uploads and deploys the page. It first checks which source is
configured and skips deploying when Pages is serving from the branch, since the two modes are
mutually exclusive — so it stays green either way.
