# Free HTML fitness website template with GSAP scroll animations — Arcline

**Website for a fitness or sports training club with coaches, a weekly schedule and membership plans: a free HTML template in one file, with GSAP scroll animations, no build step, MIT license. Made by [8B](https://8b.com/), the AI website builder.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![one HTML file: no build](https://img.shields.io/badge/one%20HTML%20file-no%20build-orange) ![GSAP: ScrollTrigger](https://img.shields.io/badge/GSAP-ScrollTrigger-88ce02)

**[Live demo](https://8bsite.github.io/fitness-website-template/)** · **[Use this template](https://github.com/new?template_name=fitness-website-template&template_owner=8bsite)** · **[Download ZIP](https://github.com/8bsite/fitness-website-template/archive/refs/heads/main.zip)**

<a href="https://8bsite.github.io/fitness-website-template/"><img src="previews/desktop.png" alt="Arcline, a free HTML template: first screen on a desktop" width="76.1%"></a> <a href="https://8bsite.github.io/fitness-website-template/"><img src="previews/phone.png" alt="Arcline, a free HTML template: first screen on a phone" width="21.9%"></a>

<p align="center"><a href="https://8bsite.github.io/fitness-website-template/"><img src="previews/scroll.gif" alt="Arcline, a free HTML template: scrolling through the first sections on a desktop" width="40%"></a><br><sub>Scroll animation</sub></p>

A one-page site for a performance training club with its own test lab, covering running, cycling, swimming, court sports and strength. Every section is a framed slide floating on a cold blue-grey mist: headings streak in and out like sprinters, tiles are dealt from a deck, a lens opens on the lab photo and the week's schedule runs sideways as you scroll.

Good for: gym, fitness or training club; running, cycling or triathlon coaching; personal trainer or coaching studio with membership plans; sports performance lab or physio clinic; multi-sport club with a weekly class schedule.

## Use it with an AI coding agent

Download the files into your project (in Windows PowerShell type `curl.exe`):

```bash
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/CREDITS.md
```

Then give your agent this prompt:

```text
Read AGENTS.md, then edit index.html. Use this template as the base for a site for <your gym, club or coaching business: what you train, where, coaches, schedule, prices, how to book>. Keep the layout, the motion and the single-file format; replace the brand name, copy, photos, coaches, schedule, prices, links and contacts, and recolour it through the CSS variables if needed.
```

Give the agent the downloaded file, not a link: from a link it would rebuild a different page. No agent? Click **[Use this template](https://github.com/new?template_name=fitness-website-template&template_owner=8bsite)**, edit `index.html` and turn on **Settings → Pages**.

## What's on the page

- **Navigation** — top bar: wordmark, a short tagline, section links, Book a test button; phone menu overlay
- **Faster than your own shadow** — two-screen opening: a navy cover slide with a photo and a three-line stepped headline, then a pale manifesto slide (demo: racket photo, "Only forward®")
- **Tested Monday. Faster by spring** — how it works: three numbered steps beside a big heading with round photos set into its lines (demo: Test, Train, Transfer)
- **Breathe. Move. Repeat.** — a three-word line over a collage of tiles, one per activity, plus a link tile (demo: strength, running, cycling, swimming, gait fitting, court sports)
- **Coached by people who still race** — four coach portraits of different heights with names and roles
- **What the lab sees** — a feature block: text on the left, a round photo ringed by four labelled measures on the right (demo: test lab, VO₂ max, threshold)
- **A week at Arcline** — weekly schedule: seven day cards in a row that runs sideways as you scroll, with a progress line
- **Members, retested** — testimonials: one large quote with a round portrait in its first line and two short quotes
- **Recovery is part of the rep** — a stepped heading, a lead and four services in two columns, beside a window of sky over calm water (demo: recovery suite)
- **Membership** — pricing: three plans in ruled columns, the middle one highlighted
- **Before your first test** — questions and answers (native &lt;details&gt;) beside a rail with a rolling ball
- **Book your first test** — booking: a heading on a line across the slide, address, hours, phone, email and a short form (placeholders)
- **Footer** — width-filling wordmark, a line about the club, links, socials, copyright and the Design: 8B credit

## Design

Palette: ![#ffffff](https://img.shields.io/badge/-%23ffffff-ffffff?style=flat-square) ![#0b1019](https://img.shields.io/badge/-%230b1019-0b1019?style=flat-square) ![#1a2333](https://img.shields.io/badge/-%231a2333-1a2333?style=flat-square) ![#dbe4ec](https://img.shields.io/badge/-%23dbe4ec-dbe4ec?style=flat-square) ![#9db1c4](https://img.shields.io/badge/-%239db1c4-9db1c4?style=flat-square) ![#536477](https://img.shields.io/badge/-%23536477-536477?style=flat-square) ![#2f54e0](https://img.shields.io/badge/-%232f54e0-2f54e0?style=flat-square) ![#edf2f6](https://img.shields.io/badge/-%23edf2f6-edf2f6?style=flat-square)  
Fonts: Geist (Google Fonts). Change both through the CSS variables in the `:root` block at the top of `<head>`. A big display line with `style="--len:N"` fills its width: set N to its new number of characters.

- The spheres, orbit rings and slide corner marks are CSS and SVG, not images: recolour them through the CSS variables in :root.
- Display lines with style="--len:N" (opening headline, "Only forward®", "Breathe. Move. Repeat.", footer wordmark) fill their width: set N to the new number of characters; a trailing ® counts as one ("arcline®" → 8, "Only forward®" → 13).
- The wordmark is written in lower case ("arcline") in the nav and the footer: a case-sensitive search for "Arcline" misses it.

## Before you publish

- Replace everything marked `data-8b-placeholder` (social preview image, favicon, phone, email, form, social) and the invented demo facts: prices, dates, address. [AGENTS.md](AGENTS.md) lists them.
- The form sends nothing yet: connect it to Formspree or Netlify Forms, or remove it.

## Tech

GSAP 3.13.0, ScrollTrigger, Lenis 1.3.27 from jsDelivr, 90 KB, no build step. Chrome and Edge 111+, Safari 16.2+, Firefox 113+ (it uses color-mix(), container query units, cascade layers, small/dynamic viewport units). With "reduce motion" on, the page is complete and still.

## License

MIT, see [LICENSE](LICENSE); the "Design: 8B" footer link is welcome, not required. Photos, fonts and libraries keep their own licences: [CREDITS.md](CREDITS.md). More free templates: [github.com/8bsite](https://github.com/8bsite).
