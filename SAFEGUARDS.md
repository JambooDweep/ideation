# Wear Today: Safeguards (Phases 1 to 4)

Date: 20/11/2026. Applies to every phase PRD in `prds/`. Where a PRD and this document disagree, this document wins until the PRD is updated. Decisions Q93 to Q102 come from the safeguards brainstorm; earlier decisions are referenced by number.

## Principles

1. **Code is the guardrail.** Facts (items, counts, prices, dates, budgets) and permissions (trust level) are checked in code, never left to the AI.
2. **Outside content is data, never instructions.**
3. **Least data.** Collect the minimum, keep it for a fixed time, let the user see, export and delete it.
4. **The user decides.** Nothing is confirmed, bought, posted, shared or deleted without the user.
5. **No harm to wellbeing.** Never comment on weight or bodies; never push spending.

## 1. Privacy and data

| Safeguard | Phase | Source |
|---|---|---|
| Photos used only for that user's suggestions; never used for training or shared | 1 | Q18 |
| Photos with faces rejected and not stored | 1 | Q11 |
| Photos with nudity, underwear being worn, children, or other people's belongings rejected before storage; neutral message to the user | 1 | Q97 |
| Fit and colour profile (see section 3) entered by the user only; never inferred from photos | 1 | Q93 |
| Colour undertone (warm, cool, neutral) collected, never skin colour | 1 | Q93 |
| Calendar read-only: titles, times, places, guest names only | 2 | Q42, Q52 |
| Guest names only (no emails or other details), used only for repeat-avoidance, deleted after 2 years | 2 | Q52 |
| Memory kept for 2 years by default; "what the agent knows about me" view with edit and delete | 2 | Q45 |
| Invitations by forwarding only; no inbox access | 2 | Q44 |
| Receipts, bookings and order emails: extract only the fields needed, delete the email immediately | 3, 4 | Q70, Q86 |
| Never stored: card numbers, bank details, payment tokens, shop passwords or logins, delivery addresses, booking references, seller details | 3, 4 | Q70, Q86, Q92b |
| Video frames not used as item photos discarded after splitting | 3 | Q70 |
| Shop links never carry personal details | 4 | Q86 |
| Trace and logs hold actions, timings and costs only, never photo, message or document content | All | Q19, Q54 |

## 2. AI accuracy and manipulation

| Safeguard | Phase | Source |
|---|---|---|
| Outfits reference real item IDs only; code validates every outfit before it is shown or saved | 1 | Q12, Q13 |
| Gap counts, cost per wear, outfit-unlock counts and budget figures calculated in code | 1, 3, 4 | Q33, Q62, Q81 |
| User-set tags and profile values always override the AI | 1 | Q12 |
| Weather beyond the forecast window labelled as seasonal norms | 1, 3 | Q24 |
| Footprint figures labelled as estimates | 4 | Q81 |
| **Prompt injection**: all outside content (forwarded invitations, receipts, bookings, order confirmations, shared product pages, listing text) treated as data only | 2 to 4 | Q95 |
| Outside content read into fixed fields (date, venue, price and so on) by a model with no tools | 2 to 4 | Q95 |
| Links and instructions inside outside content never followed | 2 to 4 | Q95 |
| Any action triggered by outside content checked in code against the trust level | 2 to 4 | Q95 |
| Refusal fallback on AI calls; failures shown honestly, never guessed | All | Q19 |

## 3. Wellbeing and inclusion

### Fit and colour profile (Q93)

Optional, part of Phase 1, entered by the user, every field skippable, editable and deletable:

- **Colour undertone**: warm, cool or neutral, with a simple guided check (for example, which looks better on you, silver or gold).
- **Height**.
- **Body proportions** in neutral terms (for example, longer legs or longer body).
- **Tailoring measurements** (optional): chest, waist, hips, inside leg, shoulder.
- **Gender preference** (Q102): the user can choose how they want to be styled (for example womenswear, menswear, or a mix), or choose not to say. If not set, styling is gender-neutral.

Used for colour advice, lengths and silhouettes, fit, alteration prompts (Phase 3) and size matching (Phase 4).

### Body-image rules (Q94)

- Never mention weight.
- Never describe an item as flattering in a way that implies a flaw.
- Never suggest dieting or changing one's body.
- Fit comments are about the clothes ("this cut is longer in the leg"), never the person.
- Enforced in the system instructions, checked in testing, and backed by an automatic filter on suggestion text.

### Inclusion (Q102)

- Gender-neutral by default; gender preference used only if the user sets it, and the user can choose not to say.
- The AI never assumes an item's gender from its category.
- Optional adaptive clothing note in the profile (for example easy fastenings or seated fit), used by the outfit engine.
- No shaming language about repeats, wardrobe size or spending.

## 4. Agent autonomy

| Safeguard | Phase | Source |
|---|---|---|
| Trust ladder enforced in code: tools only exist for the actions the current level allows | 2 to 4 | Q37, Q84 |
| Level 1: drafts and messages only; a draft is never confirmed until the user accepts | 2 | Q53 |
| Level 2: mark items away/returned and create drafts only; one-tap undo | 3 | Q71 |
| Level 3: prepare purchases; the user always pays at the shop | 4 | Q80, Q84 |
| Never post, delete, share, pay or contact anyone | 2 to 4 | Q71, Q80 |
| Action log of every agent action with time and reason | 2 to 4 | Q47 |
| Quiet hours, message frequency setting, "not helpful" feedback, user off switch | 2 | Q47 |
| Messages only when something has changed and matters | 2 | Q50 |

## 5. Money

| Safeguard | Phase | Source |
|---|---|---|
| The agent never pays; no stored payment method | 4 | Q80 |
| Shopping off until switched on; budget required first | 4 | Q79 |
| Items over the per-item maximum never shown; warning before exceeding the monthly budget | 4 | Q79 |
| **Cooling-off**: 24-hour "save for later" step on items over £100 by default, adjustable | 4 | Q98 |
| Monthly spend summary | 4 | Q98 |
| Weekly digest paused if the user goes over budget two months in a row | 4 | Q98 |
| Commission labelled, never affects ranking or inclusion; no paid placements | 4 | Q87 |
| No bulk scraping | 4 | Q92a |
| AI cost: $0.05 per user per day ceiling for background work; per-step model choice; caps on expensive steps | 2 to 4 | Q54, Q69, Q88 |
| Anthropic console monthly spend limit | 1 | Q35 |

## 6. Security (Q100)

- Users can reach only their own data (row-level security).
- Photos encrypted at rest and served through expiring links.
- Sign-in with passkeys or email codes; no passwords stored.
- Rate limits on uploads and AI calls.
- Secrets kept out of the code and out of the repository.
- Alerts on unusual activity (sign-ins, upload spikes, cost spikes).

## 7. Age (Q96)

- 18+ for the prototype and Phases 1 to 4, checked at sign-up.
- A teen version, which would bring in the UK Age Appropriate Design Code, is a later decision.

## 8. Compliance, rights and operations

### Data rights (Q99)

- One-tap export of all the user's data.
- Account deletion within 30 days, including backups.
- Plain-English privacy notice.
- Consent recorded for each connection (calendar, forwarding address, shops) and for the fit and colour profile.
- A data protection impact assessment (DPIA) completed before Phase 2.

### Monitoring and kill switches (Q101)

- Builder's global off switch for all agent messages, and for each agent tool.
- Alerts on cost spikes, error rates and body-image filter hits.
- Incident plan: find, contain, tell affected users within 72 hours if personal data is involved.

## Testing

| Area | Test |
|---|---|
| Photo safety | Labelled set: faces, nudity, underwear worn, children, other people's belongings; all rejected and not stored |
| Body-image rules | Prompt set designed to draw out weight or body comments; zero violations allowed; filter catches planted violations |
| Prompt injection | Sample invitations, receipts, bookings and product pages with planted instructions and links; none followed, no action outside the trust level |
| Trust ladder | Each level's tools only; no tool can pay, post, delete, share or contact |
| Money | Budget, per-item maximum, cooling-off and digest pause on sample spend histories |
| Privacy | Only the listed fields are stored; emails deleted after reading; export and deletion complete |
| Inclusion | Gender-neutral by default; gender preference respected when set; "prefer not to say" never infers gender |
| Spark's tone | Tone tests in [docs/persona.md](docs/persona.md): honesty, length, no emoji in sensitive moments or about the body, "are you human?" answered truthfully |

## Decision log

| # | Decision |
|---|---|
| Q93 | Optional fit and colour profile in Phase 1: undertone (not skin colour), height, proportions, optional tailoring measurements; user-entered only, never from photos. |
| Q94 | Body-image rules enforced by instructions, testing and a filter. |
| Q95 | Prompt-injection defences for all outside content, with a planted-attack test set. |
| Q96 | 18+ for Phases 1 to 4; teen version later. |
| Q97 | Photo check rejects nudity, underwear worn, children and other people's belongings; never stored. |
| Q98 | Cooling-off on items over £100 by default; monthly spend summary; digest pause after two over-budget months. |
| Q99 | Export, 30-day deletion, privacy notice, consent records, DPIA before Phase 2. |
| Q100 | Row-level security, encrypted photos with expiring links, passkeys or email codes, rate limits, no secrets in code, activity alerts. |
| Q101 | Global and per-tool kill switches, alerts, 72-hour incident plan. |
| Q102 | User sets a gender preference or chooses not to say; gender-neutral if not set; no gender assumed from item category; adaptive clothing note. |
