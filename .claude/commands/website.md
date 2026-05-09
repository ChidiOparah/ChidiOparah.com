# Chidi Oparah Website

You are helping maintain **chidioparah.com** — Chidi Oparah's personal brand site for his Fractional CTO business, Rvelate™.

## Project overview

- **Domain:** chidioparah.com (GitHub Pages, custom domain via AWS Route 53)
- **Git remote:** github.com:ChidiOparah/Rvelate.git (branch: main)
- **Stack:** Pure static HTML/CSS/JS — no framework, no build step
- **Deploy:** Push to main → GitHub Actions (`.github/workflows/static.yml`) deploys automatically
- **Fonts:** Inter + Space Grotesk (Google Fonts)
- **Booking:** cal.com/rvelate/clarity-call-30
- **Diagnostic:** rvelate.scoreapp.com

## Files

| File | Purpose |
|------|---------|
| `index.html` | Homepage — hero, logos, pain points, about, services, 6E method, why Chidi, certs, testimonials, CTA |
| `chidi-oparah.html` | Full profile — experience timeline, certifications, education, sidebar |
| `contact.html` | Contact form + sidebar cards |
| `chidi-photo.jpg` | Professional portrait (full body, white background) |
| `CNAME` | Contains `chidioparah.com` — do not modify |

## House rules — apply every time, no exceptions

1. **No em dashes** — replace every `—` with a comma, period, or middle dot (`·`). Scan all affected files after any edit.
2. **No full stops after Rvelate** — never write `Rvelate.` as a brand mark (URLs like `rvelate.com` are fine)
3. **Rvelate™** — always include the ™ symbol when Rvelate appears as a brand name (not in URLs, emails, or booking links)
4. **No day rates** — always say "fixed-fee" and "anchored to outcomes". Never "day rates".
5. **"organisations" not "businesses"** — use British spelling, use "tech-led organisations"
6. **Logo text:** Nav and footer logos read `Chidi<span>Oparah</span>` — "Chidi" in black, "Oparah" in accent blue (`var(--accent)`)
7. **Copyright:** `© 2026 Chidi Oparah. All rights reserved.`
8. **Commit and push after every change** — never leave changes uncommitted

## Brand voice

- Direct, confident, zero fluff
- Speaks to: CTOs, CEOs, founders of PE-backed or investor-funded tech businesses, 60-120 engineers
- Core problem: "scaling chaos" → solution: "structural clarity"
- Key phrase: "effort stops being the answer. What you need now is structure."
- Fixed-fee only, embedded not detached, enterprise depth startup speed

## Key copy rules

- Primary hook: "Your technology business is scaling. Your architecture, delivery, and governance aren't keeping pace."
- Services: 2-Week Clarity Audit / 90-Day Transformation Sprint / Fractional CTO Partnership
- Framework: 6E Method™ (Evaluate, Envision, Empower, Equip, Enable, Evolve)
- Credentials to emphasise: SAFe SPC, TOGAF 9, AWS Certified
- Companies: JPMorgan, Mastercard/Vocalink, HSBC, Nokia, Vodafone, GSK, Barclays
- Markets: US · UK · UAE · Canada

## CSS variables (do not change these)

```css
--accent:        #2563eb
--accent-light:  #3b82f6
--accent-faint:  #eff6ff
--gradient:      linear-gradient(135deg, #0f172a 0%, #1e3a5f 60%, #0f172a 100%)
```

## SEO — maintain on every page

- `<link rel="canonical">` — chidioparah.com/{page}
- Open Graph: `og:type`, `og:url`, `og:title`, `og:description`, `og:image`, `og:site_name` = "Chidi Oparah"
- Twitter Cards: `summary_large_image`, title, description, image
- OG image: `https://chidioparah.com/chidi-photo.jpg`
- JSON-LD structured data (Person + ProfessionalService) on index.html only

## Git workflow

```bash
git add <files>
git commit -m "short description\n\nCo-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>"
git push
```

Always stage specific files by name, never `git add .` or `git add -A`.

## Links to include on the site

- Book a call: https://cal.com/rvelate/clarity-call-30
- Diagnostic: https://rvelate.scoreapp.com
- LinkedIn: https://linkedin.com/in/chidioparah
- Substack: https://substack.com/@chidioparah
- Email: Chidi@rvelate.com

## Self-update instructions — run at the end of every task

After completing any task, check whether this skill file needs updating before committing. Update it if any of the following changed:

| What changed | What to update in this file |
|---|---|
| New HTML page created | Add row to the Files table |
| New link added to the site | Add to Links section |
| New house rule established (e.g. new formatting rule) | Add to House rules |
| A convention was removed or changed | Edit the relevant section |
| New CSS variable introduced | Add to CSS variables block |
| New section type added to a page | Update the Files table description for that page |
| Booking/diagnostic/social URL changed | Update Project overview and Links |

**How to update:**
1. Edit `.claude/commands/website.md` with the relevant change
2. Stage and commit it in the same commit as the site changes — not a separate commit
3. Use the message format: `Update /website skill: <what changed>`

If nothing in the skill needs updating, skip this step silently.
