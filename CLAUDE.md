# CLAUDE.md — [Brand] PAP+ Whitening System · Shopify theme build

## What this project is
Shopify storefront for a subscription-first teeth-whitening business (AU market, AUD pricing).
Razor-and-blades model: U-shaped LED whitening device (acquisition anchor) + PAP+ gel syringes (recurring refill revenue).
Base theme: **Elixir "LUVEA"** template (LED skincare device template), added to the store from the Elixir library and pulled into this repo.

**Source of truth for all copy, offer structure, and app config: `whitening-system-offer-build.md` in this repo. Do not invent copy or claims — pull verbatim from that doc.**

## Offer structure (summary — full detail in spec §1)
- **Tier 1 — Starter Kit:** $69 one-time. Device + 1 syringe + shade card. Decoy; do not improve it.
- **Tier 2 — The System:** $49 first order (device + 2 syringes + shade card), then $29 every 5 weeks (2-syringe refill). Pre-selected default, "Most Popular". Subscription via Loop.
- **Tier 3 — 90-Day Transformation:** $109 one-time. Device + 6 syringes + travel case + purple toothpaste.
- Shade Card Guarantee messaging appears under selector and in guarantee block.

## Tech stack & constraints
- Shopify Online Store 2.0 theme (Liquid + JSON templates). Local dev via Shopify CLI (`shopify theme dev`).
- **Loop Subscriptions** owns all recurring logic: selling plans (5-week cadence) on refill + System products, starter→refill swap workflow after order 1, order-3 free gift, cancellation flow. Theme must not duplicate any of this.
- **BOGOS** handles one-time cart gifts/progress bar only. Never let BOGOS touch subscription line items.
- **Critical wiring:** the tier selector must submit a `selling_plan` ID when Tier 2 is selected so Loop attaches the subscription. Tiers 1 and 3 submit as one-time. QA = System tier click → cart line shows selling plan → test order → order 2 renders as $29 refill.
- Catalog SKUs P1–P8 defined in spec §3. Product/variant IDs to be filled in once created in Shopify admin.

## Build tasks (priority order)
1. Map LUVEA's existing sections against the PDP flow in spec §2 → produce keep / kill / reorder list before writing code.
2. Tier selector: adapt Elixir's quantity/accordion selector section (or build custom) into three radio cards per spec §1 — Card 2 pre-selected, badges, strike-through value, per-card CTA copy. Wire per constraint above.
3. Integrate or restyle the Loop plan widget so it doesn't visually duplicate the selector.
4. PDP sections: mechanism block ("Why purple? Why PAP+?"), results timeline, comparison table, refill explainer with Loop portal screenshot, FAQ (8 Qs in spec §2), guarantee block.
5. Mobile: sticky add-to-cart bar, cards stack with Tier 2 visually dominant.
6. Announcement bar + cart drawer copy from spec §2.
7. Run pre-launch checklist, spec §7.

## Conventions & guardrails
- AUD currency, en-AU spelling, mobile-first (traffic is Instagram series → PDP).
- Claims discipline: hands-free positioning only. **No "20-second whitening" claims** (PAP+ needs ~10 min contact time), no therapeutic claims, no "guaranteed shades", no fake reviews or countdown timers.
- Keep edits theme-native (sections/blocks/settings schema) so the store owner can tweak copy in the customizer without code.
