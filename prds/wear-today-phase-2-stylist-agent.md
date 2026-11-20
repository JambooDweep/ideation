# Wear Today Phase 2: Personal Stylist Agent — Product Requirements Document

Phase 2 of the [Roadmap](../ROADMAP.md). Builds on [Phase 1](wear-today.md). Safeguards: [SAFEGUARDS.md](../SAFEGUARDS.md). Status: draft. Owner: product owner (self). Date: 20/11/2026.

## Problem Statement

In Phase 1 the user has to remember to open the app and ask. Most outfit stress comes from not thinking ahead: the client meeting tomorrow, the dinner after work, the rain nobody checked, the shirt that turns out to be in the wash. People also lose track of what they wore last time they saw the same people. An app that only answers questions cannot help with any of that.

## Solution

Wear Today becomes a personal stylist agent that looks ahead for the user.

- It reads the user's Google or Outlook calendar, works out which events matter for clothing, and drafts an outfit for each one, which the user accepts, changes or rejects.
- It sends a morning briefing timed to the user's first event: the day's outfit, the weather, prep tasks and any changes between events, readable in 10 seconds.
- It re-checks the evening before and 2 hours before each event, and only messages when the plan no longer suits, with a fix.
- It reads invitations the user forwards to a dedicated address, so dress code, venue and time need no typing.
- It remembers what was worn, at which events and with whom, and avoids repeating outfits with the same people.
- It operates at trust level 1 (remind and plan): it never confirms, buys, shares or deletes anything on its own.
- It is cost-optimised: code does the routine checking, cheap models do routine wording and classification, and stronger models are used only where they change the result.

Phase 2 features are a paid tier, with a free 30-day trial. The Phase 1 core app stays free.

## User Stories

### Connecting

1. As a user, I want to connect my Google Calendar, so that the agent knows what is coming up.
2. As a user, I want to connect my Outlook calendar, so that work events are included.
3. As a user, I want to see exactly what the agent reads from my calendar (titles, times, places, guest names) before I connect, so that I can give informed consent.
4. As a user, I want to disconnect a calendar at any time, so that I stay in control.
5. As a user, I want a personal forwarding address for invitations, so that the agent can read invitations without access to my inbox.
6. As a user, I want to start a free 30-day trial of the agent features, so that I can see whether they are worth paying for.
7. As a user, I want to be told before the trial ends, so that I can decide whether to subscribe.
8. As a user, I want the core app to keep working if I don't subscribe, so that I don't lose my wardrobe.

### Events

9. As a user, I want the agent to work out which events matter for clothing (work meeting, dinner, wedding, gym, travel, video call), so that it plans only where it helps.
10. As a user, I want routine events (reminders, focus blocks, camera-off calls) skipped, so that I am not bothered about them.
11. As a user, I want to mark any event "plan for this", so that the agent includes it.
12. As a user, I want to mark an event "ignore events like this", so that similar events are skipped in future.
13. As a user, I want a forwarded invitation to fill in dress code, venue and time automatically, so that I never retype them.
14. As a user, I want a forwarded invitation matched to the right calendar event, or added as a new event if none exists, so that nothing is duplicated.

### Plans

15. As a user, I want the agent to draft an outfit for each upcoming event that matters, so that I don't have to remember to ask.
16. As a user, I want to accept, change or reject a draft, so that the final choice is mine.
17. As a user, I want a draft never to be treated as confirmed until I accept it, so that the agent never decides for me.
18. As a user, I want drafts to follow all the Phase 1 rules (only my available items, complete outfits, weather and dress code), so that they are wearable.
19. As a user, I want high-stakes events (wedding, interview, black tie) to get the most careful suggestions, so that I get the important ones right.

### Morning briefing

20. As a user, I want a morning briefing about 90 minutes before my first event (never before 06:30, 07:30 on days with no events), so that it arrives when I am getting ready.
21. As a user, I want to change the briefing time rules, so that they fit my routine.
22. As a user, I want the briefing to show the day's outfit, the weather and any change since the plan, so that I can dress in one glance.
23. As a user, I want prep tasks in the briefing ("the shirt needs ironing", "trousers marked in the wash"), so that nothing catches me out.
24. As a user, I want multi-event days handled ("one outfit for office and dinner; add the blazer at 18:00"), so that I plan the whole day at once.
25. As a user, I want a "show alternatives" button in the briefing, so that I can change my mind quickly.
26. As a user, I want the briefing readable in 10 seconds, so that it fits a busy morning.

### Changes

27. As a user, I want the agent to re-check each plan the evening before and 2 hours before the event, so that late changes are caught.
28. As a user, I want a message only when the planned outfit no longer suits, so that I am not interrupted for nothing.
29. As a user, I want each change message to include a fix ("rain at 17:00: swap the suede shoes for the leather boots"), so that I can act on it immediately.
30. As a user, I want the agent to notice when an event is moved, added or cancelled, so that plans stay in step with my calendar.
31. As a user, I want a warning when an item in a planned outfit is marked unavailable, so that I can sort it out in time.

### Memory and repeats

32. As a user, I want the agent to remember what I wore, to which events and with whom, so that it can help me avoid repeats.
33. As a user, I want it not to suggest the same outfit to the same group of people within 60 days, so that I don't turn up in the same thing.
34. As a user, I want it not to suggest the same key item (a statement dress, a suit) two days running, so that I don't look repetitive.
35. As a user, I want to adjust or switch off the repeat rules, so that they match how I dress.
36. As a user, I want repeats with different people to be allowed, so that I can make full use of my favourites.
37. As a user, I want a "what the agent knows about me" view, so that I can see everything it remembers.
38. As a user, I want to edit or delete anything in that view, so that I control my data.
39. As a user, I want memory kept for 2 years by default, so that old data doesn't pile up.

### Notifications and control

40. As a user, I want push notifications, so that briefings and changes reach me straight away.
41. As a user, I want a daily email if push isn't available on my device, so that I still get the briefing.
42. As a user, I want to be told that iPhone push needs the app added to the home screen, so that I can set it up.
43. As a user, I want quiet hours, so that the agent never messages me at night.
44. As a user, I want to choose how often the agent messages me, so that it is helpful, not noisy.
45. As a user, I want to mark a message "not helpful", so that the agent learns what to stop sending.
46. As a user, I want an off switch for all agent messages, so that I can pause it at any time.
47. As a user, I want an action log of what the agent did and why, so that I can trust it.

### Privacy

48. As a user, I want guest names stored as names only (no emails or other details), so that other people's data is kept to a minimum.
49. As a user, I want guest names used only for repeat-avoidance and never shown to anyone else, so that my contacts' privacy is respected.
50. As a user, I want event records and guest names deleted after 2 years, so that nothing is kept for ever.

### Builder

51. As the builder, I want per-user daily AI cost tracked against a $0.05 ceiling, so that routine checks never run away with costs.
52. As the builder, I want on-demand outfit requests excluded from the cap, so that users always get an answer when they ask.
53. As the builder, I want automatic escalation to a stronger model when plan acceptance falls below target, so that quality is protected.
54. As the builder, I want dashboard metrics for briefing opens, plan acceptance, dismissals and trial conversion, so that I can track the Phase 2 targets.

## Implementation Decisions

### Architecture

- The fixed Phase 1 pipeline becomes a set of tools an agent loop can call: wardrobe search, weather, calendar read, invitation parse, outfit engine, gap analysis, memory read/write, plan draft, notify. The Phase 1 code checks remain the guardrails: every outfit is validated in code before it is shown or saved.
- Trust level 1 is enforced in code: the agent's tools can draft plans and send messages, but have no ability to confirm plans, buy, share or delete.
- Scheduled background jobs (Vercel Cron or Supabase scheduled functions): calendar sync, evening-before re-check, 2-hours-before re-check, briefing send, trial-end reminder, memory expiry.

### Modules

- **Calendar connector**: Google Calendar and Microsoft Outlook through their official interfaces, read-only. Reads titles, times, places and guest names only. Stores a sync token and detects added, moved and cancelled events.
- **Invitation inbox**: a per-user forwarding address. Extracts dress code, venue, date and time, and matches to an existing event or creates one.
- **Event classifier**: classifies each event (work meeting, dinner, wedding, gym, travel, video call, routine) and whether clothing matters. Results reused for recurring event series. User overrides ("plan for this", "ignore events like this") always win.
- **Planner**: drafts a plan per relevant event using the Phase 1 outfit engine plus repeat-avoidance rules. Draft status until the user accepts.
- **Re-check**: code compares the forecast, the event and item availability with the plan. Only when a difference makes the outfit unsuitable does it ask the outfit engine for a fix.
- **Briefing**: timing (90 minutes before first event, not before 06:30, 07:30 default, user-adjustable); content (outfit, weather and changes, prep tasks, multi-event changes, "show alternatives").
- **Notifications**: web push first; daily email fallback; quiet hours; frequency setting; "not helpful" feedback; global off switch.
- **Wardrobe check-up** (from Phase 1, Q118 to Q123): no longer a separate reminder; its prompts appear in the morning briefing on the user's chosen check-up day, with the same frequency, skip, snooze and back-off rules.
- **Memory**: worn outfits, events, guest names (names only), feedback; 2-year retention; "what the agent knows about me" view with edit and delete.
- **Repeat-avoidance**: no same outfit with the same group within 60 days; no same key item two days running; user-adjustable.
- **Subscription**: 30-day trial, trial-end reminder, paid tier for agent features; core app unaffected.
- **Action log**: every agent action with time, reason and the tools used, never message or document content.

### Cost optimisation (Q54)

| Work | How | Model |
|---|---|---|
| Weather, calendar and availability change detection; repeat rules; cost cap | Code | None |
| Event classification (cached per recurring series) | AI | `claude-haiku-5-5` |
| Briefing wording | AI | `claude-haiku-5-5` |
| Outfit composition, routine | AI, low to medium effort | `claude-sonnet-5-5` |
| Outfit composition, high-stakes events or after two rejections | AI | `claude-opus-5-5` |
| Next day's plans drafted in the evening | Bulk job via the Batch API (50% cheaper) | As above |

- System instructions and the wardrobe summary are cached so repeat requests pay the cached rate.
- Before fixing this setup, an evaluation compares Sonnet at low/medium effort with Opus at low effort on the same requests; the cheaper result per accepted plan wins.
- If plan acceptance falls below the 50% target, routine composition moves up to the next model.
- Estimated cost: about $0.02 to $0.03 per active user per day (to be measured). Hard ceiling $0.05 per user per day for routine checks, set in config; on-demand requests are excluded.
- Models configured per step in one config.

## Testing Decisions

- Good tests check behaviour the user sees, not internal details.
- **Scenario tests (highest seam: the agent over time)**: a simulated user with a scripted calendar, forecast and wardrobe over two weeks, with stubbed AI responses. Checks: briefings sent at the right times; quiet hours respected; cost cap respected; re-plan when rain moves in or a meeting moves; messages only when a plan no longer suits; repeat-avoidance rules kept; an unaccepted draft never treated as confirmed; no action above trust level 1.
- **Event classification**: a labelled set of 200 sample calendar events, scored on "clothing matters" and event type.
- **Model comparison**: the Q54 comparison of models and effort levels on the same sample requests, reported as cost per accepted plan.
- **Invitation parsing**: sample forwarded invitations with expected dress code, venue and time.
- **Privacy**: tests that only names are stored for guests, that memory expires at 2 years, and that deletion removes everything.

## Out of Scope

- Apple iCloud calendar (later).
- Reading the whole inbox (later, opt-in).
- Messaging apps such as WhatsApp or Telegram (later).
- Trips and packing (Phase 3).
- Any action above trust level 1.

## Further Notes

### Success targets

| Measure | Target |
|---|---|
| Briefings opened | 60% |
| Drafted plans accepted, as is or after a swap | 50% |
| Agent messages dismissed as unhelpful | Under 10% |
| Trial users moving to the paid tier | 30% |

### Brainstorm decision log

| # | Decision |
|---|---|
| Q42 | Google and Outlook calendars first; Apple iCloud later. |
| Q43 | Briefing about 90 minutes before the first event, not before 06:30; 07:30 default on days with no events; user-adjustable. |
| Q44 | Invitations by forwarding to a dedicated address; inbox reading later, opt-in. |
| Q45 | Remember outfits, events and guest names for 2 years by default; viewable and deletable. |
| Q46 | Free 30-day trial of agent features, then paid; core app stays free. |
| Q47 | Push notifications first, daily email fallback; messaging apps later. |
| Q48 | Plan only for events where clothing matters; user can include or ignore. |
| Q49 | Briefing: outfit, weather and changes, prep tasks, multi-event changes; 10-second read; "show alternatives". |
| Q50 | Re-check the evening before and 2 hours before; message only when the plan no longer suits, with a fix. |
| Q51 | No same outfit with the same group within 60 days; no same key item two days running; adjustable. |
| Q52 | Guest names only; used only for repeat-avoidance; deleted with the event after 2 years. |
| Q53 | Agent drafts plans; never confirmed until the user accepts. |
| Q54 | Cost-optimised with reasonable quality: code first, Haiku for routine, Sonnet for outfits, Opus for high stakes, batch overnight, caching, measured comparison, escalation on low acceptance; $0.05 per user per day ceiling. |
| Q55 | Four success targets (above). |
| Q56 | Scenario tests, 200-event classification set, model comparison. |
| Q57 | Out of scope list (above). |
