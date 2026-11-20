# Wear Today: Product Requirements Document

Phase 1 of the [Roadmap](../ROADMAP.md). Safeguards: [SAFEGUARDS.md](../SAFEGUARDS.md). Assistant persona: [Spark](../docs/persona.md). UX: [docs/ux/ux-decisions.md](../docs/ux/ux-decisions.md). Working name; can be renamed. Status: draft for prototype build. Owner: product owner (self). Date: 20/11/2026.

## Problem Statement

People regularly stand in front of a full wardrobe and still don't know what to wear. The choice depends on several things at once: what the event is, how formal it is, what the weather will be at that place and time, and how the person wants to feel. Most people hold their wardrobe in their head, forget what they own, fall back on the same few outfits, and only find out on the day that the one thing they planned is in the wash or wrong for the weather. Existing advice (magazines, shopping apps) is about clothes they don't own.

## Solution

Wear Today is a mobile-friendly, installable web app (PWA) with a chat assistant, typed or spoken, that suggests outfits from the user's own wardrobe.

1. The user builds a digital wardrobe with as little effort as possible: single photos, several items in one photo, a rail video, a rapid capture mode, "I own this" shop links, forwarded old order emails, or basics picked from a list. On first run they choose to start from an upcoming event (first outfit in about 3 minutes) or to build the wardrobe first. The app checks and fixes photos, and asks for a retake only when a photo can't be fixed.
2. The AI tags each item (category, colour, pattern, material, formality, warmth, season). The user can correct any tag.
3. The user describes what they need in free text or by voice, for example "friend's garden wedding on Saturday afternoon in Bath, I want to feel bold", helped by suggestive prompts and quick picks.
4. The app works out the occasion, dress code, mood, location and date, asks for anything missing, checks the weather forecast, and returns three outfits made only from available items, each with a one-line reason.
5. The user likes, rejects or swaps items, saves an outfit for a future date, and after the event is asked how it went. That feedback, and the style profile, shape future suggestions, and the user gets insights about their wardrobe.
6. The app spots gaps in the wardrobe: when a suggestion is held back by a missing item, and in an ongoing ranked list, it describes the item (type, colour, formality) and says how many new outfits it would unlock with what the user already owns. No brands or shopping links.

The prototype is a PWA; native iOS and Android apps follow in a later phase.

## User Stories

### Onboarding and account

1. As a new user, I want to create an account, so that my wardrobe is saved and available on any device.
2. As a new user, I want a short, optional style profile at sign-up (preferred styles, colours I avoid, fit preferences, gender preference or "prefer not to say"), so that suggestions suit me from the start.
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

### Fit and colour profile

67. As a user, I want to set my colour undertone (warm, cool or neutral) with a simple guided check, so that suggested colours suit me.
68. As a user, I want to add my height and body proportions in neutral terms, so that lengths and silhouettes suit me.
69. As a user, I want to add tailoring measurements (chest, waist, hips, inside leg, shoulder) if I choose, so that fit advice is precise.
70. As a user, I want to set how I want to be styled (for example womenswear, menswear or a mix) or choose not to say, so that suggestions respect me; styling is gender-neutral if I don't set it.
71. As a user, I want to add an adaptive clothing note (for example easy fastenings or seated fit), so that suggestions work for me.
72. As a user, I want every profile field optional, editable and deletable, and never guessed from my photos, so that I control this personal data.
73. As a user, I want the app never to comment on my weight or body, only on the clothes, so that using it feels good.

### Richer requests

74. As a user, I want to name an item to build around ("around my new green dress"), by text, voice or tapping it in my wardrobe, so that I can wear what I have in mind.
75. As a user, I want to leave items out of a request ("not the black trousers"), so that suggestions respect what I've ruled out.
76. As a user, I want the app to understand my role at the event (guest, host, wedding party, speaker, interviewee), so that the outfit suits my part.
77. As a user, I want the app to account for what I'll be doing (walking far, standing for hours, dancing, sitting on the floor, cycling there), so that the outfit is practical.
78. As a user, I want the venue and surface considered (indoors or outdoors, grass, cobbles, sand), so that my shoes work.
79. As a user, I want long events that run into the evening to include layers for the temperature drop, so that I'm comfortable all day.
80. As a user, I want photos expected at the event to favour solid colours over busy patterns, so that I look good in pictures.
81. As a user, I want common etiquette and cultural rules applied (no white at weddings unless I'm the bride, covered shoulders at religious venues if asked, dark colours at funerals), so that I never get it embarrassingly wrong.
82. As a user, I want to add my own etiquette rules ("at Hindu weddings, avoid black"), so that my culture and family customs are respected.
83. As a user, I want the app to ask when it is unsure about an etiquette rule, rather than assume, so that it doesn't impose rules that don't apply to me.
84. As a user, I want at most 2 follow-up questions per request, chosen by how much they change the outfit, so that asking stays quick.
85. As a user, I want each suggestion to show "Based on:" (weather, dress code, role, activity, venue), each tappable to correct, so that I can see and fix wrong assumptions.

### Richer profile

86. As a user, I want to say whether I run hot or cold, so that layers suit me at a given temperature.
87. As a user, I want to set hard limits (things I never wear, how much I like to cover up, highest heel I'll wear, fabrics I react to), so that I'm never suggested something I won't wear.
88. As a user, I want to set my everyday work dress code once, so that every work request is right.
89. As a user, I want to set colours I love, not only colours I avoid, so that suggestions lean towards them.
90. As a user, I want to add my hair colour and contrast level (light or dark hair against skin), so that colour advice is accurate.
91. As a user, I want to set style goals ("more polished", "more colour") and add optional inspiration photos of outfits I like, without faces, so that suggestions move towards the look I want.
92. As a user, I want these profile questions asked gradually ("one quick question" after a suggestion), never as a long form, so that setting up stays quick.

### Richer items

93. As a user, I want to mark whether an item fits now (fits well, tight, loose, needs altering), so that ill-fitting items aren't suggested.
94. As a user, I want items marked tight, loose or needs altering left out of suggestions until I mark them fixed, so that every suggestion is wearable today.
95. As a user, I want to mark favourites and confidence items, and items that are rarely comfortable, so that suggestions lean towards what I love wearing.
96. As a user, I want to confirm fabric weight and lining on outerwear and knits, so that warmth is judged correctly.
97. As a user, I want to group sets (a suit jacket that only goes with its trousers) and set "never pair these" rules, so that combinations make sense.
98. As a user, I want to mark items that need ironing or crease easily, so that the app can account for a quick morning.

### Learning and starting out

99. As a user, I want to give an optional one-tap reason when I reject an outfit (too formal, too casual, colour, not comfortable, worn recently, not me, wrong for the weather), so that the next suggestions improve straight away.
100. As a new user, I want a balanced first-set checklist (tops, bottoms, a pair of shoes of each type, a coat) shown as progress, so that I photograph the right items first.
101. As a new user, I want suggestions to start once I have 8 items, with a note that quality improves at 15 or more, so that I see value early and know what to add.

### Wardrobe check-up reminders

102. As a user, I want to choose at onboarding whether to get a wardrobe check-up reminder (monthly preselected), so that my wardrobe stays up to date without me remembering.
103. As a user, I want to change how often it comes (every 2 weeks, monthly, every 3 months) or switch it off any time, so that it suits me.
104. As a user, I want the check-up as a card on the app's home screen and, if I allow it, as a push notification, so that I see it where I prefer.
105. As a user, I want the reminder skipped if I've added or updated items in the last 2 weeks, so that I'm not reminded for nothing.
106. As a user, I want it to arrive at a good moment (Saturday at 10:00 by default, never late at night, outside quiet hours), and to change that time, so that it fits my week.
107. As a user, I want the check-up to show at most 3 personal prompts from Spark (new items, items stuck in the wash, items marked tight, seasonal swap-over, missing basics), so that it's quick and relevant.
108. As a user, I want each prompt to take me straight to the fix in one tap, and the whole check-up to take under 2 minutes, so that it's painless.
109. As a user, I want "Remind me next week" and "Stop these reminders" on every reminder, so that I stay in control.
110. As a user, I want reminders to drop to every 3 months, with a one-time note, if I ignore 3 in a row, so that the app never nags.

### Easier wardrobe building

111. As a new user, I want to see two ways to start, with what each involves (start with an event and get an outfit in about 3 minutes, or build my wardrobe first in about 10 minutes), so that I can choose what suits me.
112. As a new user starting with an event, I want Spark to tell me the 3 to 5 items to photograph for it, so that I get my first outfit quickly.
113. As a user, I want to photograph several items laid out together and have them split into separate items, so that I add many items at once.
114. As a user, I want to record one slow video along my rail or shelf and have each item found, so that I add a whole section in a minute.
115. As a user, I want a rapid capture mode that takes photos automatically and moves on, with tags reviewed later in one go, so that I don't tap for every item.
116. As a user, I want my photos fixed automatically (cropped, background removed, brightened) where possible, so that I rarely need a retake.
117. As a user, I want to check only the tags the AI is unsure about, so that reviewing is quick.
118. As a user, I want to add an item I own by sharing its shop link, using the shop's photo, so that I don't have to photograph it.
119. As a user, I want to forward old order emails and have those items added with the shop's photos, so that past purchases join my wardrobe without effort.
120. As a user, I want to add common basics from a list without a photo, clearly marked "photo needed", so that I can start with what I obviously own.
121. As a user, I want to see how many new outfits each item unlocks and my running total, so that adding items feels worthwhile.
122. As a user, I want an optional daily outfit for the day's weather, so that I have a reason to open the app every morning.
123. As a user, I want optional laundry-day prompts and short 10-minute category sprints, so that building my wardrobe fits into my routine.

## Implementation Decisions

### Platform and stack

- One installable PWA for the prototype: mobile-first, works in any modern browser, can be added to the home screen. Native iOS and Android apps are a later phase and should reuse logic where possible.
- Next.js (React, TypeScript) for the web app and its server-side API routes, in a single codebase.
- A hosted Postgres database with authentication and photo storage (for example Supabase). Row-level access so each user can only reach their own data.
- Claude API for photo quality judgement, item tagging, request understanding and outfit suggestion. Default model `claude-opus-5-5`; `claude-sonnet-5-5` as the cheaper option. Models are configured in one place, per step.
- A weather forecast API looked up by place and date/time.
- Voice: the browser's built-in speech recognition and synthesis first, with a cloud speech service as fallback where the browser lacks support. UK English voice and recognition.

### Modules

- **Accounts and profile**: sign-up with 18+ check, sign-in (passkeys or email codes), optional style profile, account deletion (removes photos, items, outfits, feedback).
- **Fit and colour profile**: optional, user-entered only (never inferred from photos): colour undertone (not skin colour), height, body proportions in neutral terms, optional tailoring measurements, gender preference or "prefer not to say", adaptive clothing note. Used by the outfit engine for colour, lengths, silhouettes and fit. Consent recorded. See [SAFEGUARDS.md](../SAFEGUARDS.md) for body-image rules and all other safeguards.
- **Capture**: camera and upload, framing guidance overlay, image downscaling before upload. Modes (Q127 to Q129):
  - **Single item** photo.
  - **Several items in one photo** (for example 4 to 6 laid on a bed), split into separate items.
  - **Rail or shelf video**, split into items (capped at 3 videos per user per day); brought forward from Phase 3.
  - **Rapid capture**: the camera stays open, captures automatically when an item is steady and well framed, and moves on; tagging runs in the background and is reviewed later in one go.
  - **Photo fixing**: auto-crop, background removal and brightness correction before the quality check; retake only when a photo can't be fixed.
  - Every item found in a multi-item photo or video goes through the quality check and tagging; the user reviews the items found before they are added.
- **"I own this" links** (Q129): the user shares a shop link for an item they own; the app fetches that one page once, at the user's request, and uses the shop's product photo and details (the Phase 4 share-a-link method, brought forward). No seller details stored.
- **Old order emails** (Q129): a per-user forwarding address (brought forward from Phase 2) accepts past order confirmations; items are added with the shop's product photos. Only item, price, date and shop are kept; the email is deleted immediately (the Phase 3 receipt rules, brought forward).
- **Basics without a photo** (Q130): about 20 common basics (white T-shirt, blue jeans, black trainers and so on) can be picked from a list, shown with a simple illustration and a "photo needed" badge. They can be used in suggestions, with Spark saying so ("using your white T-shirt, no photo yet"), and are excluded from gap and outfit-unlock counts until they have a photo.
- **First run** (Q124): two options presented side by side with what each involves, and the user chooses:
  - **Start with an event**: "What's coming up?" Spark names the 3 to 5 items to photograph for it; first outfit in about 3 minutes; the wardrobe grows through use.
  - **Build my wardrobe first**: guided capture of a balanced first set (about 10 minutes for 15 items) before the first outfit.
  Either way, the first-set checklist continues afterwards.
- **Outfits unlocked counter** (Q125): each item added shows the new outfits it creates and the running total ("+7 outfits ✨, 31 so far"), counted in code. No streaks.
- **Weather-only daily outfit** (Q126): opt-in, off by default, offered after the first outfit; a morning outfit for the day's weather at the user's location. Replaced by the Phase 2 morning briefing.
- **Habit prompts** (Q131): opt-in laundry-day prompt ("Putting laundry away? Snap each item as you fold it 🧺") under the check-up reminder settings, same no-nagging rules; 10-minute category sprints ("Today: shoes 👟") with progress.
- **Onboarding**: balanced first-set checklist (tops, bottoms, a pair of shoes of each type, a coat) shown as progress; suggestions available from 8 items, with a note that quality improves at 15 or more.
- **Photo quality check**: a fast on-device pre-check (blur, brightness, resolution) and then an AI check (single item, whole item in frame, background, no face). Returns pass/fail plus one specific tip. A photo containing a face is rejected and not stored.
- **Item tagging**: AI returns structured tags (category, colour, pattern, material, formality, warmth, season) via a fixed JSON schema, with a confidence per tag. Confident tags are accepted by default; only uncertain ones are flagged for a quick check ("Is this navy or black?") (Q128). Each tag records whether it came from the AI or the user; user-set values are never overwritten.
- **Item details** (user, one-tap): fit now (fits well, tight, loose, needs altering); favourite or confidence item, or rarely comfortable; confirmed fabric weight and lining for outerwear and knits; needs ironing or creases easily; sets and "never pair these" rules. Items marked tight, loose or needs altering are excluded from suggestions until marked fixed (Phase 3 turns them into alteration tasks).
- **Wardrobe**: item list, filters, availability toggle, delete.
- **Request understanding**: turns free text or voice into a structured request: occasion, dress code, mood, location, date/time, anchor item(s) to build around, excluded items, role (guest, host, wedding party, speaker, interviewee), activity (walking, standing, dancing, sitting on the floor, cycling), venue and surface (indoors or outdoors, grass, cobbles, sand), duration, etiquette and cultural context, photos expected. Anchors and exclusions can also be set by tapping items. It asks at most 2 follow-up questions, chosen by how much the answer would change the outfit, and returns the rest as stated assumptions. Fallback: device location and today's date.
- **Assumptions display**: each result shows "Based on:" with weather, dress code, role, activity and venue; each is tappable to correct and re-run.
- **Etiquette rules**: a built-in set of common rules checked in code (for example no white at weddings unless the user is the bride, covered shoulders at religious venues if asked, dark colours at funerals) plus user-added rules. When unsure whether a rule applies, the app asks rather than assumes.
- **Weather**: forecast for the resolved place and time; requests beyond the forecast window are told so and use typical seasonal conditions, labelled as such.
- **Outfit engine**: filters the wardrobe in code first (available items that fit now; anchors included and exclusions removed; hard limits from the profile (never-worn items, coverage, maximum heel, fabric sensitivities); sets and never-pair rules; warmth and season against the weather, adjusted for running hot or cold; formality against the dress code and the user's work dress code for work requests; footwear against activity and surface; etiquette rules), then asks the AI to compose three outfits from the shortlist with a one-line reason each, as structured output referencing item IDs only. Code validates every outfit: only real, available item IDs; at least top and bottom or a one-piece, plus shoes; outerwear when the weather calls for it. Invalid outfits are dropped and regenerated. If no valid outfit meets the occasion, the engine returns the closest match and names the missing item type. No shopping links.
- **Gap analysis**: candidate gap items are generic item descriptions (type, colour family, formality, warmth). For each candidate, code adds it as a virtual item and counts the new valid outfits it enables with the user's owned items, using the same outfit validity rules as the outfit engine. The AI may propose candidates and word the description, but the counts always come from code. In the moment, a gap is shown only when it relates to the current request (it would complete one of the three outfits or meet an unmet dress code); the insights list shows all gaps, ranked by new outfits unlocked. Dismissed gaps are stored per user and never shown again. No brands, prices or shopping links.
- **Chat assistant**: speaks as Spark, following [docs/persona.md](../docs/persona.md) (voice, honesty rules, length, emoji, tone tests).
- **Chat assistant (behaviour)**: conversational front end over request understanding and the outfit engine; supports follow-ups ("warmer", "less formal") and single-item swaps.
- **Saved outfits**: save against event and date, list upcoming.
- **Feedback**: like/reject/swap events at suggestion time, with optional one-tap reject reasons (too formal, too casual, colour, not comfortable, worn recently, not me, wrong for the weather) that also steer the next suggestions in the same chat; a post-event follow-up the day after a saved outfit's date (stars, quick tags, optional comment), which can be skipped or snoozed; in-app product feedback form with optional screenshot.
- **Personalisation**: profile plus feedback history summarised into preference signals given to the outfit engine. Profile additions, all optional and asked gradually ("one quick question" after a suggestion): runs hot or cold, hard limits, everyday work dress code, colours loved, hair colour and contrast level, style goals and optional inspiration photos (no faces, same photo check as items). Favourites and confidence items are preferred; rarely comfortable items are used less.
- **Insights**: per-user wardrobe insights; builder dashboard over anonymised, aggregated metrics.
- **Wardrobe check-up reminders**: opt-in at onboarding (monthly preselected); frequency every 2 weeks, monthly, every 3 months or off. In-app home card always; web push optional, permission asked only when reminders are switched on (on iPhone, push needs the app added to the home screen). A scheduled job (Vercel Cron or Supabase scheduled functions) checks each user: skip if items were added or updated in the last 2 weeks; send at the user's chosen time (default Saturday 10:00), outside quiet hours. Content: at most 3 prompts in Spark's voice, chosen in code from: new items, items unavailable for over 2 weeks, items marked tight, loose or needs altering, seasonal swap-over, missing basics from the gap list or first-set checklist; each links to its fix. Snooze ("Remind me next week") and stop on every reminder; after 3 ignored in a row, frequency drops to every 3 months with a one-time note; never sent twice for the same thing. From Phase 2, the check-up moves into the morning briefing.
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
- **Request understanding**: a set of sample descriptions with expected structured requests and missing-field lists, including relative dates ("this Saturday") resolved as dd/mm/yyyy, anchors and exclusions, role, activity, venue and etiquette context; checks that no more than 2 follow-up questions are asked and that unasked fields appear as stated assumptions.
- **Outfit engine constraints**: fixed wardrobes and requests; checks that anchors always appear, exclusions never do, ill-fitting items and hard limits are respected, sets and never-pair rules hold, footwear suits activity and surface, and running hot or cold shifts layers.
- **Etiquette rules**: sample events (weddings, funerals, religious venues, user-added rules); checks that no suggestion breaks an applicable rule and that the app asks when unsure.
- **Reject reasons**: checks that a reason changes the next suggestions in the same chat (for example "too formal" lowers formality).
- **Check-up reminders**: simulated users over 6 months; checks opt-in is respected, reminders are skipped after recent updates, sent only at the chosen time outside quiet hours, hold at most 3 relevant prompts, back off after 3 ignored, and are never repeated for the same thing.
- **Photo quality check**: a labelled image set (good, blurred, dark, cropped, face present) with expected pass/fail and tip; checks that photo fixing rescues fixable photos.
- **Multi-item photos and rail videos**: labelled sets scored on items found and accuracy of the split.
- **"I own this" links and order emails**: sample pages and emails; checks the right details are read, one page per share, only listed fields kept, emails deleted.
- **Basics without a photo**: checks they are flagged in suggestions and excluded from gap and unlock counts.
- **First run**: scripted runs of both first-run options; time to first outfit measured.
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
| Inbound email (forwarding address for order emails) | Cloudflare Email Routing with an Email Worker | Inbound email unlimited on the free plan; the Worker runs on Workers Free | Needs a domain on Cloudflare DNS: free if the builder already owns one (move its DNS to Cloudflare's free plan, copying existing records first, and use a sub-domain so existing email is untouched); otherwise roughly £10 a year, the only extra cost; the Worker must be written to parse each message and post it to the app |
| Voice | Browser built-in speech | Free | Support varies by browser (best in Chrome and Safari); cloud speech fallback left out of the free set-up |

Decisions:

- Photos are downscaled to about 200 KB before upload, so 1 GB holds about 5,000 item photos: roughly 100 test users at 30 to 50 items each.
- The Claude API is the only paid part. A monthly spend limit is set in the Anthropic console, and `claude-sonnet-5-5` is used for tagging and suggestions during testing to keep costs down.
- Separate Supabase projects for development and testing (the two free projects).
- Inbound email (Q133): a catch-all on a sub-domain (for example `in.<app domain>`) routes every message to one Email Worker. Each user gets a random, unguessable address (`u-<random>@in.<app domain>`). The Worker checks the address belongs to a user, extracts the message text, posts it to the app over HTTPS with a shared secret, and stores nothing itself. The app extracts only item, price, date and shop and discards the message. Messages to unknown addresses are dropped. A user can regenerate their address if it attracts spam.
- Inbound email fallback: if no domain is available during early testing, a small free email-to-webhook service (for example Mailhooks, about 100 emails a month) can stand in, on the condition that it does not retain message content.
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

## Further Notes

### Success targets for the prototype

| Measure | Target |
|---|---|
| Time for a new user to photograph 15 items | Under 10 minutes |
| Time to return 3 outfits | Under 15 seconds |
| Requests where at least 1 of 3 outfits is liked | 70% |
| Photos passing the quality check on the first or second try | 90% |
| Wardrobe check-ups opened | 40% |
| Opened check-ups leading to at least one wardrobe update | 50% |
| Users getting a first outfit within 5 minutes of sign-up | 80% |
| Users reaching 15 items within 7 days | 60% |

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
| Q10 | One item per photo. Revised by Q127: several items per photo and rail videos allowed. |
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
| Q93 | Optional fit and colour profile (see SAFEGUARDS.md). |
| Q102 | Gender preference or "prefer not to say"; gender-neutral if not set. |
| Q103 | Requests can name items to build around and items to leave out. |
| Q104 | Request understanding covers role, activity, venue and surface, duration, etiquette and photos; at most 2 follow-up questions; the rest shown as assumptions. |
| Q105 | Built-in etiquette rules checked in code, plus user-added rules; ask when unsure. |
| Q106 | Profile adds running hot or cold, hard limits, work dress code, colours loved, hair colour and contrast, style goals and inspiration photos (no faces); optional and gradual. |
| Q107 | Items add fit now, favourite or rarely comfortable, fabric weight and lining, needs ironing, sets and never-pair rules; ill-fitting items excluded until fixed. |
| Q108 | Optional one-tap reject reasons that steer the next suggestions and learning. |
| Q109 | Balanced first-set checklist; suggestions from 8 items, better at 15 or more. |
| Q110 | Each suggestion shows "Based on:" assumptions, tappable to correct. |
| Q111 to Q117 | The chat assistant is Spark: a calm, warm, honest styling assistant; see docs/persona.md. |
| Q118 | Wardrobe check-up reminder: opt-in at onboarding, monthly by default, adjustable or off. |
| Q119 | In-app card always; optional push; moves into the morning briefing from Phase 2. |
| Q120 | Skipped after updates in the last 2 weeks; Saturday 10:00 by default, outside quiet hours. |
| Q121 | At most 3 personal prompts in Spark's voice, one tap to each fix, under 2 minutes. |
| Q122 | Snooze and stop on every reminder; drops to every 3 months after 3 ignored; never repeated. |
| Q123 | Targets: 40% of check-ups opened; half of those lead to an update. |
| Q124 | First run offers both options with what each involves: start with an event, or build the wardrobe first. |
| Q125 | "Outfits unlocked" counter, counted in code, no streaks. |
| Q126 | Opt-in weather-only daily outfit, replaced by the Phase 2 briefing. |
| Q127 | Several items per photo and rail videos in Phase 1 (3 videos a day); revises Q10. |
| Q128 | Rapid capture, photo fixing, review of uncertain tags only. |
| Q129 | "I own this" links and old order emails in Phase 1, with Phase 3 and 4 privacy rules. |
| Q130 | About 20 basics without a photo, flagged in suggestions and excluded from counts; revises Phase 3 Q65 for basics. |
| Q131 | Opt-in laundry-day prompt and 10-minute category sprints. |
| Q132 | Targets: first outfit within 5 minutes for 80%; 15 items within 7 days for 60%. |
| Q133 | Free inbound email: Cloudflare Email Routing with an Email Worker on a sub-domain; random per-user addresses; Worker stores nothing; small free webhook service as early fallback. |
