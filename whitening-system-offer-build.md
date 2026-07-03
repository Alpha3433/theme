# Whitening System — Offer Build Spec
**Tier copy · PDP flow · Loop + BOGOS configuration**
Prices in AUD. Replace [Brand] throughout.

---

## 0. One correction baked into everything below

PAP+ needs ~10 minutes of contact time to whiten. A "20-second whitening" claim is not chemically credible and would collapse the public Day 1–60 series. The hook is therefore **hands-free**: *"I whiten while I do my makeup."* The 20-second framing belongs to the U-brush series you referenced (a brushing claim) — your adaptation doesn't need to copy the time, only the day-counter format.

---

## 1. Tier selector — verbatim copy

**Selector header:** Pick your plan
**Subline:** Every kit includes the device. Subscribers get it 40% off.

### Card 1 — STARTER KIT (the decoy)
> **Starter Kit** · One-time
> **$69** + $9.95 shipping
> - 1× [Brand] Sonic Whitening Device
> - 1× PAP+ Gel syringe (~3 weeks of sessions)
> - 1× Shade Card
>
> **CTA:** Buy once — $69

No badge, no value math, no free shipping. This card exists to make Card 2 obvious. Do not improve it.

### Card 2 — THE SYSTEM (pre-selected, default)
> 🏷 **MOST POPULAR · SAVE $68 TODAY**
> **The System** · Subscribe
> **$49 today** ~~$117 value~~ · then **$29 every 5 weeks**
> - 1× Sonic Whitening Device — **40% off**
> - 2× PAP+ Gel syringes (double the Starter Kit)
> - 1× Shade Card — free
> - **Free express shipping, always**
> - Refills land every 5 weeks — skip, pause or cancel in 2 clicks
>
> **CTA:** Start my whitening — $49
> **Trust line:** No lock-in. Cancel from your account — no emails, no phone calls.

### Card 3 — 90-DAY TRANSFORMATION
> 🏷 **BEST VALUE**
> **90-Day Transformation** · One-time
> **$109** · free express shipping
> - 1× Sonic Whitening Device
> - 6× PAP+ Gel syringes — the full 90 days
> - Travel case + [Brand] Purple Toothpaste
> - 1× Shade Card
>
> *For the wedding, the reunion, the new-job smile.*
> **CTA:** Go all in — $109

### Under the selector (all tiers)
> ★ **The Shade Card Guarantee** — photograph Day 1. If Day 30 isn't visibly whiter, we refund everything and you keep the device.

This guarantee doubles as content strategy: every customer is now running your series format at home.

### Refill quantity options (inside the subscription)
- 2-syringe pack — **$29** / 5 weeks *(default)*
- 4-syringe pack — **$49** / 5 weeks — "couples pack, save $9"

Note the coherence math: 2 syringes ≈ 5 weeks of daily 10-minute sessions, so the cadence matches real usage. First order ($49, device + 2 syringes) vs refill ($29, 2 syringes) prices the device at an effective $20 — which is what makes the Starter Kit at $69 for *less* gel feel absurd. That's the decoy doing its job.

---

## 2. PDP section flow (mobile-first)

**Section 1 — Gallery.** Slide 1 is a 15-second UGC loop: gel into tray, bite, timer on screen, shade-card tap at the end. Then: device hero shot, what's-in-the-box flat lay, shade card macro, honest before/after, how-to GIF. Video first — this page is where your series traffic lands, so it should look like episode zero.

**Section 2 — Title block + selector.**
- H1: **Visibly whiter teeth by Day 14**
- Sub: Hands-free PAP+ whitening. Ten minutes a day while you get ready — peroxide-free, so no zingers.
- Star rating (only once reviews are real — seed the first 20–30 from launch customers with shade-card photos; never fabricate)
- Tier selector (Section 1 copy above), Card 2 pre-selected
- Sticky add-to-cart bar on scroll (mobile)

**Section 3 — Social proof strip.** Horizontal scroll of UGC stills/clips captioned "Day 6", "Day 19", "Day 33". As the series grows, this section builds itself.

**Section 4 — How it works.**
> **1. Load it.** A ribbon of PAP+ gel in the tray.
> **2. Bite down.** LED on. Hands free.
> **3. Live your life.** Ten minutes while you do your makeup. Rinse. Done.
> *Sunday ritual: tap your teeth on the shade card and watch the number drop.*

**Section 5 — Mechanism ("Why purple? Why PAP+?").** Two-column: peroxide whitens by oxidising through the enamel — effective, but it's why strips sting. PAP+ breaks down stains without free radicals, so you get the lift without the sensitivity. The purple pigment is instant colour-correction on camera; the PAP does the permanent work underneath. Keep it dentist-safe: no "repairs enamel", no therapeutic claims.

**Section 6 — Results timeline.** Day 3: cleaner, smoother feel. Day 7: first shade-card movement for most people. Day 14: someone comments on it. Day 30: side-by-side photo proof. Include "individual results vary" — it protects you and reads honest.

**Section 7 — Comparison table.** [Brand] vs whitening strips vs in-chair ($600+). Rows: monthly cost, sensitivity, hands-free, minutes per day, whitening agent.

**Section 8 — How refills work.** Three icons: *Lands every 5 weeks* / *Skip or pause anytime* / *Cancel in 2 clicks*. Screenshot of the actual Loop portal — showing the cancel button is a conversion asset, not a risk.

**Section 9 — Review wall.** Filterable, photo-first, shade cards prioritised.

**Section 10 — FAQ.** Eight questions: Will it hurt? (PAP+ is peroxide-free — designed for sensitive teeth) · Does it work on veneers/crowns? (No — whitening only works on natural enamel; be upfront, it kills refunds) · How long per session? · When do I see results? · How do I cancel? (2 clicks, account page, no lock-in) · Shipping time? · Is PAP safe? (used in AU cosmetic whitening for years, peroxide-free pathway) · What if it doesn't work? (Shade Card Guarantee).

**Section 11 — Guarantee block + final CTA.** Repeat the Shade Card Guarantee, one button: *Start my whitening — $49*.

**Announcement bar:** Free express shipping on every subscription · Shade Card Guarantee
**Cart drawer line (one-time orders):** You're $X from free shipping →

---

## 3. Build map — Shopify + Loop + BOGOS

### Catalog structure
| SKU | Product | Price | Notes |
|---|---|---|---|
| P1 | Whitening Device | $79 | Anchor price. Hide from collections; exists for value math + post-purchase upsell |
| P2 | PAP+ Gel Refills | $29 (2-pk) / $49 (4-pk) | Variants. Selling plans attached. Standalone anchor: "$19/syringe" |
| P3 | Starter Kit | $69 | One-time bundle SKU (device + 1 syringe + card) |
| P4 | The System | $49 | Subscription-only bundle SKU (device + 2 syringes + card) |
| P5 | 90-Day Transformation | $109 | One-time bundle SKU |
| P6 | Purple Toothpaste | $19 | Retention gift + future AOV ladder |
| P7 | Travel Case | $9 | Order bump |
| P8 | Shade Card | $0 | Packed in every box — not a cart item, keeps cart logic clean |

### Loop Subscriptions
1. **Selling plan group** "Whitening Club": deliver every 5 weeks, attach to P2 and P4.
2. **The core workflow — starter-to-refill swap:** on P4, after order #1, swap the subscription line item to P2 (2-pack, $29). This is Loop's standard starter-kit flow; build it in Workflows/Flows as "after 1st order → replace product."
3. **Order #3 gift:** workflow adds P6 as a $0 one-time line on the 3rd fulfilment. Include a printed card insert: *"A little something for your Day 60."* This lands exactly on the order-2-to-3 churn cliff.
4. **Customer portal:** enable skip, reschedule, quantity swap (2-pack ↔ 4-pack), address change. Do not hide the cancel button.
5. **Cancellation flow** (in order): "Gel piling up?" → offer 8-week cadence → offer pause for 2 cycles → offer 20% off next order → confirm cancel. Each step recovers real revenue; Loop reports save-rate per offer.
6. **Free shipping on all subscription orders** — set via shipping profile for selling-plan orders (or Loop's shipping settings). One-time orders: free over $79. Net effect: Tier 1 pays shipping (extra decoy pressure), Tiers 2 and 3 ship free as promised on the cards.

### BOGOS
- **Free-gift progress bar** in cart for one-time orders: "$X to free shipping → $99 unlocks a free Purple Toothpaste." Pushes Starter Kit buyers toward Tier 3 territory.
- **BXGY rule:** free P6 when one-time cart ≥ $99.
- Keep BOGOS out of subscription logic entirely — gifts on recurring orders are Loop workflows, not BOGOS, or the two apps will fight in the cart.

### Order bump + post-purchase
- **Cart/checkout bump:** P7 travel case at $9 ("protect it — add for $9").
- **Post-purchase one-click upsell** (Shopify's native post-purchase page, or ReConvert/AfterSell if you want more control): *"Add a second device for your partner — 50% off ($39). Your gel subscription already covers you both — just switch your refill to the couples pack."* This is the one place a 4-pack swap sells itself.

### Theme work (the only custom build)
The three-card selector is a theme section, not an app feature. Loop's native widget gives you functional plan radio buttons — launch v1 with that if needed — but the card layout with pre-selection, badges and strike-through pricing is a custom Liquid/JS section wired to variant + selling-plan IDs. It's a contained one-day build.

---

## 4. Retention touchpoints (minimum viable set)
1. **Order confirmation email:** sets the ritual — "Photograph Day 1 against your shade card. Sunday is shade-check day."
2. **Day 10 email/SMS:** "First shade check?" → drives the habit that drives retention.
3. **Pre-renewal SMS, 5 days before each charge,** with a one-tap skip link. Feels anti-revenue; it's the single biggest chargeback and involuntary-churn killer in gel subs.
4. **Refill #3:** free toothpaste + insert (configured above).
5. **Cancel-flow offers** (configured above).

---

## 5. KPI targets
- Tier 2 take rate ≥ **55%** of orders (below that, the decoy isn't working — check card styling/pre-selection)
- Refill retention: order 1→2 ≥ **75%**, order 2→3 ≥ **80%**
- Blended AOV ≥ **$60** (bumps + Tier 3 doing their job)
- Refill LTV target: ~5 refills × $29 ≈ **$145** on top of starter — this is the number that sets your max CAC (~$50–60)

---

## 6. Challenger test (only after ~200 orders baseline)
**"Free device" offer:** $0 device, $39 every 5 weeks, 2-cycle minimum (Loop supports minimum billing cycles). Converts harder, churns harder. Run as an A/B against the standard System card — never as the default until the retention data says so.

---

## 7. Pre-launch checklist
- [ ] 3-week gel efficacy self-test across 3–4 suppliers with shade card — **the whole business rests on this**
- [ ] Claims pass: no therapeutic claims, no "guaranteed X shades", no fake reviews; before/afters real and typical
- [ ] Loop swap workflow tested end-to-end with a real card (order 1 → verify order 2 line item is P2 @ $29)
- [ ] Cancellation flow live before first ad dollar
- [ ] Pixel events: Subscribe vs OneTime purchase split, so ad optimisation favours subscribers
- [ ] Seed reviews from launch cohort with shade-card photos
- [ ] AU 3PL holding 3 months of gel stock (refills must land in days, not weeks — the device can dropship, refills can't)
