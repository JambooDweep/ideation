# Wear Today Phase 4: Shopping Agent — Product Requirements Document

Phase 4 of the [Roadmap](../ROADMAP.md). Builds on Phases [1](wear-today.md), [2](wear-today-phase-2-stylist-agent.md) and [3](wear-today-phase-3-wardrobe-manager.md). Status: draft. Owner: product owner (self). Date: 20/11/2026.

## Problem Statement

People buy clothes that don't go with anything they own, in sizes that don't fit, and wear them a handful of times. Shopping apps are built to sell more, rank by who pays, and know nothing about the buyer's wardrobe. Second-hand is cheaper and greener but harder to search and riskier to buy. Nobody tells the shopper, before they pay, whether an item is actually worth buying for them.

## Solution

When the user asks, Wear Today finds items that fill real gaps in their wardrobe, second-hand first, within their budget, and shows whether each one is worth buying: the new outfits it unlocks, its predicted cost per wear, a fit confidence and a footprint comparison. Results are ranked by fit, gap value and price, never by commission or payment.

The agent finds items and prepares the shop's checkout; **the user always pays at the shop**. Wear Today never pays and never stores card, bank or other payment details. Order confirmations (forwarded or "I bought it") add a draft item, count against the budget and start a return-deadline reminder.

The user can also share a product link from any shop to get the same "is this worth buying?" check.

Search and finds are free for everyone, funded by disclosed commission. Price watching, the weekly "gap finds" digest and return tracking are in the paid agent tier.

## User Stories

### Setting up

1. As a user, I want shopping switched off until I choose to turn it on, so that the app never pushes me to buy.
2. As a user, I want to set a monthly clothing budget and a maximum price per item before shopping is switched on, so that the agent stays within my means.
3. As a user, I want to set my size for each category, and for each brand where it differs, so that finds fit.
4. As a user, I want to add measurements optionally, so that fit can be judged more precisely.
5. As a user, I want the agent to learn my sizes from items in my wardrobe and from returns ("Brand X runs small for you"), so that fit improves over time.
6. As a user, I want to delete my sizes and measurements at any time, so that I control that data.

### Finding items

7. As a user, I want to ask for an item ("find me white trainers"), so that the agent searches for me.
8. As a user, I want to start a search from a gap in my wardrobe, so that I buy what unlocks the most outfits.
9. As a user, I want second-hand marketplaces searched alongside new retailers, with second-hand shown first, so that I buy greener and cheaper.
10. As a user, I want UK shops first, so that delivery and returns are simple.
11. As a user, I want nothing over my per-item maximum shown, so that I'm not tempted beyond my budget.
12. As a user, I want results ranked by fit, gap value and price, never by commission, so that I can trust the order.
13. As a user, I want a "why this order?" link, so that I can see how results were ranked.
14. As a user, I want a clear "We may earn a commission" label on every find that carries one, so that I know when the app benefits.
15. As a user, I want an optional weekly "gap finds" digest of up to 3 items matching my top gaps, within budget, off by default, so that I can see good finds without searching.

### Is it worth buying?

16. As a user, I want each find to show how many new outfits it unlocks with what I own, so that I know its real value.
17. As a user, I want a predicted cost per wear based on how often I wear similar items, so that I can judge the price.
18. As a user, I want a fit confidence (high, medium or low) with the reason, so that I know the risk.
19. As a user, I want a rough footprint comparison of second-hand against new, labelled as an estimate, so that I can choose the greener option.
20. As a user, I want to share a product link from any shop and get the same check, so that I can judge items I find myself.
21. As a user, I want the details read from a shared link shown for me to confirm, so that mistakes are caught.

### Second-hand safety

22. As a user, I want trust signals on second-hand listings (seller rating, condition, whether the photos are the seller's own), so that I can buy with confidence.
23. As a user, I want a fake warning for brands that are often counterfeited, so that I'm not caught out.
24. As a user, I want listings from low-rated sellers and listings with stock photos only hidden by default, with an option to show them, so that risky listings don't reach me unless I want them.

### Buying

25. As a user, I want the agent to prepare the shop's checkout with the item and my size, so that buying is quick.
26. As a user, I want to always pay myself at the shop, so that the agent can never spend my money.
27. As a user, I want a warning before a purchase would take me over my monthly budget, so that I stay in control.
28. As a user, I want to forward the order confirmation or tap "I bought it", so that the app knows what I bought.
29. As a user, I want a purchase to create a draft wardrobe item, confirmed with a photo, so that new clothes join my wardrobe easily.
30. As a user, I want purchases counted against my monthly budget, so that I can see what I have spent.

### Price watching and returns

31. As a user, I want to add items to a watch list with a target price, so that I buy when the price is right.
32. As a user, I want an alert when a watched item reaches my target price, so that I don't miss it.
33. As a user, I want return deadlines tracked from my orders, so that I don't miss them.
34. As a user, I want a reminder 5 days before a return deadline, so that I have time to decide.
35. As a user, I want the agent to draft the return steps, so that returning is easy.
36. As a user, I want the agent never to start a return or contact a seller itself, so that I stay in control.
37. As a user, I want a returned item taken out of my wardrobe and my size profile updated, so that future finds fit better.

### Privacy

38. As a user, I want Wear Today never to store my card numbers, bank details, payment tokens, shop passwords or logins, so that my financial data is safe.
39. As a user, I want my delivery address never stored, so that personal data is kept to a minimum.
40. As a user, I want order emails deleted straight after reading, keeping only item, price, date, shop and return deadline, so that nothing sensitive is kept.
41. As a user, I want shop links never to carry my personal details, so that shops don't learn about me from Wear Today.
42. As a user, I want no seller details stored from shared links or listings, so that other people's data is respected.

### Builder

43. As the builder, I want commission recorded separately from ranking, so that it can be shown never to affect order or inclusion.
44. As the builder, I want dashboard metrics for the Phase 4 targets, so that I can track them.
45. As the builder, I want the weekly digest counted in the $0.05 per user per day ceiling and on-demand searches excluded, so that costs stay predictable.

## Implementation Decisions

### Sources

- Second-hand marketplaces (for example eBay, Vinted, Depop) through official interfaces where offered; marketplaces without a public interface are approached for partnerships later.
- New retailers through affiliate product feeds.
- UK shops first.
- No bulk scraping (Q92a): it breaks most sites' terms, collects seller personal data, goes stale, breaks often, and would undermine the trust promise.
- **Share a link** (Q92b): the user shares one product link; the app fetches that one page, once, at the user's request, and reads the product details the page publishes for search engines and link previews (name, price, colour, photos). The user confirms them. No seller details are stored. The link leads to the shop's own checkout, with no commission.

### Trust level 3: prepare purchases

- The agent may fill the basket and prepare the checkout with the user's saved size. The user always pays at the shop.
- No tool can pay. No payment method is stored.
- Every action is in the action log.

### Modules

- **Size profile**: per-category and per-brand sizes, optional measurements, learning from wardrobe items and returns; fit confidence with reason.
- **Budget**: required before shopping is on; monthly budget and per-item maximum; over-maximum items never shown; warning before exceeding the monthly budget; spend from confirmed purchases.
- **Search**: on request, or from a gap; queries official interfaces and feeds; second-hand first; filters by size, budget and trust signals.
- **Ranking**: by fit, gap value and price, second-hand first; commission recorded separately and never used for order or inclusion; "why this order?" explanation.
- **Value check**: outfits unlocked (counted in code, as in Phase 1 gap analysis), predicted cost per wear from the user's wear history of similar items, footprint estimate (labelled).
- **Second-hand trust**: seller rating, condition, own-photos check, counterfeit-risk brand warning; low-rated and stock-photo-only listings hidden by default.
- **Checkout hand-off**: opens the shop's checkout with the item and size; links carry no personal details.
- **Purchase capture**: forwarded order confirmation or "I bought it"; draft wardrobe item (confirmed with a photo); spend recorded; return deadline extracted.
- **Price watch**: watch list with target prices; alerts.
- **Returns**: deadline tracking, 5-day reminder, drafted return steps; returned items removed and size profile updated. The agent never starts a return or contacts a seller.
- **Weekly digest**: optional, off by default, up to 3 finds for top gaps, within budget.
- **Commission disclosure**: "We may earn a commission" label on each find that carries one.

### Cost optimisation

| Work | How | Model |
|---|---|---|
| Searches via official interfaces, budget checks, outfit-unlock counts, price watching, return deadlines | Code | None |
| Order confirmation reading, find descriptions | AI | `claude-haiku-5-5` |
| Fit and style match from listing photos (capped at 20 listings per search) | AI | `claude-sonnet-5-5` |

On-demand searches are excluded from the $0.05 per user per day ceiling; the weekly digest counts towards it.

### Privacy

Never stored: card numbers, bank details, payment tokens, shop passwords and logins, delivery addresses, full order emails (deleted after reading), seller details. Kept: item, price, date, shop, return deadline; sizes and measurements (deletable at any time).

## Testing Decisions

- Good tests check behaviour the user sees, not internal details.
- **Ranking**: fixed sample listings; checks that commission never changes the order, second-hand comes first, items over the per-item maximum never appear, and low-rated or stock-photo-only listings are hidden by default.
- **Budget**: sample spend histories; checks the monthly budget warning and the per-item maximum.
- **Value figures**: fixed wardrobes; checks that outfit-unlock counts and predicted cost per wear are exact.
- **Fit learning**: sample returns; checks the size profile updates correctly.
- **Payment boundary**: checks that no tool can pay; that no card, bank, payment token, shop login or address is ever stored; that order emails are deleted after reading; and that shop links carry no personal details.
- **Share a link**: sample product pages; checks the right details are read, that only one page is fetched per share, and that no seller details are stored.

## Out of Scope

- The agent paying, or any stored payment method (permanently).
- Bulk scraping of shops or marketplaces.
- Paid placements or sponsored rankings (permanently).
- Starting returns or contacting sellers on the user's behalf.
- Shops outside the UK (later).
- Coordinating with other people's agents (Phase 5).

## Further Notes

### Success targets

| Measure | Target |
|---|---|
| Searches leading to a find the user opens or saves | 40% |
| Purchases that are second-hand | 50% |
| Purchases returned for poor fit | Under 15%, falling as the size profile learns |
| Items bought through Wear Today reaching 10 wears within 6 months | Above the user's own average for new items |
| Over-budget purchases preceded by a warning | 100% |

Second-hand share and wear count matter more than sales, in keeping with "buy less, better".

### Brainstorm decision log

| # | Decision |
|---|---|
| Q76 | Second-hand marketplaces and new retailers, second-hand first, UK first; official interfaces and feeds only. |
| Q77 | Shop on request; optional weekly "gap finds" digest, off by default. |
| Q78 | Size profile by category and brand, optional measurements, learning from wardrobe and returns; fit confidence with reason. |
| Q79 | Monthly budget and per-item maximum, required before shopping is on. |
| Q80 | The agent never pays: it prepares the shop's checkout and the user pays. No card or other sensitive data stored. |
| Q81 | Value check: outfits unlocked, predicted cost per wear, footprint estimate. |
| Q82 | Price watch with target prices; return deadline tracking with a 5-day reminder; drafted return steps; never starts a return. |
| Q83 | Second-hand trust signals and counterfeit warnings; risky listings hidden by default. |
| Q84 | Trust level 3 redefined as "prepare purchases"; the user always pays. |
| Q85 | Purchases known from forwarded order confirmations or "I bought it". |
| Q86 | Never store payment details, logins, addresses or full order emails; links carry no personal details. |
| Q87 | Commission labelled on every find; never affects ranking or inclusion; "why this order?" link. |
| Q88 | Cost model: code for search and checks, Haiku for reading and wording, Sonnet for fit from photos (20 per search). |
| Q89 | Search and finds free, funded by disclosed commission; price watch, digest and returns in the paid agent tier. |
| Q90 | Five success targets (above). |
| Q91 | Test areas (above). |
| Q92 | Out of scope list (above). |
| Q92a | No bulk scraping; partnerships for marketplaces without a public interface. |
| Q92b | "Share a link": one page fetched once at the user's request for the worth-buying check. |
