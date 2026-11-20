# Wear Today: Product Requirements Document

Working name; can be renamed. Status: draft for prototype build. Owner: product owner (self). Date: 20/11/2026.

## Problem Statement

People regularly stand in front of a full wardrobe and still don't know what to wear. The choice depends on several things at once: what the event is, how formal it is, what the weather will be at that place and time, and how the person wants to feel. Most people hold their wardrobe in their head, forget what they own, fall back on the same few outfits, and only find out on the day that the one thing they planned is in the wash or wrong for the weather. Existing advice (magazines, shopping apps) is about clothes they don't own.

## Solution

Wear Today is a mobile-friendly, installable web app (PWA) with a chat assistant, typed or spoken, that suggests outfits from the user's own wardrobe.

1. The user builds a digital wardrobe by photographing their clothes, shoes and accessories one item at a time. The app guides each photo and checks it is good enough to analyse, giving a specific tip when it isn't.
2. The AI tags each item (category, colour, pattern, material, formality, warmth, season). The user can correct any tag.
3. The user describes what they need in free text or by voice, for example "friend's garden wedding on Saturday afternoon in Bath, I want to feel bold", helped by suggestive prompts and quick picks.
4. The app works out the occasion, dress code, mood, location and date, asks for anything missing, checks the weather forecast, and returns three outfits made only from available items, each with a one-line reason.
5. The user likes, rejects or swaps items, saves an outfit for a future date, and after the event is asked how it went. That feedback, and the style profile, shape future suggestions, and the user gets insights about their wardrobe.
6. The app spots gaps in the wardrobe: when a suggestion is held back by a missing item, and in an ongoing ranked list, it describes the item (type, colour, formality) and says how many new outfits it would unlock with what the user already owns. No brands or shopping links.

The prototype is a PWA; native iOS and Android apps follow in a later phase.

## User Stories

### Onboarding and account

1. As a new user, I want to create an account, so that my wardrobe is saved and available on any device.
2. As a new user, I want a short, optional style profile at sign-up (preferred styles, colours I avoid, fit preferences, optional gender presentation), so that suggestions suit me from the start.
3. As a new user, I want to skip any or all profile questions, so that I can start quickly.
4. As a user, I want to edit my style profile at any time, so that it keeps up with my taste.
5. As a user, I want to install the app on my phone's home screen, so that it feels like a normal app.
6. As a user, I want a short first-run guide to photographing my first items, so that I know how to build my wardrobe.

### Building the wardrobe

7. As a user, I want to photograph a wardrobe item with my phone camera from inside the app, so that adding items is quick.
8. As a user, I want to upload an existing photo from my gallery, so that I can add items I have already photographed.
9. As a user, I want on-screen guidance while framing (one item, whole item in frame, plain background, good light), so that my photos pass first time.
10. As a user, I want the app to check each photo for focus, lighting, framing, single item and background, so that only usable photos enter my wardrobe.
11. As a user, I want a specific tip when a photo fails ("too dark, move nearer a window"), so that I know exactly how to fix it.
12. As a user, I want photos showing a person's face to be rejected, so that my wardrobe holds no personal images.
13. As a user, I want to retake a failed photo straight away, so that I don't lose momentum.
14. As a user, I want the AI to tag each item's category, colour, pattern, material, formality, warmth and season, so that I don't have to type descriptions.
15. As a user, I want to review and correct the tags, so that the wardrobe is accurate.
16. As a user, I want my corrections to always override the AI's tags, so that the app never reverts my changes.
17. As a user, I want to add items in a quick sequence (photo, check, tags, next), so that I can photograph 15 items in under 10 minutes.
18. As a user, I want to browse my wardrobe by category, colour and season, so that I can see what I own.
19. As a user, I want to delete any item, so that my wardrobe reflects what I own.
20. As a user, I want to mark an item unavailable ("in the wash", "at the dry cleaner's") and mark it back, so that suggestions only use items I can wear.
21. As a user, I want clothes, shoes, outerwear and accessories (bags, jewellery, belts, scarves) all to count as items, so that suggestions are complete outfits.

### Asking for an outfit

22. As a user, I want to describe what I need in free text, so that I can say it naturally.
23. As a user, I want to speak my request, so that I can ask hands-free while getting ready.
24. As a user, I want suggestive example prompts showing what the assistant understands (event, time, place, mood, dress code), so that I give it what it needs.
25. As a user, I want optional quick picks for occasion, formality and mood, so that I can ask in a couple of taps.
26. As a user, I want the app to infer the dress code from my description and show it, so that I can correct it if it's wrong.
27. As a user, I want the app to read the location and date from my description, so that I don't fill in a form.
28. As a user, I want the app to ask only for missing details, falling back to my current location and today's date, so that a quick request still works.
29. As a user, I want the weather forecast for the event's place and time to be taken into account, so that I am neither cold nor overheated.
30. As a user, I want to see the weather the suggestion is based on (for example "14°C, light rain, 18:00"), so that I understand the choice.
31. As a user, I want my mood to influence the suggestions (bold, relaxed, confident, understated), so that I feel the way I want to.
32. As a user, I want to ask for an outfit for a future date within the forecast window (up to about 7 to 14 days), so that I can plan ahead.

### Receiving suggestions

33. As a user, I want three outfit suggestions per request, so that I have a real choice without being overwhelmed.
34. As a user, I want each outfit shown as a collage of my own item photos, so that I can picture it immediately.
35. As a user, I want a one-line reason for each outfit, so that I trust the choice.
36. As a user, I want every outfit to include at least a top and bottom (or a one-piece) plus shoes, with outerwear when the weather needs it, so that it is wearable as given.
37. As a user, I want suggestions returned within 15 seconds, so that the app is quicker than deciding myself.
38. As a user, I want suggestions to use only available items I own, so that I can actually wear them.
39. As a user, I want to be told plainly when my wardrobe can't meet the occasion, with the closest outfit and the missing item named ("a dark suit or a long dress"), so that I know where I stand.
40. As a user, I want to like or reject an outfit, so that the app learns my taste.
41. As a user, I want to swap a single item in an outfit for an alternative, so that I can fine-tune without starting again.
42. As a user, I want to ask follow-ups in the chat ("something warmer", "less formal"), so that I can refine the suggestions conversationally.
43. As a user, I want to save my chosen outfit against the event and date, so that I don't have to decide again on the day.
44. As a user, I want to see my upcoming saved outfits, so that I can get ready in advance.

### Voice

45. As a user, I want the assistant to speak its replies, so that I can use it while dressing.
46. As a user, I want to switch spoken replies off easily, so that I can use the app quietly.
47. As a user, I want voice to work in UK English, so that it understands me and sounds natural.

### Feedback and learning

48. As a user, I want a follow-up the day after a saved outfit's event ("How did your outfit go at Saturday's wedding?"), so that I can say how it worked.
49. As a user, I want to rate the outfit 1 to 5 stars, pick quick tags (comfortable, got compliments, too warm, too formal) and add an optional typed or spoken comment, so that feedback takes seconds.
50. As a user, I want to skip or snooze the follow-up, so that it never nags me.
51. As a user, I want my likes, rejections, swaps and post-event ratings to shape future suggestions, alongside my style profile, so that the app gets better for me.
52. As a user, I want a "Your wardrobe insights" view (most and least worn items, best-rated outfits, items never suggested, patterns such as "you rate bold colours higher at parties"), so that I understand and make better use of my wardrobe.
53. As a user, I want to send feedback about the app itself (bugs, ideas) with an optional screenshot, so that I can help improve it.

### Privacy and control

54. As a user, I want my photos used only to make my suggestions, so that my wardrobe stays private.
55. As a user, I want to delete my whole account and all its data, so that I can leave cleanly.
56. As a user, I want dates shown as dd/mm/yyyy and temperatures in °C, so that the app reads naturally in the UK.

### Builder (product owner)

57. As the builder, I want an anonymised dashboard of like rate, post-event rating, swap rate, photo-check pass rate and response time, so that I can track the prototype's success targets.
58. As the builder, I want to review in-app product feedback in one place, so that I can prioritise fixes.
59. As the builder, I want the AI model choice set in one config, so that I can switch between quality and cost.
60. As the builder, I want each AI call's token use and cost recorded, so that I know the running cost per user and per request.

### Wardrobe gaps

61. As a user, I want a suggestion to tell me when one missing item would complete or improve it ("Missing: a neutral blazer. Adding one would complete this outfit and pair with 6 other items you own"), so that I know what is holding the outfit back.
62. As a user, I want a "Gaps in your wardrobe" list in my insights, ranked by how many new outfits each item would unlock ("White trainers would create 14 new combinations with what you have"), so that I can add the items that make the most of my wardrobe.
63. As a user, I want each gap described by item type, colour and formality ("a navy or charcoal blazer, smart-casual"), without brands or shopping links, so that it is advice, not advertising.
64. As a user, I want the "would pair with N items" and "N new combinations" figures to be calculated from my actual wardrobe, so that I can trust them.
65. As a user, I want to dismiss a gap suggestion as "not interested", so that it is not shown to me again.
66. As a user, I want the gap list to update when I add, delete or mark items unavailable, so that it always reflects my current wardrobe.

## Implementation Decisions

### Platform and stack

- One installable PWA for the prototype: mobile-first, works in any modern browser, can be added to the home screen. Native iOS and Android apps are a later phase and should reuse logic where possible.
- Next.js (React, TypeScript) for the web app and its server-side API routes, in a single codebase.
- A hosted Postgres database with authentication and photo storage (for example Supabase). Row-level access so each user can only reach their own data.
- Claude API for photo quality judgement, item tagging, request understanding and outfit suggestion. Default model `claude-opus-5-5`; `claude-sonnet-5-5` as the cheaper option. Models are configured in one place, per step.
- A weather forecast API looked up by place and date/time.
- Voice: the browser's built-in speech recognition and synthesis first, with a cloud speech service as fallback where the browser lacks support. UK English voice and recognition.

### Modules

- **Accounts and profile**: sign-up, sign-in, optional style profile, account deletion (removes photos, items, outfits, feedback).
- **Capture**: camera and upload, framing guidance overlay, image downscaling before upload.
- **Photo quality check**: a fast on-device pre-check (blur, brightness, resolution) and then an AI check (single item, whole item in frame, background, no face). Returns pass/fail plus one specific tip. A photo containing a face is rejected and not stored.
- **Item tagging**: AI returns structured tags (category, colour, pattern, material, formality, warmth, season) via a fixed JSON schema. Each tag records whether it came from the AI or the user; user-set values are never overwritten.
- **Wardrobe**: item list, filters, availability toggle, delete.
- **Request understanding**: turns free text or voice into a structured request (occasion, dress code, mood, location, date/time, extra constraints), returns which fields are missing, and asks for them. Fallback: device location and today's date.
- **Weather**: forecast for the resolved place and time; requests beyond the forecast window are told so and use typical seasonal conditions, labelled as such.
- **Outfit engine**: filters the wardrobe in code first (available items only; warmth and season against the weather; formality against the dress code), then asks the AI to compose three outfits from the shortlist with a one-line reason each, as structured output referencing item IDs only. Code validates every outfit: only real, available item IDs; at least top and bottom or a one-piece, plus shoes; outerwear when the weather calls for it. Invalid outfits are dropped and regenerated. If no valid outfit meets the occasion, the engine returns the closest match and names the missing item type. No shopping links.
- **Gap analysis**: candidate gap items are generic item descriptions (type, colour family, formality, warmth). For each candidate, code adds it as a virtual item and counts the new valid outfits it enables with the user's owned items, using the same outfit validity rules as the outfit engine. The AI may propose candidates and word the description, but the counts always come from code. In the moment, a gap is shown only when it relates to the current request (it would complete one of the three outfits or meet an unmet dress code); the insights list shows all gaps, ranked by new outfits unlocked. Dismissed gaps are stored per user and never shown again. No brands, prices or shopping links.
- **Chat assistant**: conversational front end over request understanding and the outfit engine; supports follow-ups ("warmer", "less formal") and single-item swaps.
- **Saved outfits**: save against event and date, list upcoming.
- **Feedback**: like/reject/swap events at suggestion time; a post-event follow-up the day after a saved outfit's date (stars, quick tags, optional comment), which can be skipped or snoozed; in-app product feedback form with optional screenshot.
- **Personalisation**: profile plus feedback history summarised into preference signals given to the outfit engine.
- **Insights**: per-user wardrobe insights; builder dashboard over anonymised, aggregated metrics.
- **Usage and cost log**: per AI call, record step, model, tokens and cost, never photo or text content.

### Rules

- The app only suggests items the user owns and has marked available.
- The AI never invents items: outfits reference item IDs, and code checks them.
- Photos are used only for that user's suggestions; they are not used to train models or shared.
- UK English throughout; dates dd/mm/yyyy; temperatures °C.

## Testing Decisions

- Good tests check external behaviour (what the user sees and what a module returns for given inputs), not internal details.
- **Highest seam: the outfit engine.** Given a wardrobe, a structured request and a weather forecast, it returns three valid outfits or a clear gap message. Tested with fixed wardrobes and a stubbed AI response to cover: only available items used; formality and warmth filters; outerwear in cold or rain; missing-category gap messages; invalid AI output (unknown item IDs, incomplete outfits) rejected.
- **Gap analysis**: fixed wardrobes with known answers, checking that the counts of new combinations and paired items are exact, that the ranking orders by outfits unlocked, that in-the-moment gaps appear only when relevant to the request, that dismissed gaps never reappear, and that output contains no brands or links.
- **Request understanding**: a set of sample descriptions with expected structured requests and missing-field lists, including relative dates ("this Saturday") resolved as dd/mm/yyyy.
- **Photo quality check**: a labelled image set (good, blurred, dark, cropped, several items, face present) with expected pass/fail and tip.
- **Item tagging**: a labelled image set scored for tag accuracy; check that user edits survive re-tagging.
- **End-to-end**: a scripted run in a mobile browser: sign up, add items, request an outfit, swap an item, save it, give post-event feedback, delete the account.
- **Evaluation against success targets** (see Further Notes), run on a small group of test users.

## Hosting for Testing

The prototype is tested on free tiers only. Limits were checked against 2026 sources on 20/11/2026; confirm them on each provider's pricing page before relying on them.

| Need | Free choice | Free-tier limits | Constraints |
|---|---|---|---|
| Next.js PWA hosting | Vercel Hobby | No card, no expiry; HTTPS (required for a PWA); a preview link for each push; about 100 GB transfer and a few hours of server time a month | Personal, non-commercial use only; a feature pauses until the month resets if limits are exceeded |
| Database, sign-in, photo storage | Supabase Free | 500 MB database, 1 GB file storage, 5 GB data out a month, 50,000 monthly users, up to 2 projects | Project pauses after about a week of low activity: open it before test sessions or add a scheduled ping |
| Weather forecast | Open-Meteo | Free, no key, forecasts up to 16 days | Non-commercial use; terms to be confirmed |
| Voice | Browser built-in speech | Free | Support varies by browser (best in Chrome and Safari); cloud speech fallback left out of the free set-up |

Decisions:

- Photos are downscaled to about 200 KB before upload, so 1 GB holds about 5,000 item photos: roughly 100 test users at 30 to 50 items each.
- The Claude API is the only paid part. A monthly spend limit is set in the Anthropic console, and `claude-sonnet-5-5` is used for tagging and suggestions during testing to keep costs down.
- Separate Supabase projects for development and testing (the two free projects).
- Moving to Vercel Pro and Supabase Pro (about $20 and $25 a month, from third-party guides) is needed before any commercial use, and removes the inactivity pause.

## Out of Scope

- Shopping, affiliate links or "buy this" suggestions.
- Social sharing.
- Virtual try-on.
- Native iOS and Android apps (later phase).
- Calendar sync (later phase).
- Payments or subscriptions.
- Languages other than English.
- Repeat-avoidance based on what the user wore recently.
- Photos of whole outfits or several items at once (one item per photo only).

## Further Notes

### Success targets for the prototype

| Measure | Target |
|---|---|
| Time for a new user to photograph 15 items | Under 10 minutes |
| Time to return 3 outfits | Under 15 seconds |
| Requests where at least 1 of 3 outfits is liked | 70% |
| Photos passing the quality check on the first or second try | 90% |

### Brainstorm decision log

| # | Decision |
|---|---|
| Q1 | Help people choose what to wear for an event, occasion and mood. |
| Q2 | New standalone idea. |
| Q3 | PRD for own build; end goal is app and web. |
| Q4 | Clothes come from the user's own wardrobe via camera photos, with a guided quality check. |
| Q5 | General consumer choosing for themselves. |
| Q6 | Free-text request with suggestive prompts showing what the AI expects. |
| Q7 | Weather and dress code shape the pick. |
| Q8 | Prototype: mobile-friendly web app with a chat assistant that supports voice. |
| Q9 | One PWA now; native apps later. |
| Q10 | One item per photo. |
| Q11 | Check focus, light, framing, single item, background; reject faces; give a specific tip. |
| Q12 | AI tags every item; user edits always win. |
| Q13 | Three outfits as collages with reasons; like, reject, swap. |
| Q14 | Location and date from the description; ask if missing; fall back to device location and today. |
| Q15 | Dress code inferred, shown, correctable. |
| Q16 | Two-way voice; spoken replies easy to switch off. |
| Q17 | Optional, skippable style profile that learns from feedback. |
| Q18 | Account with cloud storage; delete item or account; photos used only for suggestions. |
| Q19 | Claude for vision and suggestions, configurable models; browser or cloud speech. |
| Q20 | Working name "Wear Today". |
| Q21 | Honest about wardrobe gaps: closest outfit plus the missing item; no shopping. |
| Q22 | Clothes, shoes and accessories all count; minimum outfit rules. |
| Q23 | Available/unavailable toggle per item. |
| Q24 | Plan ahead within the forecast window and save outfits; plus user feedback and analysis (Q29 to Q31). |
| Q25 | UK English, °C, dd/mm/yyyy. |
| Q26 | Next.js PWA, Supabase-style backend, Claude API, browser speech with cloud fallback. |
| Q27 | Four success targets (above). |
| Q28 | Out-of-scope list (above). |
| Q29 | Post-event follow-up the day after: stars, quick tags, optional comment; skippable or snoozable. |
| Q30 | Insights for the user and an anonymised dashboard for the builder; feedback feeds suggestions. |
| Q31 | In-app product feedback form with optional screenshot. |
| Q32 | Gap suggestions both in the moment (when relevant) and as a ranked "Gaps in your wardrobe" list in insights. |
| Q33 | Gaps described by type, colour and formality; no shopping links; combination counts calculated in code from the real wardrobe. |
| Q34 | Gap suggestions can be dismissed and are remembered. |
| Q35 | Test on free tiers: Vercel Hobby, Supabase Free, Open-Meteo, browser speech; Claude API is the only paid part. |
