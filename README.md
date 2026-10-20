# Free HTML fitness website template with GSAP scroll animations

Fitness website template: a one-page site for a gym, training club or coaching studio, with a test lab, four coaches, a seven day schedule that scrolls sideways, three membership plans and a booking form. The look is framed white, navy and pale slides on a misty blue-grey page. It is one HTML file with an AGENTS.md, so Claude Code, Cursor or Codex can adapt it to your club.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![one HTML file: no build](https://img.shields.io/badge/one%20HTML%20file-no%20build-orange) ![GSAP: ScrollTrigger](https://img.shields.io/badge/GSAP-ScrollTrigger-88ce02)

**[Live demo](https://8bsite.github.io/fitness-website-template/)** · **[Use this template](https://github.com/new?template_name=fitness-website-template&template_owner=8bsite)** · **[Download ZIP](https://github.com/8bsite/fitness-website-template/archive/refs/heads/main.zip)** · **[Template page on 8b.com](https://8b.com/templates/arcline/)**

<a href="https://8bsite.github.io/fitness-website-template/"><img src="previews/desktop.png" alt="Fitness website template: first screen on a desktop" width="76.1%"></a> <a href="https://8bsite.github.io/fitness-website-template/"><img src="previews/phone.png" alt="Fitness website template: first screen on a phone" width="21.9%"></a>

<p align="center"><a href="https://8bsite.github.io/fitness-website-template/"><img src="previews/scroll.gif" alt="Fitness website template: scrolling through the first sections" width="40%"></a><br><sub>Scroll animation</sub></p>

## Use it with Claude Code, Cursor or Codex

Download the four files into your project folder (`curl.exe` in Windows PowerShell):

```bash
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/CREDITS.md
```

Then fill in the angle brackets and give your agent this prompt:

```text
Read AGENTS.md, then edit index.html. Turn this template into the site for <my gym, club or coaching business: sports offered, address, opening hours, coaches and qualifications, the weekly schedule with times, membership plans with monthly prices, what a first test costs, how people book>. Replace first the brand name, the three plans, the seven day cards and the four coaches. Keep the section ids and the classes and attributes AGENTS.md lists; the sports collage grid is built for eight tiles; set each display line's --len number to its new character count. Ask me for any missing fact and never invent prices, hours, addresses, qualifications, member results or contacts.
```

In a vibe coding session with Claude Code, Cursor or Codex, start with the facts only the club can supply: plan names, monthly prices and pause terms, class times and rooms, coach names and qualifications, address, opening hours and a booking link. The member quotes, race times, lab equipment list and the claim that every coach holds a degree are invented, so the agent should ask for real ones or delete them. Search for the old name in any letter case, because the wordmark is lower case. Drop the ® signs unless the marks are registered.

No agent? Click **[Use this template](https://github.com/new?template_name=fitness-website-template&template_owner=8bsite)**, edit `index.html` on GitHub and turn on **Settings > Pages**.

## Sections and motion

- **Navigation**: top bar: wordmark, a short tagline, section links, Book a test button; phone menu overlay.
- **Faster than your own shadow**: two-screen opening: a navy cover slide with a photo and a three-line stepped headline, then a pale manifesto slide (demo: racket photo, "Only forward®"). Smooth scrolling throughout. While the cover holds, its headline lines streak off sideways and the slide shrinks and darkens; the next heading streaks in.
- **Tested Monday. Faster by spring**: how it works: three numbered steps beside a big heading with round photos set into its lines (demo: Test, Train, Transfer). Tied to scroll, three round photos roll into gaps in the heading while the words after the first two photos slide into place.
- **Breathe. Move. Repeat.**: a three-word line over a collage of tiles, one per activity, plus a link tile (demo: strength, running, cycling, swimming, gait fitting, court sports). Tied to scroll, the tiles start as a tilted pile in the middle and are dealt out to their places.
- **Coached by people who still race**: four coach portraits of different heights with names and roles. Two rings draw and turn with scroll, and each portrait settles from a slight zoom.
- **What the lab sees**: a feature block: text on the left, a round photo ringed by four labelled measures on the right (demo: test lab, VO₂ max, threshold). Tied to scroll, a round lens opens on the lab photo from a small circle and, on wide screens, four measures swing around it.
- **A week at Arcline**: weekly schedule: seven day cards in a row that runs sideways as you scroll, with a progress line. Pinned, the seven day cards run sideways as you scroll, leaning into faster scrolls, while a progress line fills.
- **Members, retested**: testimonials: one large quote with a round portrait in its first line and two short quotes. The large quote streaks in from the left, its round portrait settles from a slight zoom and the two short quotes rise in.
- **Recovery is part of the rep**: a stepped heading, a lead and four services in two columns, beside a window of sky over calm water (demo: recovery suite). Tied to scroll, a pale sun sinks into the window, the sky fades from navy to pale blue-grey and the water settles.
- **Membership**: pricing: three plans in ruled columns, the middle one highlighted. Rings draw and turn with scroll, the heading streaks in and the three plans rise one after another.
- **Before your first test**: questions and answers (native &lt;details&gt;) beside a rail with a rolling ball. Tied to scroll, a ball rolls down the rail beside the questions, turning as it travels.
- **Book your first test**: booking: a heading on a line across the slide, address, hours, phone, email and a short form (placeholders). Tied to scroll, the heading slides along its line to the right while the line stretches to full width.
- **Footer**: width-filling wordmark, a line about the club, links, socials, copyright and the Design: 8B credit. The width-filling wordmark streaks in from the left, skewed and stretched, as the footer comes into view.

## Design

![#ffffff](https://img.shields.io/badge/-%23ffffff-ffffff?style=flat-square) white slides  
![#0b1019](https://img.shields.io/badge/-%230b1019-0b1019?style=flat-square) text and dark buttons  
![#1a2333](https://img.shields.io/badge/-%231a2333-1a2333?style=flat-square) navy slides  
![#dbe4ec](https://img.shields.io/badge/-%23dbe4ec-dbe4ec?style=flat-square) misty page background  
![#9db1c4](https://img.shields.io/badge/-%239db1c4-9db1c4?style=flat-square) blue-grey mist, rules, rings  
![#536477](https://img.shields.io/badge/-%23536477-536477?style=flat-square) slate secondary text  
![#2f54e0](https://img.shields.io/badge/-%232f54e0-2f54e0?style=flat-square) cobalt blue for keyboard focus rings (white on navy slides) and focused form fields  
![#edf2f6](https://img.shields.io/badge/-%23edf2f6-edf2f6?style=flat-square) pale panels and fields

**Geist**: all text: medium-weight headings set very large with tight negative tracking (Google Fonts). Each section from the opening to the footer is a framed slide with corner crosshairs and a soft shadow, floating on a fixed blue-grey mist crossed by thin circles; in the week section each day card is its own slide. White, navy and pale slides are mixed down the page and step left or right. Photos are desaturated, round photo chips sit inside heading lines and pale spheres act as ornaments.

## Questions

**Does the booking form send anything?**  
No. It requires a name and a valid email, then shows a thank-you line and clears itself, but nothing leaves the page. Connect Formspree or Netlify Forms, or remove the form and keep the email link. AGENTS.md has the steps. The line promising a coach will call within one working day is invented, so edit it too.

**Is this website design for personal trainers or only for gyms?**  
Both. A solo coach can use it as a personal trainer website template: keep the method, schedule, plans and booking, and swap the four coach portraits for one or two, or remove the coaches section with the steps in AGENTS.md. Rename the lab block as an assessment or trial session. The five sports are only demo copy.

**Is the weekly schedule easy to change?**  
Yes. Each day is a plain list item with a session name, a time and place, a short note and a photo. Add or remove cards and the sideways scroll recalculates its length when the page loads or resizes. Each card holds one session, so a long timetable needs another layout or a link to your booking system.

## Is it the right base?

Choose this base when you sell coached training with a structure: an entry test or trial, a block of weeks, a retest and monthly tiers. A venue that sells timed passes, parties and booked slots fits the [indoor activity venue](https://8b.com/templates/hopla/) template better. The weak spot is the schedule. Each of the seven day cards holds one session, so a gym with a dozen classes a day needs another layout or a link to a booking system. The form takes requests only, and the three plan buttons link to the contact section rather than to a checkout.

## Before you publish

- Replace what is marked `data-8b-placeholder` (social preview image, favicon, phone, email, form, social) and the invented demo facts; [AGENTS.md](AGENTS.md) lists them.
- The form sends nothing yet: connect it to Formspree or Netlify Forms, or remove it.

## Tech

GSAP 3.13.0, ScrollTrigger, Lenis 1.3.27 from jsDelivr, 90 KB, no build step. Chrome and Edge 111+, Safari 16.2+, Firefox 113+ (it uses color-mix(), container query units, cascade layers, small/dynamic viewport units). With "reduce motion" on, the page is complete and still.

## License

MIT, see [LICENSE](LICENSE). Photos, fonts and libraries keep their own licences: [CREDITS.md](CREDITS.md). More free templates: [8b.com/templates](https://8b.com/templates/) · [github.com/8bsite](https://github.com/8bsite).
