---
name: jawsai-supersite
description: >
  Build a JAWSAI911 Shark SuperSite for a real local-service client: a
  conversion landing page that is 100% client-branded, grounded in researched
  facts, and wired to the two biggest operator leaks in that vertical (almost
  always missed first contact + quotes that go cold). Use whenever the ask is
  a company site, client site, SuperSite, local business landing page,
  service-business website, or "build a site for [business]". Canonical
  system: Pressure Cleaning Fort Lauderdale / Pressure Clean LLC. Second
  SuperSite: Affordable Pressure Cleaning LLC (Dania Beach) — clone the
  system, never the paint. Pair with design-ui and og. Auth and database
  stay OFF unless the client asked for accounts.
metadata:
  short-description: "JAWSAI911 client SuperSite: research, two leaks, converting local-service landing"
user-invocable: true
---

# JAWSAI911 Shark SuperSite

A SuperSite is **not a brochure**. It is the public face of the client plus
the desk that catches the job when the crew cannot pick up.

This file is the whole skill. Do not look for a references folder.

**Always also load** `design-ui` (tokens, anti-slop, photography) and dispatch
the `og` brand-asset pass once the name and palette settle. Do not wait on it.

---

## 0. Who this site is for

| Role | Example | Rule |
| --- | --- | --- |
| **Agency** | JAWSAI911 · [jawsai911.com](https://jawsai911.com) | Ghosted hero lockup + footer sentence on **every** landing page. Never a second brand. |
| **Client** | Pressure Clean LLC · Affordable Pressure Cleaning LLC | The site is *their* brand, *their* phone, *their* city. |

If the user says “my company is X and Y is my client,” Y owns the page. X
gets a **ghosted Shark SuperSite lockup** at the top of the hero (translucent, not a banner) plus `{product} by {agency}` in the footer, both linking out. Clone `src/components/agency-mark.tsx` as-is (§7). Do not skip it.

**Clone the system, never the paint.**

| Client | City | What to copy | What not to copy |
| --- | --- | --- | --- |
| Pressure Clean LLC | Fort Lauderdale | Anatomy, leaks, desk, file map | Headline, teal/navy, prices |
| Affordable Pressure Cleaning LLC | Dania Beach | Same system + ghosted agency mark | Olive/charcoal, Oswald, $149/$429/$779 |

---

## 1. Build sequence (do not skip)

1. **Triage.** Client marketing site → auth OFF, database OFF, leads in `localStorage` until a real Command Agent backend is wired.
2. **Ground the client.** Search the real business. Capture legal name, DBA, phone, SMS, address, hours, rating, review count, real quotes, service area, mission. Invent nothing you can verify. Fake testimonials are a last resort and must read like the market, never like lorem.
3. **Research the vertical.** Find the **two biggest operator leaks** for *this* trade in *this* kind of market. Numbers required. Default pair:
   - **Leak 01 — missed first contact** (on the job / after hours / voicemail) → **Site Agent**
   - **Leak 02 — quotes that die after one touch** → **Command Agent**
4. **Translate leaks for the buyer.** The homeowner lives the symptom (“they don’t pick up”), not the P&L. Put leak + desk fix on the page as a two-card section.
5. **Name the palette and type.** Unique to the trade and place. Pressure Clean used Atlantic navy + sand + water teal + Barlow Condensed / Outfit. Affordable used charcoal + limestone + olive + Oswald / Figtree. The next client does **not** get either skin unless they are that shop.
6. **Dispatch the og brand pass.** Then keep building.
7. **Generate real photography** of *their* work in *their* city. No gray boxes, no emoji-as-icon, no stock-looking interiors.
8. **Implement the anatomy** (§5). Clone `agency-mark.tsx` onto the hero — every landing page, no exceptions.
9. **Wire one pipeline.** Quote form, desk chat, and email signup all `saveLead()`. Click-to-call + SMS on every conversion surface.
10. **Verify.** Desktop + mobile smoke, form submit, chat open, no horizontal overflow, Grok pill not covering the mobile CTA. Confirm the Shark SuperSite lockup is visible (translucent, top-right of the hero) on both viewports.

---

## 2. Double stack (always both)

```
Site Agent     = what the buyer sees and can do at 11pm
Command Agent  = what happens to the lead after it lands
```

| Layer | On the SuperSite | Do not ship without |
| --- | --- | --- |
| **Site Agent** | Sticky phone, quote form, SMS, 24/7 desk chat, click-to-call, mobile CTA bar | A path that works when nobody answers the truck phone |
| **Command Agent** | Shared `saveLead()` pipeline, visible follow-up timeline (now / same day / 24h / 72h), seasonal rebook list, review promise in FAQ | Copy that says the quote will be followed, plus a timeline the buyer can see |

If you only ship pretty sections, you built a brochure. If you only ship a form, you hid the desk. Both.

---

## 3. Research the vertical, then pick two leaks

Do this **before** writing hero copy. The SuperSite exists to close the leaks
you find here — not to decorate a service list.

### Ground the client (30–60 minutes of search, not memory)

Search `{business name}` `{city}` and the legal entity. Capture:

- Legal name + DBA / how they answer the phone
- Phone, whether SMS is plausible (almost always yes for trades)
- Address, service area, hours
- Rating + review count + **verbatim quotes** (grammar-clean, don’t invent praise)
- Mission / about blurb in their own words
- What they actually sell (house wash vs roof vs commercial — don’t guess)

If two listings disagree (address, phone), prefer Chamber / the number on
more than one source, and don’t put a second conflicting address on the page.

### Research operator pain for *this* trade

Search like an owner, not a designer:

- `{trade} missed calls` `{trade} leads don’t book` `{trade} follow up quotes`
- `{trade} stuck at $100k` `{trade} no-shows` `{trade} after hours leads`
- Home-service stats if the trade is thin: first-to-respond, voicemail hangup rate

You want **numbers** (even if they are industry-typical, cite the claim in
internal copy only — the public page uses rounded plain language).

Rank by **revenue leaked per week on a small crew**, not by blog-post volume.

| Rank | Leak | Why it usually wins |
| --- | --- | --- |
| 1 | Missed first contact | Hands full, 80% who hit voicemail never leave a message, 35–40% of inquiries after hours, first shop to answer wins |
| 2 | Quotes that go cold | 2–5 follow-ups to book; 24h follow-up converts 35–45% more; 40–60% of open quotes die from silence |
| Runner-up | No rebook / review engine | Happy jobs evaporate; map pack starves |
| Runner-up | Owner still on every hat | Real, but a SuperSite does not hire their first tech |
| Runner-up | Underpricing | Real, but a landing page is the wrong tool |

**Default for almost every home-service SuperSite:** leaks 1 and 2.
Replace a default only when research for *this* trade is clearly different
(e.g. a clinic’s #1 is no-show / intake; a shop’s #1 is after-hours DMs).

| Leak | JAWSAI911 layer | What must exist on the page |
| --- | --- | --- |
| They don’t pick up | **Site Agent** | Quote form, click-to-call, SMS, 24/7 desk chat, mobile CTA, shared `saveLead()` — “leave it here, it still hits the desk” |
| They quote once and go silent | **Command Agent** | Visible timeline (now / same day / 24h / 72h), pipeline language, seasonal list, review/rebook promise in FAQ |

Operator version (internal, sales deck):

> Missing 1 in 3 calls costs $3k–$10k a month in peak season.

Buyer version (on the client site):

> The wand is in both hands. You hit voicemail. Most people hang up and dial the next listing. Leave it here — the desk still catches you.

Rules: symptom first, system second; one concrete action per leak card; do not lecture the buyer about the owner’s P&L; do not name “CRM” or “automation stack” — say **desk**, **pipeline**, **check-in**; two cards only. A third leak becomes FAQ or why-us, not another band.

If you cannot answer “what does the homeowner do at 9pm when the truck is parked?” the Site Agent is unfinished. If you cannot answer “what happens to my quote tomorrow if I don’t reply?” the Command Agent is unfinished.

---

## 4. Copy and design rules

- **One city, one trade, one voice.** Place-specific (salt air, canal spray, neighborhoods) beats generic “quality you can trust.”
- **Display + body.** Condensed uppercase for titles is the SuperSite register. ≤ 2 families. ≤ 5 colors. Tokens in `@theme` — no hex in JSX.
- **Photography is the product.** Hero is a full-bleed job photo with a dark wash, not a gradient blob. Service grid is photos with overlay titles, not icon circles.
- **Proof before pitch.** Real rating, real address, real reviews, real starting prices.
- **CTAs everywhere.** Hero, header, mobile bar, leak cards, pricing, quote. Dual CTA: quote + phone.
- **No emoji. No purple SaaS. No Inter-on-white template.** Follow `design-ui`.
- **Agency credit is required chrome on every landing page.** Clone `agency-mark.tsx`. Smoked-glass lockup, top-right of the hero (fin + “Shark SuperSite” + JAWSAI911), plus `{product} by {agency}` in the footer. Same tokens as the client — no electric-blue plate, no product-overview slide.

---

## 5. Page anatomy

Required order. Rename labels to the trade; do not drop a band.

Sticky **header** (always on): mark + wordmark, in-page anchors, phone, Get a quote.
Smooth scroll + `scroll-padding-top` for the sticky bar.

| # | Band | Anchor | Job |
| --- | --- | --- | --- |
| 1 | **Hero** | `#top` | Place-specific headline over a real job photo. Dual CTA: quote + phone. One line for the first leak (“Crew on a roof? Chat or text the desk”). **Required:** ghosted **Shark SuperSite / JAWSAI911** lockup top-right (`AgencyMark`) — smoked glass, client tokens, links out. Every landing page. |
| 2 | **Trust bar** | — | 4 facts: rating, crew/size, licensed, speed. Dark strip. No icons-as-decoration without a label. |
| 3 | **The two leaks** | `#desk` | Two split cards. Left = the leak (buyer voice). Right = the desk (Site Agent then Command Agent). CTAs: open chat / SMS on 01, jump to quote on 02. Quiet SuperSite credit under the grid. |
| 4 | **Services** | `#services` | Photo cards, not icon grid. 4–6 real surfaces. Overlay title + one sentence. |
| 5 | **Why us** | — | 4 points that are *this* crew in *this* climate. Dark band is fine. |
| 6 | **Before / after** | `#results` | Interactive slider. Same angle. Buyer can drag the line. CTA to quote that job type. |
| 7 | **Pricing** | `#pricing` | Three starting tiers. Middle featured. “From $X”. Each card CTAs to `#quote`. No bait, no “contact for price” as the only number. |
| 8 | **Reviews** | `#reviews` | 3–4 quotes. Initials + neighborhood, not fake headshots. Real quotes first. |
| 9 | **Quote + list** | `#quote` | Full quote form (name, phone, email, service, neighborhood, notes). Phone + SMS. **Follow-up timeline** beside or under the pitch. Seasonal email list (rebook engine, not a newsletter). Success states. |
| 10 | **FAQ** | — | Include the two leak questions first, then trade questions (method, plants, area, licensed). |
| 11 | **Footer** | — | Legal name, DBA, phone, address, hours, service-area line, nav, ©, **Shark SuperSite by JAWSAI911**. |
| 12 | **Mobile CTA** | — | Fixed Call + Free quote. Inset so it does not sit under the Grok pill (`pl-32` + bottom offset on small screens). |
| 13 | **Desk chat** | — | Fixed launcher. Short form: name, phone, what they need. Same `saveLead({ source: "chat" })`. Openable from leak-card buttons via a window event. |

Conversion: one primary action per view (**get a quote**); phone is the always-on second. Every pricing card, leak card, and hero points at `#quote` or the phone. Forms store to one pipeline and show a human success line (“In the pipeline. We’ll call or text a range.”) — not a toast that vanishes. Follow-up timeline is part of the quote band, not a hidden FAQ.

Chrome: sticky navy (or the client’s dark) header; sand/ink page; one accent for primary buttons; `font-display` for titles, `font-sans` for body; tap targets ≥ 44px; chat sits above the mobile CTA (`bottom-24` on small screens).

---

## 6. Data shape

All client copy lives in **one module** (`src/lib/company.ts`):

- `COMPANY` — name, dba, phone, tel/sms hrefs, address, hours, rating
- `AGENCY` — name + href + product (`Shark SuperSite`) — **same on every client**
- `NAV`, `SERVICES`, `TIERS`, `TESTIMONIALS`, `FAQS`, `SERVICE_AREAS`
- `DESK_LEAKS` — exactly two: pain title/body + agent + solution title/body

```ts
export const AGENCY = {
  name: "JAWSAI911",
  href: "https://jawsai911.com",
  product: "Shark SuperSite",
} as const;

// DESK_LEAKS shape — keep this object. Exactly two entries.
{
  num: "01",
  agent: "Site Agent",          // or Command Agent
  painTitle: "They don’t pick up.",
  pain: "…buyer-facing, with one hard number…",
  solutionTitle: "We still catch you.",
  solution: "…what they can do on this page, tonight…",
}
```

Leads (`src/lib/leads.ts`): one localStorage key from *their* slug (`pcfl-leads`, `apc-leads`), sources `quote | chat | signup`.
Desk chat open event (`src/lib/desk.ts`): `OPEN_DESK_CHAT` + `openDeskChat()`.

---

## 7. Agency mark (required on every landing page)

System chrome, not client paint. Clone as-is. Do not skip. Do not redesign. Do
not turn it into a banner, a top bar, or a product-overview slide.

Smoked-glass lockup in the **top-right of the hero**, under the sticky header,
linking to [jawsai911.com](https://jawsai911.com):

- primary-token hairline (left)
- shark fin mark
- **SHARK SUPERSITE**
- **JAWSAI911**
- faint shark silhouette in the photo (non-interactive, ~10% opacity)

Plus the footer sentence: `{AGENCY.product} by {AGENCY.name}` →
**Shark SuperSite by JAWSAI911**.

Why ghosted: the page belongs to the client. Readable enough that a visitor
knows JAWSAI911 built it; quiet enough that it does not compete with the
headline, phone, or quote CTA.

- `bg-navy/35` + `backdrop-blur-sm` + `shadow-on-navy` — see-through plate
- type at `text-navy-foreground/70` (hover `/90`)
- **same tokens as the client** (`navy`, `navy-foreground`, `primary`) so it
  blends on every palette. Never introduce electric blue or a second font.

Placement: inside the hero (`relative isolate`, `overflow-hidden`), absolutely
`right-3 top-4` (desktop `right-5 top-5`). Not in the sticky header.

Hard no: do not omit because “the footer already credits us”; do not paste the
JAWSAI911 presentation slide, logo PNG, or rainbow bar; do not make the hero
about JAWSAI911; do not restyle per client beyond the existing tokens.

```tsx
import { AGENCY } from "@/lib/company";

/** Required on every JAWSAI911 SuperSite. Clone as-is; restyle only via tokens. */

function FinMark({ className }: { className?: string }) {
  return (
    <svg viewBox="0 0 32 32" className={className} fill="none" aria-hidden>
      <path
        d="M5 28c6-9 9-18 11.5-25 2.2 8 7.5 16 12.5 25-8-2-16-2-24 0Z"
        fill="currentColor"
      />
      <path
        d="M10 22h8M12.5 17.5 17 11l5 3.5"
        stroke="currentColor"
        strokeWidth="1.2"
        strokeLinecap="round"
        strokeLinejoin="round"
        opacity="0.42"
      />
    </svg>
  );
}

function SharkGhost({ className }: { className?: string }) {
  return (
    <svg viewBox="0 0 160 56" className={className} fill="currentColor" aria-hidden>
      <path d="M6 32c10-9 28-14 52-12 18 1.5 36 5 50-3l16-8-10 12 20 4-20 3 10 12-16-7c-14 8-32 10-50 8-20-2-36-3-46-8-4-2-8-6-8-7 6 .5 12 1.5 16 2.5C16 28 10 27 6 32Z" />
      <path d="M62 20 74 4l10 14c-7 1-14 2-22 2Z" />
      <path d="M54 34 48 48l16-11Z" />
    </svg>
  );
}

export function AgencyMark() {
  return (
    <>
      <SharkGhost className="pointer-events-none absolute -right-6 top-8 w-56 text-navy-foreground opacity-10 sm:top-10 sm:w-80" />
      <a
        href={AGENCY.href}
        target="_blank"
        rel="noreferrer"
        aria-label={`${AGENCY.product} by ${AGENCY.name}`}
        className="absolute right-3 top-4 z-10 flex min-h-11 items-center gap-2.5 rounded-lg bg-navy/35 px-3 py-1.5 text-navy-foreground/70 shadow-on-navy backdrop-blur-sm transition-colors duration-200 hover:bg-navy/50 hover:text-navy-foreground/90 sm:right-5 sm:top-5"
      >
        <span className="h-8 w-px rounded-full bg-primary/55" aria-hidden />
        <FinMark className="size-8 shrink-0" />
        <span className="leading-none">
          <span className="block font-display text-xs uppercase tracking-[0.2em]">
            {AGENCY.product}
          </span>
          <span className="mt-1 block text-xs uppercase tracking-[0.18em] text-navy-foreground/55">
            {AGENCY.name}
          </span>
        </span>
      </a>
    </>
  );
}
```

---

## 8. File map

Copy **structure, data shape, and leak pattern**. Do **not** copy headlines,
tokens, or prices onto the next client.

| Path | Owns |
| --- | --- |
| `src/lib/company.ts` | All copy: COMPANY, AGENCY, NAV, SERVICES, TIERS, TESTIMONIALS, FAQS, SERVICE_AREAS, DESK_LEAKS |
| `src/lib/leads.ts` | `saveLead` / `readLeads` — one localStorage key, sources `quote \| chat \| signup` |
| `src/lib/desk.ts` | `OPEN_DESK_CHAT` event + `openDeskChat()` |
| `src/lib/utils.ts` | `cn()` |
| `src/styles.css` | `@theme` tokens, display type, shadows, reduced motion, hero stagger |
| `src/routes/index.tsx` | Section composition only |
| `src/routes/__root.tsx` | Title, description, theme-color, fonts, favicon link |
| `src/components/site-header.tsx` | Sticky nav |
| `src/components/agency-mark.tsx` | **Clone as-is.** Ghosted Shark SuperSite lockup — every landing page |
| `src/components/hero.tsx` | Photo hero + dual CTA + desk hint + `<AgencyMark />` |
| `src/components/trust-bar.tsx` | Four facts |
| `src/components/response-system.tsx` | The two leaks |
| `src/components/services.tsx` | Photo grid |
| `src/components/why-us.tsx` | Four reasons |
| `src/components/before-after.tsx` | Range-input slider |
| `src/components/pricing.tsx` | Three tiers, middle featured |
| `src/components/testimonials.tsx` | Quotes |
| `src/components/quote-form.tsx` | Quote + timeline + email list |
| `src/components/faq.tsx` | Details/summary |
| `src/components/site-footer.tsx` | Contact + SuperSite credit |
| `src/components/mobile-cta.tsx` | Call + quote |
| `src/components/site-chat.tsx` | Desk chat |
| `src/components/ui/*` | Button, input, label, textarea |
| `public/images/` | hero, house, driveway, roof, pavers, commercial, before, after |

Photography: photoreal job photos **in their city**, technicians from behind or
mid-distance, no readable competitor signage, no watermarks. Hero 16:9; one
image per service; before (stained) → image-to-image after (same camera).

---

## 9. Worked SuperSites

Proof that the **system** transfers and the **paint** does not. Next client:
new city, new tokens, new photography, new prices, same anatomy.

### Pressure Clean LLC — Fort Lauderdale

- Phone `(954) 744-6542` · 3805 SW 53rd Pl
- Headline: **The home you bought is still under there.**
- Tokens: sand `#F4EFE6` / ink `#102030` / water teal `#1B6E6C` / navy `#0B1C2C`
- Type: Barlow Condensed + Outfit
- Tiers from `$189` / `$449` featured / `$799`
- Lead key: `pcfl-leads`

### Affordable Pressure Cleaning LLC — Dania Beach

- Gunnar M. · `(954) 729-0590` · 317 SE 4th Ter · 7 AM–7 PM seven days
- Headline: **Fair price. Clean work. That’s it.**
- Tokens: limestone `#ECEAE4` / ink `#1A1814` / olive `#2F5D50` / charcoal `#161412`
- Type: Oswald + Figtree
- Tiers from `$149` / `$429` featured / `$779`
- Lead key: `apc-leads`

What stayed identical: anatomy, two leaks, Site Agent + Command Agent,
`saveLead()` from quote / chat / signup, follow-up timeline, sticky nav,
mobile CTA (`pl-32`), desk chat, footer **Shark SuperSite by JAWSAI911**,
agency mark on the hero, auth off, database off.

---

## 10. Hard no

- Do not make the page about JAWSAI911, Medicare, or dealerships because those are other Jaws products. The **stack** transfers; the **vertical** is researched fresh.
- Do not reuse Pressure Clean headlines, prices, or teal/navy unless this *is* that client. Do not reuse Affordable’s olive/charcoal or “Fair price. Clean work.” unless this *is* that client.
- Do not skip leak research because “every business needs leads.”
- Do not add auth or a database for a quote form.
- Do not ship lorem, fake star widgets, or placeholder images.
- Do not ship a SuperSite without the ghosted Shark SuperSite lockup on the hero. Footer credit is not a substitute.

---

## Finish checklist

- [ ] Real client facts (phone, address, hours, at least two real or clearly local quotes)
- [ ] Two vertical leaks researched with numbers, rewritten for the buyer, mapped to Site Agent / Command Agent
- [ ] Section anatomy complete
- [ ] One lead pipeline from quote + chat + signup
- [ ] Follow-up timeline visible on the quote section
- [ ] Sticky nav, smooth anchors, mobile CTA, desk chat
- [ ] Ghosted JAWSAI911 Shark SuperSite lockup cloned onto the hero (every landing page)
- [ ] Footer: Shark SuperSite by JAWSAI911
- [ ] Unique tokens + photography; `design-ui` + `og` honored
- [ ] Desktop + mobile render check, forms actually submit
