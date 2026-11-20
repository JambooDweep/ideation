# Wear Today: Roadmap

Date: 20/11/2026. Status: vision agreed in brainstorming (Q36 to Q41). Each phase gets its own PRD in `prds/` when it is started.

## Vision

A personal style agent that runs your wardrobe. It starts as an app you ask, becomes an agent that looks ahead for you, and grows into the service every other part of your life can ask about clothes.

### North star

In priority order:

1. **Stylist**: you always look and feel right for the occasion.
2. **Wardrobe manager**: you get the most out of what you already own.
3. **Sustainability coach**: you buy less, and better.

The stylist brings people in, the manager keeps them, and sustainability sets it apart.

## Phases

| Phase | Name | One line | PRD |
|---|---|---|---|
| 1 | Wear Today app | Ask for an outfit; get three from your own wardrobe | [prds/wear-today.md](prds/wear-today.md) |
| 2 | Personal stylist agent | It messages you first, remembers, and reads your invitations | Next |
| 3 | Wardrobe manager | Trips, usage, care, clear-outs and automatic capture | Next |
| 4 | Shopping agent (opt-in) | Gap-led, second-hand-first buying within your limits | Later |
| 5 | Social and coordinating agents | Your agent coordinates with friends' and family's agents | Later |
| 6 | Ambient and visual | Try-on avatar, mirror, speaker, AR, smart tags | Later |
| 7 | Platform | Other agents ask your style agent; third-party add-ons | Later |

Phases 2 and 3 come next: they give the biggest jump in usefulness and depend only on what Phase 1 builds.

### Phase 1: Wear Today app

Photograph your wardrobe one item at a time with a guided quality check; the AI tags each item. Describe the event by text or voice and get three outfits shaped by weather, dress code and mood, with reasons, swaps, saved outfits, gap suggestions, post-event feedback and insights. PWA on free hosting. See the PRD.

### Phase 2: Personal stylist agent

- **Messages you first**: reads your calendar and the forecast; a morning briefing with tomorrow's outfit.
- **Remembers**: who you have seen, what you wore and how it went ("you wore the green dress to Sam's last party"). Repeat-avoidance becomes part of the outfit engine.
- **Reads invitations**: takes dress code, venue and time from invitation emails, so nothing needs typing.
- **Watches for clashes**: warns when a planned outfit has an item marked in the wash.
- **Architecture shift**: from a fixed pipeline to an agent that chooses tools (wardrobe search, weather, calendar, outfit checker, gap analysis, notifications). The code checks remain as guardrails.
- **Background jobs**: scheduled daily checks; a per-user daily cost cap, a cheaper model for routine checks.
- **Channels**: push notifications and the morning briefing; messaging apps as a later option.

### Phase 3: Wardrobe manager

- **Trips**: reads a flight or hotel booking, checks the weather at the destination for each day, and builds a packing list and outfit plan from the fewest pieces.
- **Usage**: wear counts, cost per wear, items unworn for 12 months, a seasonal swap-over reminder.
- **Care**: washing and dry-cleaning reminders; repair and alteration prompts spotted in photos.
- **Clear-outs**: drafts resale listings or donation plans for unworn items; the user approves each one.
- **Automatic capture**: adds new items from purchase receipts in email, or splits every item out of a single video of the rail.

### Phase 4: Shopping agent (opt-in)

- **Gap-led shopping**: searches shops for the gap that unlocks the most outfits, second-hand first, within a budget the user sets.
- **Price watching and returns**: watches prices on items of interest; tracks returns and their deadlines.
- **Sustainability**: a wardrobe footprint and "buy less, better" nudges.
- **Strict authority**: never buys without one-tap approval each time, until the user opts out. Spending limit and action log always visible.

### Phase 5: Social and coordinating agents

- **Group coordination**: agent-to-agent coordination with friends and family: matching family photos, a wedding party colour scheme, not clashing with the host.
- **Shared wardrobes**: borrowing between friends, partners or flatmates, with "who has my coat?" tracking.
- **Stylist on request**: a human stylist reviews the agent's plan for big events (pay per use).

### Phase 6: Ambient and visual

- **Virtual try-on**: outfits shown on a private avatar of the user's body shape.
- **Always nearby**: a smart mirror or speaker in the bedroom; a phone camera view that shows outfits over the user's own wardrobe.
- **Smart tags**: washable tags track what is clean, packed or lent out without logging.

### Phase 7: Platform

- **Open interface**: other agents ask the style agent ("what should she pack?", "is this outfit ready?").
- **Third-party add-ons**: specialist agents such as sports kit, workwear or school uniforms.

## Principles across every phase

### Trust ladder

How far the agent acts on its own. The user moves up one setting at a time and can step back down whenever they like.

| Level | The agent may | From phase |
|---|---|---|
| 0 | Suggest | 1 |
| 1 | Remind and plan | 2 |
| 2 | Act on reversible things (mark items, draft listings) | 3 |
| 3 | Spend within limits | 4 |

Level 3 is the ceiling. It is switched on only by the user, and every purchase needs a one-tap approval until the user opts out. The agent never shares or deletes anything without asking.

### Memory you can see

A "what the agent knows about me" view; the user can edit or delete any of it.

### Code-checked facts

The agent never states an item, count, price or date that code has not checked. Outfits reference real item IDs; gap counts and costs are calculated in code.

### Privacy

- Consent for each connection (calendar, email, shops), revocable at any time.
- Read the minimum: event titles, times and places, not full calendars or inboxes.
- An action log of what the agent did and why.
- Photos and personal data used only to serve that user.

## Shopping stance

Shop on request only. Gap-led, second-hand first, no paid placements, and any commission earned is disclosed. Until Phase 4, there is no shopping at all.

## Business model

| Tier | What | Phase |
|---|---|---|
| Free | Core app: wardrobe, suggestions, gaps, feedback | 1 |
| Paid subscription | Agent features: proactive briefings, memory, invitations, trips, usage, care, clear-outs | 2 to 3 |
| Pay per use | Human stylist review | 5 |
| Disclosed affiliate commission | Purchases the user approves | 4 |

## Brainstorm decision log

| # | Decision |
|---|---|
| Q36 | North star: stylist, then wardrobe manager, then sustainability coach. |
| Q37 | Autonomy ceiling: Level 3, spending within limits, user-enabled only, from Phase 4; one-tap approval per purchase until the user opts out. |
| Q38 | Shopping on request only: gap-led, second-hand first, no paid placements, commission disclosed. |
| Q39 | Free core; paid tier for agent features; pay-per-use stylist reviews; disclosed affiliate commission in Phase 4 only. |
| Q40 | Phases 2 and 3 next. |
| Q41 | `ROADMAP.md` for the vision; one PRD per phase in `prds/`; Wear Today PRD stays as Phase 1. |
