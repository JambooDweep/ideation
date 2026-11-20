# Wear Today Phase 3: Wardrobe Manager — Product Requirements Document

Phase 3 of the [Roadmap](../ROADMAP.md). Builds on [Phase 1](wear-today.md) and [Phase 2](wear-today-phase-2-stylist-agent.md). Safeguards: [SAFEGUARDS.md](../SAFEGUARDS.md). Status: draft. Owner: product owner (self). Date: 20/11/2026.

## Problem Statement

Even with outfits planned, a wardrobe takes work to run. Packing for a trip means guessing the weather and over-packing. Building the digital wardrobe one photo at a time is the biggest effort in the product. People wear a small part of what they own, forget what needs dry-cleaning or mending, and keep clothes they never wear because sorting them out is a chore. Nobody knows what each item really costs per wear.

## Solution

Wear Today's agent becomes a wardrobe manager, built in this order:

1. **Trips**: spots trips in the calendar or forwarded bookings (or the user adds one), and builds a packing plan: an outfit for each day and event from the destination's forecast, the fewest pieces that mix together, a checklist within luggage limits, without items needed for events back home. Packed items are marked away until the trip ends.
2. **Automatic capture**: forwarded receipts become draft items; one video of a rail or shelf is split into separate items, each run through the Phase 1 quality check. *Update (Q127, Q129): rail videos and old order emails now arrive in Phase 1. Phase 3 builds on them: ongoing receipts feed prices and cost per wear, and capture links into usage and care.*
3. **Usage**: accepted plans count as worn (one-tap correction next morning), giving wear counts, cost per wear, and monthly insights with one suggestion.
4. **Clear-outs**: items unworn for 18 months, including a full season when they would suit, are flagged; the agent drafts a resale listing or donation plan for the user to approve.
5. **Care**: care labels read from optional photos; wear-based washing and dry-cleaning reminders; repair tasks from photos and a twice-yearly wardrobe check.

The agent works at trust level 2: it can act on reversible things (mark items packed or away, create drafts) with one-tap undo and a full action log. It never posts, deletes or contacts anyone. Phase 3 is part of the same paid agent tier as Phase 2, at no extra price.

## User Stories

### Trips

1. As a user, I want the agent to spot trips in my calendar (flights, hotel stays, "Lisbon 12/03 to 16/03"), so that I don't have to tell it.
2. As a user, I want to forward booking emails to my Wear Today address, so that trips are picked up even when they aren't in my calendar.
3. As a user, I want to add a trip by hand, so that I can plan any trip.
4. As a user, I want a packing plan with an outfit for each day and each event, based on the forecast at my destination, so that I pack the right things.
5. As a user, I want the plan to use the fewest pieces that mix together, so that I pack light.
6. As a user, I want to set a luggage limit (cabin bag only or checked bag), so that the plan fits what I am taking.
7. As a user, I want items planned for events back home kept out of the packing plan, so that I don't pack something I need.
8. As a user, I want to tick items off while packing, so that I don't forget anything.
9. As a user, I want packed items marked away until the trip ends, so that the agent doesn't suggest them at home.
10. As a user, I want items returned to my wardrobe automatically after the trip, with one-tap undo, so that I don't have to update anything.
11. As a user, I want to change the packing plan, so that it fits my plans.
12. As a user, I want the packing plan updated if the forecast changes before I leave, so that I am ready for the weather.

### Automatic capture

13. As a user, I want to forward purchase receipts, so that new clothes are added without typing.
14. As a user, I want a receipt to create a draft item with name, price, date and shop, so that most of the details are filled in.
15. As a user, I want draft items to stay drafts until I add a photo that passes the quality check, so that my wardrobe never holds items without a usable picture.
16. As a user, I want to record one video of a rail or shelf and get each item split out, so that I can build my wardrobe in minutes.
17. As a user, I want every item from a video checked for quality and tagged, so that it is as good as a single photo.
18. As a user, I want to review the items found in a video before they are added, so that mistakes are caught.
19. As a user, I want to be told which items in a video need a retake, so that I know what to photograph separately.

### Usage

20. As a user, I want an accepted plan to count as worn unless I say otherwise, so that tracking takes no effort.
21. As a user, I want a one-tap "Wore something else?" correction in the next morning's briefing, so that the record stays accurate.
22. As a user, I want wear counts for every item, so that I can see what I really use.
23. As a user, I want to add a price to an item, or have it filled in from a receipt, so that I can see cost per wear.
24. As a user, I want cost per wear shown only where a price exists, so that the figures are real.
25. As a user, I want to see my most and least worn items and items unworn this season, so that I understand my habits.
26. As a user, I want a figure like "you wear 20% of your wardrobe 80% of the time", so that I can see how much I really use.
27. As a user, I want a monthly summary with one suggestion ("you own 6 white shirts and wear 2; consider clearing out 2"), so that I get one useful action each month.

### Clear-outs

28. As a user, I want items flagged only after 18 months unworn, including a full season when they would suit, so that seasonal clothes aren't flagged by mistake.
29. As a user, I want to mark any item "keep", so that it is never flagged.
30. As a user, I want the agent to draft a resale listing (title, description, suggested price, photos) for a flagged item, so that selling takes seconds.
31. As a user, I want a donation plan (nearest charity shop or clothing bank) as an alternative, so that I can give items away easily.
32. As a user, I want to approve each listing or plan before anything happens, so that nothing leaves my wardrobe without my say.
33. As a user, I want to copy a listing into my resale app of choice, so that I can sell where I like.
34. As a user, I want items I sell or donate removed from my wardrobe only when I confirm, so that my records stay correct.

### Care

35. As a user, I want to photograph an item's care label and have the instructions read, so that I don't have to remember them.
36. As a user, I want wear-based care reminders with sensible defaults by category ("dry-clean the suit every 8 wears", "wash jeans every 6 wears"), so that my clothes are looked after.
37. As a user, I want to adjust care reminders for each item, so that they match how I treat my clothes.
38. As a user, I want a "collect from the cleaner's" reminder when a dry-clean-only item has been unavailable for a set number of days, so that I don't forget it.
39. As a user, I want care tasks in the morning briefing, not as separate messages, so that I am not interrupted.
40. As a user, I want to report damage or retake a photo and get a repair task, so that problems are fixed.
41. As a user, I want an optional twice-yearly wardrobe check of my top 20 items (about 10 minutes), so that wear and tear is spotted early.
42. As a user, I want each issue found to become a task ("loose button on the navy coat: tailor or DIY"), so that I know what to do.

### Trust and privacy

43. As a user, I want every agent action at trust level 2 undoable in one tap, so that I am always in control.
44. As a user, I want every action in the action log with the reason, so that I can see what the agent did.
45. As a user, I want the agent never to post, delete or contact anyone, so that nothing happens behind my back.
46. As a user, I want receipts and bookings deleted straight after reading, keeping only item, price, date and shop or trip dates and destination, so that my payment details, address and booking references are never stored.

### Builder

47. As the builder, I want background work kept under the $0.05 per user per day ceiling, with on-demand actions excluded, so that costs stay predictable.
48. As the builder, I want rail videos capped at 3 per user per day, so that the most expensive step can't run away.
49. As the builder, I want dashboard metrics for the Phase 3 targets, so that I can track them.

## Implementation Decisions

### New agent tools

Trip detect, booking parse, packing planner, receipt parse, video split, wear log, usage stats, clear-out flagger, listing draft, donation plan, care label read, care scheduler, repair task, mark away/return. All Phase 1 and Phase 2 code checks still apply.

### Modules

- **Trip detection**: from calendar events (flight, hotel, multi-day away events), forwarded bookings, or manual entry. Extracts dates and destination only.
- **Packing planner**: per-day and per-event outfits using the destination forecast for each day (seasonal norms beyond the forecast window, labelled), minimum-piece optimisation in code (maximise outfits from the fewest items), luggage limit, excludes items reserved for home events in the trip window. Tick-off checklist; marks items away; returns them after the trip.
- **Receipt capture**: forwarded receipts parsed into draft items (name, price, purchase date, shop). Draft until a passing photo is added.
- **Rail video capture**: one video split into item crops; each crop goes through the Phase 1 quality check and tagging; user reviews before adding; failing crops listed for retake.
- **Wear log**: accepted plan = worn; correction in the next briefing.
- **Usage stats**: wear counts, cost per wear (priced items only), most and least worn, unworn this season, share of wardrobe worn, monthly summary with one suggestion. Code only.
- **Clear-out flagger**: unworn 18 months and through at least one full suitable season; "keep" exemption. Code only.
- **Clear-out drafts**: resale listing (title, description, suggested price, existing photos) or donation plan (nearest charity shop or clothing bank). User approves each one; item removed only on confirmation.
- **Care**: optional care label reading; default wear-based schedules by category, adjustable per item; dry-cleaner collection reminder; tasks surfaced in the morning briefing.
- **Repairs**: from photo retakes, damage reports, and an optional twice-yearly check of the top 20 most-worn items.
- **Trust level 2 enforcement**: in code, tools may only mark items away/returned and create drafts; every action is undoable in one tap and logged. No tool can post, delete or contact anyone.

### Cost optimisation

| Work | How | Model |
|---|---|---|
| Usage stats, clear-out flags, care schedules, minimum-piece packing optimisation | Code | None |
| Receipt and booking reading, care label reading, listing wording | AI | `claude-haiku-5-5` |
| Rail video splitting and checking (capped at 3 videos per user per day) | AI | `claude-sonnet-5-5` |
| Packing plans | AI | `claude-sonnet-5-5`; `claude-opus-5-5` for trips over 7 days or with more than 3 events |

The Phase 2 approach carries over: caching, bulk overnight jobs where not time-sensitive, the $0.05 per user per day ceiling for background work, and on-demand actions excluded.

### Privacy

- Receipts and bookings: extract only item, price, purchase date and shop, or trip dates and destination; delete the email immediately; never store payment details, addresses or booking references.
- Video frames not used as item photos are discarded after splitting.

## Testing Decisions

- Good tests check behaviour the user sees, not internal details.
- **Packing plans**: sample trips with fixed wardrobes and forecasts; checks that every day and event is covered, the fewest pieces are used, luggage limits are respected, and items for home events are excluded.
- **Rail videos**: a labelled set of rail and shelf videos, scored on items found and accuracy of the split.
- **Receipts and bookings**: sample emails; checks the right fields are extracted and nothing sensitive is stored.
- **Clear-out rules**: fixed wear histories; checks the 18-month rule, the full-season rule and "keep".
- **Trust level 2**: checks that every action is undoable in one tap and logged, and that no tool can post, delete or contact anyone.

## Out of Scope

- Posting directly to resale apps; any automatic selling or donation booking.
- Booking dry cleaners or tailors.
- Reading the whole inbox (forwarding only).
- Shopping or buying (Phase 4).
- Laundry tracking with smart tags (Phase 6).

## Further Notes

### Success targets

| Measure | Target |
|---|---|
| Detected trips with an accepted packing plan (as is or after changes) | 70% |
| New items added through receipts or rail videos, after 3 months | 40% of new items |
| Flagged clear-out items acted on (listed, donated or kept) within 30 days | 25% |
| Rise in share of wardrobe worn at least once in 6 months, within 6 months of joining | 15 percentage points |

The last target is the wardrobe manager's main measure.

### Brainstorm decision log

| # | Decision |
|---|---|
| Q58 | Build order: trips, automatic capture, usage, clear-outs, care. |
| Q59 | Trips from calendar detection and forwarded bookings first; manual entry as fallback. |
| Q60 | Packing plan: per-day and per-event outfits, fewest pieces, luggage limits, home-event items excluded, tick-off checklist, packed items marked away. |
| Q61 | Accepted plan counts as worn; one-tap correction in the next briefing. |
| Q62 | Prices from receipts or user entry, optional; cost per wear only for priced items. |
| Q63 | Clear-out flag after 18 months unworn, including a full suitable season; "keep" exemption. |
| Q64 | Draft resale listings and donation plans; user approves each; no posting. |
| Q65 | Receipts and rail videos; receipt items stay drafts until a passing photo is added. Revised by Phase 1 Q129 and Q130: shop product photos count as photos, and about 20 basics may be added without a photo. |
| Q66 | Optional care label photos, wear-based defaults by category, care tasks in the morning briefing. |
| Q67 | Repairs from photos and damage reports plus an optional twice-yearly check of the top 20 items. |
| Q68 | Usage insights with one monthly suggestion. |
| Q69 | Cost model: code for stats and flags, Haiku for reading and wording, Sonnet for video and packing, Opus for long or busy trips; 3 videos a day; $0.05 ceiling. |
| Q70 | Receipts and bookings: extract minimum, delete email, never store payment details, addresses or booking references. |
| Q71 | Trust level 2: mark away/returned and create drafts only; one-tap undo; action log; never post, delete or contact. |
| Q72 | Part of the paid agent tier at no extra price. |
| Q73 | Four success targets (above). |
| Q74 | Five test areas (above). |
| Q75 | Out of scope list (above). |
