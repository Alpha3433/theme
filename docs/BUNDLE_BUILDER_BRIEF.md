# Task: Integrate the FÜM-style bundle builder into this theme

## Context (read first)

We reverse-engineered FÜM's "Journey Pack" page (tryfum.com.au/products/journey-pack)
from a HAR capture and their product JSON. Findings:

- It is **one native Shopify product**, no bundle app on the storefront.
- Product options are the builder steps: Option 1 = Device (3 values),
  Option 2 = Pack (6 values), Option 3 = Accessories (5 values) → **90 variants**,
  each pre-priced. Their theme re-renders via the Section Rendering API
  (`?section_id=...&option_values=...`) on each tile click.
- Subscription is baked into option values: "(Cores Club)" values are priced
  **9.75% below** the one-time value with `compare_at_price` = one-time price
  (that's the strikethrough). At add-to-cart a **selling plan** is attached
  (Loop Subscriptions; first delivery at shown price, then 30% off recurring,
  deliver every 1/2/3 months).
- Verified price behaviour to match pixel-for-pixel: with nothing selected the
  device tiles show `SELECT +$0 / +$30 / +$104` (deltas floored to whole dollars)
  and the CTA shows the cheapest completion `$150.75` with `$167.04` struck through.

## Files in this repo for the task

- `sections/bundle-builder.liquid` — complete working section (markup + CSS + JS
  + schema). Client-side pricing from an embedded variant JSON island; locked
  accordion steps; per-tile deltas; sticky CTA; selling-plan attach for option
  values containing a configurable marker (default `(Club)`); marquee strip;
  theme-editor blocks for tile image/description/badge.
- `docs/journey-pack-reference.json` — FÜM's actual product JSON (ground truth
  for structure, pricing math, and selling plan shape). Reference only; our
  product will have its own components and prices.

## Your tasks

1. **Adapt the section to this theme** (don't rewrite it):
   - Cart drawer: the section currently supports Dawn-style
     `cart-notification`/`cart-drawer` custom elements with `renderContents()`,
     falling back to a `/cart` redirect. Inspect this theme's cart drawer
     implementation (search `cart/add`, drawer JS in `assets/`) and wire the
     success path so the drawer opens/refreshes natively.
   - Typography/colors: map the section's CSS to this theme's settings/variables
     (fonts via `settings_schema.json` font pickers or existing CSS custom
     properties) so it doesn't look bolted on. Keep the FÜM layout: serif-ish
     display title with a highlighted word, tile grid with bordered SELECT
     buttons and hard drop shadows, sticky rounded CTA, dark marquee strip.
   - Money formatting: confirm `shop.money_format` renders correctly with this
     store's currency settings.

2. **Create the product template**: `templates/product.bundle.json` containing
   the bundle-builder section (plus whatever recommendation/footer sections the
   default product template carries, minus the standard product-info section).

3. **Generate the product import CSV** at `docs/bundle-product-import.csv` for a
   3-option product following the pricing rules below, so the 90 variants don't
   have to be created by hand. Ask me for the component list and prices before
   generating; use FÜM's structure as the shape.

   Pricing rules (FÜM's exact system):
   - One-time variant price = sum of component prices, no compare-at.
   - Subscription variant (value contains the marker) price =
     one-time × (1 − club discount), compare-at = one-time price.
   - Optional step must include a "None"-style value at +$0.

4. **QA checklist** (verify in `shopify theme dev` preview before any push):
   - Deltas render floored (+$0 style), recompute as prior steps change
   - Steps 2/3 locked (greyed, unclickable) until prior step chosen
   - CTA label walks Select device → Select pack → Add to cart; price +
     strikethrough always shows cheapest completion until fully resolved
   - Marker value selected → frequency dropdown appears → `selling_plan`
     included in `/cart/add.js` payload (check Network tab)
   - Sold-out combination disables CTA with message
   - Mobile: 2-col tiles, sticky CTA, thumbnails scroll horizontally
   - `shopify theme check` passes on changed files

## Constraints

- Keep the section self-contained (one file) — no new global assets unless the
  theme's drawer integration genuinely requires it.
- Don't modify other templates or sections beyond the new template JSON.
- This theme is GitHub-connected: **work on a feature branch**, not the branch
  the live theme tracks. Pushes to the connected branch deploy to the theme.
- Do not copy FÜM's photography, copy, brand assets, or clinician-endorsement
  claims. Layout and mechanics only.
