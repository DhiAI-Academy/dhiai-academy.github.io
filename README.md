# DhiAI Academy — website

The company website for **DhiAI Academy**, served by GitHub Pages at **https://dhiai-academy.github.io**.

Plain HTML, CSS and a little JavaScript. There is no build step: GitHub Pages serves exactly what's in this repository.

```
index.html          Home
programmes.html     Beginner & Advanced, day by day
schools.html        For schools
about.html          Story, beliefs, founders
contact.html        Enquiry options + numbered FAQ
404.html            Not-found page
css/site.css        All styles (brand tokens at the top)
js/site.js          Mobile menu, scroll reveal (site works without it)
assets/logo/        Official logo files from the brand kit
assets/img/         Icons, pattern, share image (og-image.png)
assets/fonts/       Self-hosted Manrope, Inter, JetBrains Mono, Noto Sans Devanagari (धी only) — SIL OFL
.nojekyll           Tells GitHub Pages to serve files as-is
```

> **Current address:** the site is live at `koundinya-nvss.github.io/dhiai-academy.github.io/` while the `dhiai-academy` organisation is set up. All absolute links (canonical URLs, share image, 404 page, app icons, sitemap) already point to `https://dhiai-academy.github.io`, so they will work once the site moves. Until then, link previews and the 404 page won't display correctly at the current address.

## 1. Publish on GitHub Pages (one-time, ~5 minutes)

A site at `dhiai-academy.github.io` must live in a repository named **`dhiai-academy.github.io`**, owned by a GitHub account or organisation named **`dhiai-academy`**.

1. Create a free GitHub organisation called `dhiai-academy` (github.com → your avatar → *Your organizations* → *New organization* → Free). Add co-founders as owners.
2. In that organisation, create a **public** repository named exactly `dhiai-academy.github.io`.
3. Upload the contents of this folder (not the folder itself) to the repository root:
   ```bash
   cd dhiai-academy.github.io
   git init -b main
   git add .
   git commit -m "Launch DhiAI Academy website"
   git remote add origin https://github.com/dhiai-academy/dhiai-academy.github.io.git
   git push -u origin main
   ```
4. Repository → *Settings* → *Pages* → *Build and deployment*: Source **Deploy from a branch**, Branch **main**, folder **/ (root)** → Save.
5. After a minute or two the site is live at https://dhiai-academy.github.io. Tick *Enforce HTTPS* on the same page.

## 2. Fill in the placeholders (before sharing the link)

Use find-and-replace across all `.html` files.

| Find | Replace with | Where |
|---|---|---|
| `910000000000` | WhatsApp number: country code + number, digits only (e.g. `919876543210`) | Footer, Contact |
| `+91 00000 00000` | The same number, formatted for display | Contact |

Already filled in: enquiry form `https://forms.gle/y132yC91gApkvvTc7` and support email `dhiai.support@gmail.com`.

**Instructor photo (optional):** in `about.html`, replace `<div class="mono-av mono-av--lg" aria-hidden="true">KN</div>` with
`<img class="mono-av--lg" src="assets/img/koundinya.jpg" alt="Koundinya N. V. S. S." width="104" height="104">` (square photo, at least 208×208 px).

### Suggested Google Form

Create it at forms.google.com from the account you'll both check, then link it to a Google Sheet (*Responses → Link to Sheets*) and share the sheet with Rohit.

1. **I am a…** — Parent / Student / School / Other (multiple choice, required)
2. **Your name** (required)
3. **Phone or WhatsApp number** (required)
4. **Email** (optional)
5. **Student's class** — 10 / 11 / 12 / Not applicable
6. **Board** — CBSE / ICSE–ISC / Cambridge IGCSE–A Level / IB / Other
7. **Interested in** — Beginner / Advanced / Not sure yet / School partnership (checkboxes)
8. **School name** (optional)
9. **Your question** (paragraph)
10. **Consent** (required checkbox): *"I am 18 or over (or a parent or guardian), and I agree that DhiAI Academy may use these details to reply to this enquiry."*

The site tells under-18s to ask a parent to send the enquiry, and says details are used only to reply. Keep the form consistent with that.

## 3. Later: your own domain

When you buy a domain (e.g. `dhiai.academy`): add a file named `CNAME` containing just the domain, set the DNS records GitHub shows under *Settings → Pages → Custom domain*, then find-and-replace `https://dhiai-academy.github.io` with the new address (canonical links, share tags, `sitemap.xml`, `robots.txt`).

## Editing notes

- **Brand rules live in the DhiAI Brand Guidelines.** Colours are CSS variables at the top of `css/site.css`. Use the logo files in `assets/logo/` and never retype the wordmark.
- **The single-line logo here has a corrected frame.** The brand kit's `dhiai-logo-singleline-*.svg` cuts off the descender of the "y" in "Academy" (its viewBox is 202 units tall). This copy uses a 220-unit-tall viewBox. Update the kit's copy too.
- **Copy voice:** no hype words, no promises you can't measure, sentence-case headings. See §8 of the guidelines.
- **Photos:** add real photos of students building once you have them (with written parental consent for any minor shown). The guidelines rule out stock imagery and AI-generated people.
