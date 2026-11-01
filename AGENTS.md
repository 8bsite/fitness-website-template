# AGENTS.md: fitness website template

Website for a fitness or sports training club with coaches, a weekly schedule and membership plans. One file, `index.html`, with inline CSS and scripts, no JavaScript libraries: the scroll motion is CSS scroll-driven animations plus a small inline motion kit; no build step, and none is needed for copy, colour or photo edits. A GSAP build of the same page is `index.gsap.html` (GSAP 3.13.0, ScrollTrigger, Lenis 1.3.27 from jsDelivr): edit one of the two, not both.

## Files
Edit these files, not a page fetched by URL (that arrives as a summary).
```bash
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/CREDITS.md
```
Upload `index.html`, LICENSE and CREDITS.md; not this file, README.md or `previews/`.

## Keep
- Every `id`, `data-8b-section`, `data-8b-motion` and `data-8b-part` (`section:<id>` styles, `scene:<id>` animation).
- The motion parts `motion-gate` (head: sets `data-8b-live` on `<html>` only with scroll-driven animation support and no reduced motion), `motion-kit` and `motion`, and every other `data-8b-*` attribute (`data-8b-items` groups, `data-8b-off`, `data-8b-enter`): the CSS and the kit read them. Items ordered by `--i` follow their group; counts the CSS fixes are listed under Known limits (`data-8b-fixed` marks such a group).
- Selectors the scripts use:
  - `section-script:navigation`: `.nav__bar` `.nav__menu` `.menu` `.menu__close`
  - `section-script:opening`: `.op-s1`
  - `section-script:contact`: `.ct-form` `.ct-status` `data-ok` `data-error`
  - `scene-script:disciplines`: `.ds-grid` `.ds-tile`
  - `scene-script:week`: `.wk-stage` `.wk-view` `.wk-track`
  - `scene-script:faq`: `.fq-rail` `.fq-ball`
  - `scene-script:contact`: `.ct-run` `.ct-title`
- `style="--len:N"` = characters in that display line, spaces included: `Faster than` is 11, `your own` is 8, `shadow` is 6, `Breathe. Move. Repeat.` is 22.
- The scroll scenes (`scene:<id>` styles and `scene-script:<id>` scripts) read these classes, so keep them: opening `.op-s1` `.op-line` `.op-line--1` `.op-line--2` `.op-line--3` `.op-meta` `.op-photo` `.op-ring` `.op-slide` `.op-dim` `.op-ground` `.op-card` `.op-title2` `.op-orb`; method `.mt-gap` `.mt-chip` `.mt-after` inside the three `span` rows of `#method-title`; disciplines `.ds-grid` `.ds-tile`; lab `.lb-stage` `.lb-lens` `.lb-ring` and the `li` items of `.lb-notes`; week `.wk-stage` `.wk-view` `.wk-track` `.wk-progress`; recovery `.rc-window` `.rc-sun` `.rc-cool` `.rc-sea`; faq `.fq-list` `.fq-rail` `.fq-ball`; contact `.ct-run` `.ct-title` `.ct-line`.
- The spheres, orbit rings and slide corner marks are CSS and SVG, not images: recolour them through the CSS variables in :root.
- Display lines with style="--len:N" (opening headline, "Only forward®", "Breathe. Move. Repeat.", footer wordmark) fill their width: set N to the new number of characters; a trailing ® counts as one ("arcline®" is 8, "Only forward®" is 13).
- The wordmark is written in lower case ("arcline") in the nav and the footer: a case-sensitive search for "Arcline" misses it.
- Colours and fonts are variables in `:root` (`data-8b-part="tokens"`): `--color-1` #ffffff (white slides), `--color-2` #0b1019 (text and dark buttons), `--color-3` #1a2333 (navy slides), `--color-4` #dbe4ec (misty page background), `--color-5` #9db1c4 (blue-grey mist, rules, rings), `--color-6` #536477 (slate secondary text), `--color-7` #2f54e0 (cobalt blue for keyboard focus rings (white on navy slides) and focused form fields), `--color-8` #edf2f6 (pale panels and fields); body text needs 4.5:1 contrast.
- With reduced motion the page must read in full.
- Keep the header comment and `<meta name="generator">`. Keep the "Design: 8B" footer link unless the site owner asks to remove it.

## Replace
- `data-8b-placeholder` (og-image, favicon, phone, email, form, social): real value in, attribute out; no value, remove the row (no image: drop `og:image`, set `twitter:card` to `summary`).
- Book a test buttons in the nav, the phone menu and the first screen, and "Book a lab test" in lab: now #contact; owner's target: your booking page, or keep #contact if the form takes bookings.
- Start Base / Start Build / Start Peak in membership: now #contact; owner's target: the sign-up or checkout URL of each plan.
- The form in `#contact` (fields `name`, `email`, `sport`, `goal`) sends nothing; `section-script:contact` handles its submit in the page (read it before you connect a service). Formspree: `action="https://formspree.io/f/<id>"` and `fetch` POST `new FormData(form)` first. Netlify: `data-netlify="true"` and a hidden `form-name`. Or delete it and the script.
- The name Arcline (any letter case); the favicon letter and colours in `<link rel="icon">`.
- Photos (25, Unsplash: opening 2, method 3, disciplines 6, coaches 4, lab 1, week 7, stories 1, recovery 1): `src`, no `srcset`/`sizes`, `width`/`height` to the ratio, `alt`, CREDITS.md.
- `<title>`, meta description, og tags.

## Ask the owner for
All demo text, never to be invented:
- Prices and plan terms: Base €89, Build €159, Peak €249 a month, "billed monthly, no joining fee, pause any time for injury or travel", the entry test included in every plan, and each plan's four inclusions (three group sessions a week, monthly plan review, a data dashboard and app, a twelve-week coach-written block, unlimited pool, track and courts, a personal coach with a weekly call, physio and the recovery suite) (membership, FAQ "Can I pause my membership?").
- Retest cycle and test length: "Two hours in the lab", twelve-week blocks adjusted every Sunday, retest every twelve weeks on Base and Build and every eight weeks on Peak, "a report the same day" (method, lab, membership, FAQ).
- Lab equipment and claims: breath gas, blood lactate, force plates, video at 240 frames a second, a treadmill, bike and swimming flume (lab, FAQ "What happens in the lab test?").
- Coaches: Daniel Okafor (head coach, running and triathlon), Maya Ferreira (court sports and strength), Tomas Lindqvist (lab lead, cycling), Ines Varga (swimming and mobility), and "Every coach holds a sport-science degree and a current race licence" (coaches, photo alt texts).
- Member quotes and results: Lena Brandt, half marathon 1:41 to 1:32, "nine minutes faster" after twelve weeks; Samir Haddad, trail runner; Julia Moretti, club tennis (stories).
- The weekly schedule: session times 06:30, 06:30, 18:00, 07:00, "Any time", 08:00, 10:00, and the places (lab and bike room, outdoor track, gym floor, 25 m pool, recovery suite, from the club, Courts 1-3), "forty easy minutes", "groups of four", "Most members mix three sports in one week" (week).
- Facilities: the recovery suite (cold plunge at four degrees for three minutes, sauna, weekly physio slots, sleep coaching with daily heart-rate variability), "Bike racks, ten parking spaces and showers with towels" (recovery, FAQ, week).
- Address and hours: "Harbour Street 1, 1000 Copenhagen" (an invented address that replaced a real-looking one), "Mon-Fri 06:00-21:00, Sat-Sun 07:00-15:00", "Club and lab on the harbour in Copenhagen" (contact, footer).
- Phone and email (already replaced with +45 00 00 00 00 and lab@arcline.example) and the service promise "A coach will call within one working day" (contact form's data-ok message), "Call the club and a coach will answer" (FAQ).
- Registered trademark signs: "arcline®" (nav, footer wordmark) and "Only forward®" (opening); remove the ® unless the marks are registered.
- The five sports and the claims "Most members start from three sessions a week or fewer" (FAQ) and "a coach who has raced it" (disciplines); "© 2026 Arcline Performance Club" (footer); the <title> and meta description.

## Known limits
- Without JavaScript the phone menu button cannot open the overlay. On phones the footer links only Method, Lab, Week and Membership, and the first screen links Contact, Membership and Method; Sports and FAQ have no other link.
- Without scroll-driven animation support (Firefox today) or with reduced motion on, the page shows its finished layout: the tiles in their collage, the lens open with the four measures in place, and the week as a row that scrolls sideways by hand.
- The method heading moves exactly three rows through CSS :nth-of-type rules, and the slide of the words after the first two photo chips is a fixed share of those words' widths: after new words the motion starts from a slightly different place, and a fourth row would stay still unless the rules get a fourth entry.
- On phones the last tiles of the disciplines deck travel to places below the screen, so part of their path is out of view.

## Check
375 and 1440 px, reduced motion on, a browser without scroll-driven animations (Firefox: the finished static layout), console clean; `data-8b-placeholder` and Arcline left only in class names.
