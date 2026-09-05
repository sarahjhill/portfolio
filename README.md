# Sarah Hill — Portfolio

[![Deployment](https://img.shields.io/badge/deployment-GitHub_Pages-purple)](https://sarahjhill.com/portfolio/)
[![GitHub last commit](https://img.shields.io/github/last-commit/sarahjhill/portfolio)](https://github.com/sarahjhill/portfolio/commits/main)
[![GitHub repo size](https://img.shields.io/github/repo-size/sarahjhill/portfolio)](https://github.com/sarahjhill/portfolio)

**Live site:** [sarahjhill.com/portfolio](https://sarahjhill.com/portfolio/)

## Introduction

A single-page developer portfolio for Sarah Hill, Full-Stack AI Developer. It exists to do one job fast: show a recruiter or client the stack, the real projects, and the story — with a human pulse instead of corporate jargon.

The page is branded to sit alongside [Dragon Fire Design](https://sarahjhill.com/), Sarah's freelance studio for tradeswomen and small businesses — same flame/amber palette, same "no bespoke solutions tailored to your needs" voice, same free-of-jargon rule.

## UX

### The 5 Planes of UX

**1. Strategy**

- **Purpose** — get a visitor from "who is this?" to "I want to talk to her" in under a minute, with proof (real projects, real code) rather than claims.
- **Primary user needs** — a recruiter scanning for stack fit; a potential client checking for trustworthiness and personality; Sarah herself, as a living CV she can point people to.
- **Project goals** — demonstrate front-end craft (animation, accessibility, responsive layout) as much as list it in prose.

**2. Scope**

- Hero with stack/hackathon pills and animated stats
- About section pulled from Sarah's own CV language
- Skills grid (Full-Stack & AI, Human-Centric Design, Team Building)
- Six project cards, each with an honest case-study modal
- Journey timeline (Code Institute programme, consultancy years, education)
- Contact CTA and footer cross-link to Dragon Fire Design

**3. Structure**

Single page, anchor-linked nav (About / Skills / Work / Journey), case studies open as modals rather than separate pages so the visitor never loses their place.

**4. Skeleton**

Bootstrap 5's grid and components (navbar, modal, cards) as the skeleton, with a full custom dark theme layered on top via CSS custom properties.

**5. Surface**

See Colour Scheme and Typography below.

### Colour Scheme

Tokens are matched exactly to Dragon Fire Design (`sarahjhill.com`), not invented separately:

| Token | Hex | Use |
| --- | --- | --- |
| `--bg` | `#0a0a0c` | Page background (ink) |
| `--bg-soft` | `#141419` | Alternating section band |
| `--card` | `#1c1c22` | Cards, modals |
| `--flame-1` | `#ff3b1f` | Primary accent, CTAs, brand surname |
| `--flame-2` / amber | `#ffb020` | Secondary accent, brand tagline, outline buttons |
| `--ink-dim` | `#8b8b95` | Secondary text |

### Typography

- [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (Google Fonts) — headings, brand lockup, stat numbers.
- [Inter](https://fonts.google.com/specimen/Inter) (Google Fonts) — body copy and UI text.

## Features

### Existing Features

| Feature | Notes |
| --- | --- |
| Animated hero stats | Count-up-on-scroll for shipped apps, live platforms, and a "0 buzzwords" joke stat. |
| Stack/hackathon pill strip | Python, Django, JavaScript, Hackathon-tested — scannable in seconds. |
| Case study modals | Six projects, each with role, real stack, honest status (including team-project and prototype disclaimers) and a feature list that staggers in on open. |
| Screenshot lightbox | Custom-built (no external library) — keyboard arrows, click-through gallery, captions, for Cardiff Community Meals and Mission Control. |
| Dragon Fire Design tie-in | Matching logo lockup, exact brand colour tokens, and a direct pull-quote from the studio site. |
| Fully responsive | Verified at 375px (mobile) through desktop — nav collapses, cards restack, modals scroll independently. |
| Dark-theme accessible contrast | `data-bs-theme="dark"` so Bootstrap's own secondary-text tokens meet contrast, not just the custom palette. |

### Future Features

Tracked as [GitHub Issues](https://github.com/sarahjhill/portfolio/issues) rather than left as a wishlist here:

- Real screenshots for the CarbMate and CodeStar Blog case studies, once both are redeployed.
- Redeploy `carbmate` and `codesta-blog` to Heroku (both currently offline).
- Consider folding in Many Voices, Muslimah Web Design, and a fuller SJH Process write-up from sarahjhill.com.
- Full keyboard-trap and screen-reader pass on the case study modals and lightbox.
- Custom domain, and a real contact form instead of `mailto:`.

## Tools & Technologies

| Tool / Tech | Use |
| --- | --- |
| [![badge](https://img.shields.io/badge/HTML-grey?logo=html5&logoColor=E34F26)](https://en.wikipedia.org/wiki/HTML) | Semantic page structure |
| [![badge](https://img.shields.io/badge/CSS-grey?logo=css&logoColor=1572B6)](https://en.wikipedia.org/wiki/CSS) | Custom theming layered on Bootstrap |
| [![badge](https://img.shields.io/badge/JavaScript-grey?logo=javascript&logoColor=F7DF1E)](https://www.javascript.com) | Reveal animations, count-up stats, modal stagger, custom lightbox |
| [![badge](https://img.shields.io/badge/Bootstrap-grey?logo=bootstrap&logoColor=7952B3)](https://getbootstrap.com) | Grid, navbar, modal, dark colour mode |
| [![badge](https://img.shields.io/badge/Google_Fonts-grey?logo=googlefonts&logoColor=4285F4)](https://fonts.google.com) | Space Grotesk and Inter typefaces |
| [![badge](https://img.shields.io/badge/Bootstrap_Icons-grey?logo=bootstrap&logoColor=7952B3)](https://icons.getbootstrap.com) | Iconography throughout |
| [![badge](https://img.shields.io/badge/GitHub_Pages-grey?logo=githubpages&logoColor=222222)](https://pages.github.com) | Hosting |
| [![badge](https://img.shields.io/badge/GitHub_Actions-grey?logo=githubactions&logoColor=2088FF)](https://github.com/features/actions) | Auto-deploy to Pages on every push to `main` |
| [![badge](https://img.shields.io/badge/Claude-grey?logo=claude&logoColor=D97757)](https://claude.ai) | Planning, build, and content assistance — see AI Tool Usage below |

## AI Tool Usage

Claude (Anthropic) was used throughout development: structuring the page, writing and reviewing HTML/CSS/JS, pulling real project facts from local READMEs and code rather than inventing them, and capturing real screenshots of the Cardiff Community Meals and Mission Control prototypes via a scripted headless browser.

All content decisions, brand direction, and final review were Sarah's. Case studies were deliberately written to be honest about scope — Mission Control is credited as a four-person team project, not a solo build, and CarbMate carries its "not a medical device" disclaimer exactly as written in the project's own README.

## Testing

Manual testing covered:

- Console-clean load (no JS errors) on initial load and after every modal/lightbox interaction.
- Responsive check at 375px (mobile) and desktop widths — nav collapse, card restacking, modal scroll behaviour.
- Modal + lightbox function: open/close, keyboard arrow navigation, focus/backdrop behaviour, staggered feature reveal on open.
- All internal anchors and external project links resolve to their live targets.

No automated test suite yet — see [Future Features](#future-features).

## Deployment

### GitHub Pages via GitHub Actions

This repo deploys automatically on every push to `main`:

- `.github/workflows/static.yml` uploads the repository root as the Pages artifact and deploys it — no build step, since this is plain HTML/CSS/JS.
- One-time setup: **Settings → Pages → Build and deployment → Source → GitHub Actions**.
- Live at [sarahjhill.com/portfolio](https://sarahjhill.com/portfolio/) a minute or two after each push.

### Local Development

No build tools required:

```bash
git clone https://github.com/sarahjhill/portfolio.git
cd portfolio
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Credits

### Content

| Source | Notes |
| --- | --- |
| [Markdown Builder](https://markdown.2bn.dev/) | Tim Nelson, Code Institute — used to structure this README |
| [Claude](https://claude.ai) | Build assistance, code review, and case-study research — see AI Tool Usage |

### Brand

| Source | Notes |
| --- | --- |
| [Dragon Fire Design](https://sarahjhill.com/) | Sister site — brand colours, logo lockup, and tagline sourced from here |

### Fonts & Icons

| Source | Notes |
| --- | --- |
| [Google Fonts](https://fonts.google.com) | Space Grotesk and Inter |
| [Bootstrap Icons](https://icons.getbootstrap.com) | Icon set throughout |

### Featured Projects

Cardiff Community Meals, Mission Control, CarbMate, and CodeStar Blog are all Sarah's own repositories — see [github.com/sarahjhill](https://github.com/sarahjhill) for source.
