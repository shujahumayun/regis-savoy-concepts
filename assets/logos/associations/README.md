# Association marks

Built 2026-08-04 for the Thoughtful Leadership &amp; Mentorship and Associations pages, replacing
the placeholder monogram cards with real institution logos in a scroll gallery.

Same pipeline and canvas as `../deals/` (`../normalise_logos.py`, adapted as
`normalise_associations.py` in the session scratchpad): 440x150 transparent PNGs, single ink
(`#071B3B`), scaled by ink mass, displayed at 220x75. Every mark here rasterised clean in plain
`dark` mode on the first pass, no `silhouette`/`invert` handling needed, since the two knockout
marks (LSE's white-on-red box, NYU's white torch on purple) both fall inside the "any pixel
darker than near-white is ink" rule and resolve to the right shape on their own.

## What is here (14, 7 for Ideas/Associations plus 7 for Education/Wildlife/Mentorship)

| Mark | Source | Note |
| --- | --- | --- |
| FRSA | Wikimedia Commons, `RSA_logo.svg` | wordmark plus its underline bar, both part of the mark |
| LSE | Wikimedia Commons, `London_school_of_economics_logo_with_name.svg` | full lockup, crest and wordmark |
| New York University | Wikimedia Commons, `Nyu_long_color.svg` | |
| Friedrich-Alexander-Universität Erlangen-Nürnberg | Wikimedia Commons, `..._Logo_07.2022.svg` | current 2022 mark |
| Teach For India | teachforindia.org site header | reused on the Education and Mentorship pages |
| Acumen Fund | Wikimedia Commons, `Acumen_logo.png` | source carries a "changing the way the world tackles poverty" tagline underneath, cropped out before normalising |
| Tata Literature Live | litlive.in site header | the "literature live!" script wordmark only; the red M device and "The Mumbai LitFest" line were cropped out as too busy for a small tile |

Added 2026-08-08 for `beyond-wealth-education.html`, `beyond-wealth-wildlife.html` and `beyond-wealth-mentorship.html`, via `../normalise_beyond_wealth_marks.py`, same single-ink pipeline reading from the already-trimmed `../associations-color/` set instead of raw SVGs:

| Mark | Source | Note |
| --- | --- | --- |
| Jane Goodall Institute | `../_raw/janegoodall-wordmark-white.png` | already a white-on-transparent wordmark, needed `invert` mode instead of the usual `dark` mode |
| Ol Pejeta Conservancy | Desktop sourced PNG, see `../associations-color/README` equivalent history | |
| CRY, Child Rights and You | Desktop sourced PNG | brand is monochrome black by design, reads cleanly in navy too |
| PFA, People For Animals | Desktop sourced PNG | |
| BWC, Beauty Without Cruelty | Desktop sourced PNG | low-res source, mark is legible but soft at small sizes |
| CUPA, Compassion Unlimited Plus Action | Desktop sourced PNG | fine circular ring type, legible at the 220x75 display size but faint |
| ARF, Animal Rights Fund | Desktop sourced PNG | unconfirmed match, same caveat as the associations-color source |

## Resolved 2026-08-11

Two of the three below are now sourced, from client-supplied files dropped straight into
`../associations-color/` in full colour (no single-ink navy pass, unlike the rest of this
folder) and wired into every rail, mgallery and mention grid that carried their text fallback:

| Mark | File | Note |
| --- | --- | --- |
| Queen Elizabeth Diamond Jubilee Trust | `../associations-color/07-queen-elizabeth-diamond-jubilee-trust.png` | The Trust itself still has no logo, per the original note below (wound up 2020, no body to clear a mark). The client supplied The Queen's Young Leaders emblem instead, the programme QEDJT ran; that displays under the Trust's name sitewide now |
| NITI Aayog & Atal Tinkering Labs | `../associations-color/08-atal-innovation-mission-niti-aayog.png` | Client-supplied combined NITI Aayog / Atal Innovation Mission lockup, still carries the Government of India emblem. Client clearance implied by supplying the file directly; confirm in writing before this goes fully live if that hasn't happened |

**UN PRI** is still text-only, unchanged, see below.

A third mark, **Karuna Mother Teresa Charitable Trust**, was also a text fallback (never tracked
in the "missing 3" list below since it wasn't part of this folder's original sourcing pass) and
is now resolved the same way: client-supplied seal, `../associations-color/18-karuna-mother-teresa-charitable-trust.png`.

Original notes, kept for context:

## What was missing (3 of 10)

Placeholder text stands in on the page for these, so both pages stay publishable.

| Mark | Why |
| --- | --- |
| **UN PRI** | Status is "application submitted", not signatory. Showing the mark before that is confirmed misrepresents the relationship on a SEBI regulated firm's site |
| **NITI Aayog & Atal Tinkering Labs** | Carries the Government of India emblem, restricted under the State Emblem of India Act. Atal Tinkering Labs (AIM) has its own separate mark if the client wants the tile split later |
| **Queen Elizabeth Diamond Jubilee Trust** | The Trust wound up in 2020. No live body exists to grant permission, and the only sources found (seeklogo, iconape) are third-party archive reproductions, not an official file. Needs its own call before any mark is sourced or shown |

## Before publish

Same gate as `../deals/`: these are third party trademarks. Sourcing a clean file is not
permission to display it. Written clearance is required per institution before any of these
fourteen marks (the original seven plus the 2026-08-08 Education/Wildlife/Mentorship set)
replaces its text fallback on the live site.
