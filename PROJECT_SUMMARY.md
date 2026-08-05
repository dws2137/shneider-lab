# Shneider Lab Website — Project Summary

A multi-page static website built for Neil A. Shneider, MD, PhD (Columbia University,
Eleanor and Lou Gehrig ALS Center). Self-contained HTML/CSS, no build step, designed
to be hosted for free on GitHub Pages.

## Design direction
- **Palette:** true red / white / blue. Off-white (near-white, cool-toned) background,
  deep navy-blue ink for text, bright red as the primary accent, and a medium blue
  ("steel") as a secondary accent — no amber, orange, or tan tones anywhere.
- **Type:** Source Serif 4 (headers), IBM Plex Sans (body), IBM Plex Mono (data,
  citations, tags) — loaded via Google Fonts CDN.
- **Signature motif:** a soma rendered as an atom (nucleus + three rotating orbit
  rings) fused with a motor axon — a visual pun on "FUS" (the RNA-binding protein
  the lab studies) and "fusion." Used in the nav logo and animated in the homepage
  hero. The atom/soma is sized large relative to the thin axon line, reading like a
  classic cartoon motor neuron with a prominent cell body — applied consistently to
  both the nav logo (enlarged) and the homepage hero animation.

## Pages
| File | Purpose |
|---|---|
| `index.html` | Homepage — hero with axon signal animation, ASO mechanism animation/explainer, join CTA |
| `research.html` | Three research pillars: RNA-binding protein toxicity, iPSC disease models, genetic therapies (links out to Silence ALS) |
| `silence-als.html` | Dedicated page for the lab's ASO/ulefnersen program — mechanism diagram, milestone timeline, related publications |
| `people.html` | PI profile (Dr. Shneider, featured) + lab roster as a one-profile-per-row list |
| `publications.html` | Selected Publications (3 highlighted cards) + Complete Bibliography (reverse-chronological list) |
| `contact.html` | Lab address, email, map placeholder, prospective-trainee note |
| `style.css` | Shared stylesheet — all pages pull from this one file for consistent theming |

## Grounded content
Real, verifiable facts were used instead of generic placeholder science:
- Dr. Shneider directs the Eleanor and Lou Gehrig ALS Center and the Center for
  Motor Neuron Biology and Disease at Columbia.
- Lab focus: FUS/TDP-43 RNA-binding protein toxicity, iPSC-derived motor neuron
  models, mouse genetics.
- Real cited papers:
  - Sharma A, et al. *Nature Communications* (2016) — mutant FUS toxic gain of function
  - Korobeynikov VA, et al. *Nature Medicine* (2022) — ASO silencing of FUS
  - Shneider NA, et al. *The Lancet* (2025) — jacifusen/ulefnersen case series
- The ASO mechanism diagram (homepage and Silence ALS page) is **original artwork**,
  not a reproduced journal figure — captioned with citations to the real papers.

## Iteration history
1. **Initial build:** single-page site inspired by sternberglab.org's structure,
   with GitHub Pages hosting instructions.
2. **Split into pages:** separated Research, Publications, and Contact into their
   own HTML files sharing `style.css`; added step-by-step GitHub repo setup
   instructions.
3. **Branding/content pass:** atom-fused motor neuron logo, red accent, ASO
   homepage animation, affiliate logo placeholders, Selected vs. Complete
   publications split.
4. **Palette + structure refinement:** shifted to red/white/blue, enlarged the atom
   motif, added a Silence ALS tab, moved the PI profile/team roster to a dedicated
   People page.
5. **Latest pass (this session):**
   - Replaced the remaining warm/cream tones (background, borders, and the
     coral-leaning "orange" accent used for eyebrow text on dark panels) with a
     cooler, true red/white/blue set of variables in `style.css`. Because every
     page pulls colors from CSS variables, this single change re-themes all pages.
   - Enlarged the atom/soma proportion in both the nav logo (also sized up overall)
     and the homepage hero animation, so the cell body reads bigger relative to the
     axon — more like a classic cartoon neuron.
   - Enlarged and bolded the "Columbia University · Department of Neurology" line
     on the homepage hero, now set in the accent red (`.eyebrow-lg`).
   - Removed the PI profile and team roster from `index.html`; both now live only
     on `people.html`.
   - Rebuilt `people.html`'s lab roster as a one-profile-per-row list
     (`.people-list` / `.person-row`) instead of a grid, with room for a short bio
     per person. Dr. Shneider's featured profile (with the two affiliate logo
     slots) stays at the top of the same page.
   - Built out `silence-als.html`: mechanism diagram (reused/re-skinned from the
     homepage), a four-step numbered program timeline (mouse model →
     compassionate use → case series → global trial), related-publication cards,
     and a contact CTA. Added a "Silence ALS" tab to the nav on every page.

## Known open items
- Replace all bracketed placeholders: PI headshot, lab roster names/photos/bios,
  mailing address, phone number, and the two affiliate `.logo-slot` placeholders
  on `people.html`.
- Embed a real Google Map on `contact.html` once the building address is set.
- Do a final visual pass once real photos/logos are in, since placeholder boxes
  can shift the balance of a section.

## How to deploy
1. Create a GitHub repo (ideally named `<username>.github.io` for the root domain).
2. Upload all files in this folder to the repo root (not a subfolder).
3. In **Settings → Pages**, set source to `main` branch, `/ (root)`.
4. Site goes live at `https://<username>.github.io/` within a couple of minutes.
