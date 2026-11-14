# Moral Panic website: handoff for Claude Code

This folder holds the approved design ("A · Red Wedge") as a working, static page. The goal is to turn it into the live one-page site for Moral Panic, keeping the look exactly as it is.

## What's here

- `index.html`: the full page in plain HTML and CSS, no build step. Open it in a browser to see the design.
- `assets/logo/`: the logo as transparent PNGs, cut from the official social pack.
  - `logo-horizontal.png`: mark + wordmark side by side (used in the header)
  - `logo-stacked-on-cream.png` / `logo-stacked-on-black.png`: the stacked lockup
  - `mark-on-cream.png` / `mark-on-black.png`: the halftone circle + red wedge on its own (good for favicon / social images)

## The page, top to bottom

1. Header: horizontal logo, one nav link ("Get in touch", jumps to the sponsor section).
2. Hero: huge "MORAL PANIC" wordmark, the halftone circle and the red wedge from the logo at page scale. All CSS, no images.
3. Intro line ("A video series exploring the fault lines of modernity, hosted by Raza Jafri and Buster Franken.") next to a black signup panel: "Next episode: The Jensen interview", email field, "Notify me" button.
4. "Watch and listen": YouTube, Spotify, Instagram, TikTok, X.
5. "Sponsor / Collaborate": black band with a slanted top edge and a "Get in touch" button.
6. Footer: "Moral Panic".

## Brand

| Token | Hex | Use |
|---|---|---|
| Cream | `#EDE3CC` | page background, text on black |
| Ink | `#111111` | text, black panels |
| Red | `#D7261E` | the wedge, the "Notify me" button |
| Halftone grey | `#8C8577` | circle behind the halftone dots |

Type is **Jost** (Google Fonts, weights 500–900), a stand-in for the logo's geometric typeface. If the real font file turns up, swap it in. Visual language: constructivist, flat colour, hard edges, no rounded corners, no gradients, no shadows.

## What still needs doing

- [ ] **Email signup**: connect the form to the newsletter service: [SERVICE: e.g. Kit, Buttondown, Mailchimp, Beehiiv]. Show a short confirmation in place of the form after submitting, in the same style.
- [ ] **Channel links**: fill in the real URLs:
  - YouTube: [URL]
  - Spotify: [URL]
  - Instagram: [URL]
  - TikTok: [URL]
  - X: [URL]
- [ ] **Contact**: make "Get in touch" a `mailto:` link to [CONTACT EMAIL].
- [ ] **SEO / sharing**: page title, description, Open Graph + Twitter card image (1200×630, can be built from the logo), favicon from `mark-on-cream.png`.
- [ ] **Hosting**: deploy to [Vercel / Netlify / GitHub Pages], on [DOMAIN] if there is one.
- [ ] Keep it fast and simple: a static site is enough. Don't add a framework unless it's needed for the signup integration.
- [ ] Check it at phone width (≈390px) and desktop (≈1440px); the layout already stacks on phones.

## Suggested first prompt for Claude Code

> Read HANDOFF.md and open index.html. This is the approved design for the Moral Panic website. Keep the design pixel-identical. First ask me for anything marked [LIKE THIS] that you need, then wire up the email signup, fill in the links, add SEO/social tags and a favicon, and help me deploy it.
