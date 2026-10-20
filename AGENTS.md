# Arcline — notes for AI coding agents

One HTML file: markup, inline CSS and inline scripts; GSAP with ScrollTrigger, Lenis smooth scroll, all from jsDelivr. No build step, no framework.

## Files
Work from the files: a page read through a link comes back as a summary, and a page rebuilt from it would differ.
```bash
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/fitness-website-template/main/CREDITS.md
```
In Windows PowerShell type `curl.exe`. Publish `index.html` with LICENSE and CREDITS.md; this file, README.md and `previews/` are not part of the site.

## Do not break
- Keep it one file unless the user asks otherwise; no framework or bundler for copy, colour or photo changes.
- Keep the ids and the `data-8b-section` / `data-8b-motion` attributes. Each section has its styles in `<style data-8b-part="section:<id>">` and its animation, if any, in `<script data-8b-part="scene:<id>">`.
- The scripts find these classes and attributes; when you change a section's markup, keep them or update the script:
  - `section-script:navigation`: `.nav__bar` `.nav__menu` `.menu` `.menu__close`
  - `section-script:opening`: `.op-s1`
  - `scene:opening`: `.op-s1` `.op-line--1` `.op-line--2` `.op-line--3` `.op-line` `.op-meta` `.op-photo` `.op-ring` `.op-slide` `.op-dim` `.op-ground` `.op-card` `.op-title2` `.op-orb`
  - `section-script:contact`: `.ct-form` `.ct-status` `data-ok` `data-error`
  - `scene:method`: `.mt-title` `.mt-gap` `.mt-chip` `.mt-after`
  - `scene:disciplines`: `.ds-grid` `.ds-tile`
  - `scene:lab`: `.lb-stage` `.lb-note` `.lb-lens` `.lb-ring`
  - `scene:week`: `.wk-stage` `.wk-view` `.wk-track` `.wk-progress`
  - `scene:recovery`: `.rc-window` `.rc-sun` `.rc-cool` `.rc-sea`
  - `scene:faq`: `.fq-rail` `.fq-ball` `.fq-list` `.fq-item`
  - `scene:contact`: `.ct-run` `.ct-title` `.ct-line`
- Colours, fonts, radii and shadows are CSS variables in the `:root` block (`data-8b-part="tokens"`); change them there and keep body text at 4.5:1 contrast or more.
- Animations run only when the visitor allows motion (`prefers-reduced-motion: no-preference`); the page must stay readable without them.
- A display line with `style="--len:N"` is sized to fill its width: N is its number of characters, spaces included (`Faster than` → 11, `your own` → 8).
- Keep the header comment and `<meta name="generator">`. Keep the "Design: 8B" footer link unless the site owner asks to remove it.

## Replace before publishing
- Everything marked `data-8b-placeholder` (og-image, favicon, phone, email, form, social); remove the attribute once the real value is in. With no real value: no preview image — delete the `og:image` tag and set `twitter:card` to `summary`; no phone, email or address — remove that link or row.
- Book a test buttons in the nav, the phone menu and the first screen, and "Book a lab test" in lab: link to #contact now; point them to your booking page, or keep #contact if the form takes bookings.
- Start Base / Start Build / Start Peak in membership: link to #contact now; point them to the sign-up or checkout URL of each plan.
- **The form sends nothing.** `section-script:contact` checks the fields and shows a thank-you message without sending. Pick one:
  - Formspree: set `action="https://formspree.io/f/<id>"` on the form; in the script, before the thank-you message, `await fetch(form.action, { method: 'POST', body: new FormData(form), headers: { Accept: 'application/json' } })` and show it only if the response is ok.
  - Netlify Forms (site on Netlify): add `name="contact" data-netlify="true"` and `<input type="hidden" name="form-name" value="contact">`; send with `fetch('/', { method: 'POST', headers: { 'Content-Type': 'application/x-www-form-urlencoded' }, body: new URLSearchParams(new FormData(form)) })`.
  - No form service: remove the `<form>` together with the script that handles it (it would fail without the form) and keep the email link.
- Invented demo facts (ask the user for the real ones; do not make up prices, dates or addresses):
  - Prices and plan terms: Base €89, Build €159, Peak €249 a month, "billed monthly, no joining fee, pause any time for injury or travel", the entry test included in every plan, and each plan's four inclusions (three group sessions a week, monthly plan review, a data dashboard and app, a twelve-week coach-written block, unlimited pool, track and courts, a personal coach with a weekly call, physio and the recovery suite) (membership, FAQ "Can I pause my membership?").
  - Retest cycle and test length: "Two hours in the lab", twelve-week blocks adjusted every Sunday, retest every twelve weeks on Base and Build and every eight weeks on Peak, "a report the same day" (method, lab, membership, FAQ).
  - Lab equipment and claims: breath gas, blood lactate, force plates, video at 240 frames a second, a treadmill, bike and swimming flume (lab, FAQ "What happens in the lab test?").
  - Coaches: Daniel Okafor (head coach, running and triathlon), Maya Ferreira (court sports and strength), Tomas Lindqvist (lab lead, cycling), Ines Varga (swimming and mobility), and "Every coach holds a sport-science degree and a current race licence" (coaches, photo alt texts).
  - Member quotes and results: Lena Brandt, half marathon 1:41 to 1:32, "nine minutes faster" after twelve weeks; Samir Haddad, trail runner; Julia Moretti, club tennis (stories).
  - The weekly schedule: session times 06:30, 06:30, 18:00, 07:00, "Any time", 08:00, 10:00, and the places (lab and bike room, outdoor track, gym floor, 25 m pool, recovery suite, from the club, Courts 1–3), "forty easy minutes", "groups of four", "Most members mix three sports in one week" (week).
  - Facilities: the recovery suite (cold plunge at four degrees for three minutes, sauna, weekly physio slots, sleep coaching with daily heart-rate variability), "Bike racks, ten parking spaces and showers with towels" (recovery, FAQ, week).
  - Address and hours: "Harbour Street 1, 1000 Copenhagen" (an invented address that replaced a real-looking one), "Mon–Fri 06:00–21:00, Sat–Sun 07:00–15:00", "Club and lab on the harbour in Copenhagen" (contact, footer).
  - Phone and email (already replaced with +45 00 00 00 00 and lab@arcline.example) and the service promise "A coach will call within one working day" (contact form's data-ok message), "Call the club and a coach will answer" (FAQ).
  - Registered trademark signs: "arcline®" (nav, footer wordmark) and "Only forward®" (opening); remove the ® unless the marks are registered.
  - The five sports and the claims "Most members start from three sessions a week or fewer" (FAQ) and "a coach who has raced it" (disciplines); "© 2026 Arcline Performance Club" (footer); the <title> and meta description.
- `<title>`, the meta description and the og tags; photos (Unsplash, see CREDITS.md) when the user has their own.

## Notes
- The spheres, orbit rings and slide corner marks are CSS and SVG, not images: recolour them through the CSS variables in :root.
- Display lines with style="--len:N" (opening headline, "Only forward®", "Breathe. Move. Repeat.", footer wordmark) fill their width: set N to the new number of characters; a trailing ® counts as one ("arcline®" → 8, "Only forward®" → 13).
- The wordmark is written in lower case ("arcline") in the nav and the footer: a case-sensitive search for "Arcline" misses it.
- Without JavaScript the phone menu button cannot open the overlay; the links stay reachable in the footer.
- On phones the last tiles of the disciplines deck travel to places below the screen, so part of their path is out of view.

## Common edits
- Rebrand: search the old name (`Arcline`) in any letter case and replace every match; change the favicon letter and colours in `<link rel="icon">`.
- Photos: replace `src` and delete `srcset` and `sizes` (they list Unsplash sizes), keep `width`/`height` to the new photo's ratio, update `alt` and CREDITS.md.
- Remove a section: delete its markup, its `section:<id>` and `scene-style:<id>` styles, its `scene:<id>` and `section-script:<id>` scripts, and links to `#<id>`.
- Native scroll instead of smooth scroll: delete the Lenis block in `page-init` and the Lenis `<script>` tag.

## Check and publish
- Open the page at 375 and 1440 px, with reduced motion on, with the console open.
- Search `data-8b-placeholder` and the old name: nothing should be left but class names.
