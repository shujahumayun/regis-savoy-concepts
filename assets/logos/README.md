# Logo assets

Built 2026-08-04 for the Deals and Mandates gallery (homepage + Private Equity page), then
extended the same day for the Thoughtful Leadership &amp; Mentorship and Associations galleries.

## Layout

- `_raw/` — untouched sources exactly as downloaded. Never edit these, re-run the pipeline instead.
- `deals/`: normalised output for the fifteen deal companies. See `normalise_logos.py`.
- `associations/`: normalised output for the institution marks. See `associations/README.md`
  and `normalise_associations.py`.

Every mark, in both folders, is a 440x150 transparent PNG, single ink (`#071B3B`, the site's
midnight), displayed at 220x75.

## How they were normalised

Marks are scaled by **ink mass, not bounding box**. A compact badge and a wide hairline
wordmark set to the same pixel height look nothing like the same size, so each mark is scaled
until it carries the same alpha mass, then centred on a shared canvas. A few carry weight the
maths misreads (a solid disc reads heavier than its area suggests) and are nudged by hand.

Sources do not arrive in one shape, so ink extraction runs in one of three modes:

| Mode | When | Used for |
| --- | --- | --- |
| `dark` | dark pixels are ink, light is paper | the common case |
| `silhouette` | alpha already carries the shape, fill is one flat colour | Kreedo (white export, would vanish on ivory), Upaghna |
| `invert` | light type knocked out of a dark container | Adukale (white type in a dark pill) |

SVG sources are rasterised at 1600px through headless Chrome, since no SVG renderer is
installed locally.

## What is here (10 of 15)

| Mark | Source | Note |
| --- | --- | --- |
| Nykaa | Wikimedia, `Nykaa_New_Logo.svg` | nykaa.com blocks scripted fetches |
| BrijRama Palace | brijhotels.com `/img/logo.svg` | this is the Brij Hotels group mark, not a property specific one |
| Tugkraft | tugkraft.com | the arrow device is the mark, kept solid |
| University Living | cdn.universityliving.com | |
| Adukale | adukale.com (Shopify CDN) | |
| Rotoris | Shopify CDN | |
| Kreedo | kreedology.com, white export recoloured | |
| QNu Labs | inline SVG lifted from the site header | no standalone file is published |
| Upaghna Ventures | Wix static | |
| Harvesting | harvesting.co, the HFN mark | trades as HFN Kisan, confirm this is the mark the client means |

## What is missing (5 of 15)

Placeholder text monograms stand in on the page, so both pages are publishable as they are.

| Mark | Why |
| --- | --- |
| **dltledgers** | `dltledgers.com` now resolves to a **parked domain** (`ap:"parking"`). The company appears defunct. Confirm before showing the mark at all. |
| **CreditTap** | no conclusive company found, several unrelated fintechs share the name |
| **Nublo** | only match is a UAE payments app incorporated in Dubai 2022, cannot confirm same entity |
| **N Gen** | too generic to resolve, NGEN Research (Mumbai) is an unverified candidate |
| **Automatic Hospitality (AHIPL)** | no holding company mark exists publicly. Brands are findable individually: The Aures, Indian BBQ Co, Osteria, BLVD. Client decides whether the tile is a typeset wordmark or one brand mark. |

## Before publish

These are third party trademarks. Sourcing them is not the same as being allowed to display
them. `site-spec.md` carries the compliance gate: written clearance is required before naming
deals or clients on a SEBI regulated firm's site.

Seven of the ten association marks are now sourced, same gate applies. See
`associations/README.md` for what is here, what is still text, and why.
