# Thrilla — Website (thrilla-web)

## Full project context
~/Projects/Thrilla_Handover__Master.md

## Live URL
https://getthrilla.com

## Purpose
Marketing and pre-launch website for Thrilla. Hosts the landing page, privacy policy, and terms of service. Built as static HTML/CSS — no framework, no build step required.

---

## Commands
```bash
# No build step needed — pure HTML/CSS
# Deploy by pushing to main — Cloudflare Pages auto-deploys in ~30 seconds
cd ~/Projects/thrilla-web
git add . && git commit -m "description" && git push origin main
```

## Local preview
Open index.html directly in a browser, or use a simple local server:
```bash
cd ~/Projects/thrilla-web
npx serve .
```

---

## Dev Standards (non-negotiable)
- All colours must match Thrilla brand — background #142C55, orange #FA6400
- No external CSS frameworks — plain CSS only, keep it lightweight
- Must be fully responsive — mobile and desktop
- Every interactive element needs appropriate aria labels
- Colour must never be the sole carrier of meaning
- WCAG AA contrast on all text — check before shipping
- No hardcoded font sizes where dynamic sizing is possible
- No dark patterns, no fake urgency, no manipulative copy

---

## Brand colours
- background: #142C55
- orange (CTAs, accents, links): #FA6400
- textPrimary: #FFFFFF
- textSecondary: rgba(255,255,255,0.80)
- textMuted: rgba(255,255,255,0.50)
- card background: rgba(255,255,255,0.05)
- border: rgba(255,255,255,0.08)
- Thrill tier colours: Heating Up #F5A623 / Scorching #FF6B35 / Thrilla #FA6400

---

## File structure
```
thrilla-web/
├── index.html          ← landing page
├── privacy.html        ← privacy policy (/privacy)
├── terms.html          ← terms of service (/terms)
├── css/
│   └── styles.css      ← shared styles (if extracted)
└── assets/
    └── wordmark.svg    ← Thrilla wordmark (placeholder text until asset ready)
```

---

## Page structure (index.html)
1. **Hero** — "Where Thrill Gets Delivered" / "Electric moments, on time." / iOS + Android buttons (Coming Soon badges)
2. **What is Thrilla** — 2-3 sentence description
3. **How it works** — 3-step flow, text and icons, no app screenshots yet
4. **Sports covered** — AFL, NBA, F1 live + NFL coming soon
5. **Know When We Launch** — Tally waitlist form embedded
6. **Contact** — Tally contact form embedded
7. **Footer** — Twitter/X, Instagram, privacy policy, terms, copyright

---

## Copy (locked — do not change without instruction)

**Hero:**
"Where Thrill Gets Delivered"
Subtext: "Electric moments, on time."

**What is Thrilla:**
"Thrilla is a real-time sports companion built to surface the moments that matter most. It cuts through noise and clutter to highlight only the big moments. The result is instant, high-clarity alerts for the game's most electric moments — delivered instantly."

**How it works:**
- Step 1 — Set Your Thrill Zone: "Choose the sports and moments you care about. Thrilla learns your preferences and focuses your alerts from the start."
- Step 2 — Thrilla Watches. You Don't Have To.: "Thrilla monitors games and tension levels in real time, filtering out everything else."
- Step 3 — You Get the Moment.: "When the stakes rise, you know it. Clean, real-time alerts that deliver only the big moments."

**Sports:**
- AFL: "The last quarter. The margin. The moment. Thrilla knows when an AFL game is about to become unmissable."
- NBA: "Buzzer beaters don't announce themselves. Thrilla does. Get alerted when the fourth quarter gets electric."
- F1: "Gaps close fast. Thrilla tracks the race in real time and tells you when the lead is about to change hands."
- NFL (coming soon): "Sunday just got smarter. NFL alerts are on the way."

**Waitlist section:**
- Heading: "Know When We Launch"
- Subline: "No spam. Just a single notification when Thrilla is live."
- Tally form embed (waitlist form — get embed code from Tally dashboard)

**Contact section:**
- Tally form embed (contact form — get embed code from Tally dashboard)

**Footer:**
- Twitter/X: @GetThrilla
- Instagram: @GetThrilla
- Links: Privacy Policy (/privacy), Terms of Service (/terms)
- Copyright: © 2026 Thrilla. All rights reserved.

---

## Tally forms
Both forms are created and configured in Tally (tally.so) — account: support@getthrilla.com
- Waitlist form: "Know When We Launch" — email field only, notifications to support@getthrilla.com
- Contact form: name + email + message fields, notifications to support@getthrilla.com
- Get embed codes from Tally dashboard before building

---

## Wordmark
Placeholder text "THRILLA" in bold all-caps until SVG asset is ready. When the asset is delivered, replace with <img> tag referencing assets/wordmark.svg.

---

## Deployment — Cloudflare Pages
- Hosting: Cloudflare Pages (free tier)
- Domain: getthrilla.com (registered on Cloudflare)
- Auto-deploys on every push to main branch
- Setup: Cloudflare dashboard → Pages → Connect to Git → select thrilla-web repo → deploy

---

## End of session
Update ~/Projects/Thrilla_Handover__Master.md to reflect any changes:
- File structure changes
- New pages added
- Copy or design changes
- New version entry in Section 34 (Version History)
