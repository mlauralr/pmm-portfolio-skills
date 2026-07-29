---
name: "pmm-campaign-nurture"
description: "Designs a complete nurture email sequence for any product/company — copy, timing, branching logic, and exit conditions — delivered as a Word document ready to implement. Pulls segment, pain trigger, and canonical messages from the active project context in memory/projects/. Use when the user says \"build a nurture sequence\", \"I need emails to mature leads\", \"how do we follow up on trials that didn't convert\", \"post-demo sequence\", \"onboarding emails\", \"cold lead nurture\", \"re-engagement sequence\", or any variant of turning a lead segment into an automated communication sequence."
---

# Campaign Nurture (generic)

Designs nurture sequences aligned with the active product's approved messaging, with ready-to-use copy and clear timing logic.

## Instructions

### Step 1: Load context

Look for the active project's brief in `memory/projects/`. If unclear which project applies, ask. If no context file exists, ask for the messaging framework or persona/segment definitions before proceeding.

Identify the segment/persona the sequence targets, to select the right pain trigger and messages.

### Step 2: Define the sequence type

Four types. If not specified, determine which applies from context, or ask:

| Type | When | Objective |
|---|---|---|
| **Onboarding** | Trial activated, first 14 days | Drive to the activation milestone before it lapses |
| **Post-demo** | After a demo, no immediate decision | Keep momentum, close the conversation in 2–3 weeks |
| **Trial not converted** | Trial expired without upgrade | Re-engage and convert in the next 30 days |
| **Re-engagement** | Cold leads or customers inactive 60+ days | Spark interest with a new angle |

If the type doesn't fit any of the four, ask.

### Step 3: Gather missing input

If not specified, ask **in a single message**:

1. **Sequence type?** (onboarding, post-demo, trial not converted, re-engagement)
2. **Target segment/persona?**
3. **Prior interaction context?** (what they saw in the demo, what feature they used, why they didn't convert)
4. **Max number of emails?** (otherwise use the standards below)

### Step 4: Build the sequence

**Length standards by type** (default, adjust to context or user input):

| Type | Emails | Total duration |
|---|---|---|
| Onboarding | 5 emails | 14 days |
| Post-demo | 4 emails | 21 days |
| Trial not converted | 3 emails | 30 days |
| Re-engagement | 3 emails | 21 days |

For each email, define: number and name; timing (e.g., "Day 3 of trial" or "48h after demo"); send condition (always / only if previous wasn't opened / only if action X wasn't taken); subject line (with A/B variant if relevant); full copy in the tone and language used in context, direct and consultative, free of jargon the persona wouldn't use; single CTA; exit condition.

**Copy principles** (pull from context, don't invent):
- The entry pain varies by segment — use the context's mapping (e.g., a regulatory/financial trigger for sales-led new logos, an efficiency/productivity trigger for PLG installed base)
- Match the persona's stated preference for length and tone from context (if a persona values concision, keep emails short)
- Use only canonical numbers from context when citing benchmarks
- Never open with a differentiator or mechanism as the main promise — lead with the outcome
- Default to a consultative tone unless context specifies otherwise

**Branching logic:** for sequences longer than 3 emails, define at least one branch condition — opened previous → send deeper version; didn't open → send simplified version with different subject; completed the desired action → exit sequence.

### Step 5: Produce the Word document

Use the `docx` skill. Save in the active project's folder.

File name: `Nurture_[Type]_[Segment]_[MonthYear].docx`

Structure: cover page (type, target segment, date) · executive summary (objective, duration, entry/exit conditions) · text flow diagram (table: Email → Timing → Condition → CTA → Exit) · one email per section (Heading 2) with all Step 4 fields · implementation notes (recommended platform, list segmentation, tracking).

### Step 6: Consistency check

Verify before delivering: pain trigger is correct for the segment; numbers match context's canonical benchmarks; no email opens with a mechanism/differentiator as the main promise; tone matches what context specifies for this persona.

## Examples

**Example 1 — Post-demo sequence**

User says: "Build a post-demo nurture sequence for operations managers who saw the reporting feature."

Actions:
1. Load context, find the Operations Manager persona and its pain trigger and tone preference
2. Confirm 4 emails / 21 days as the default, adjust if user specifies otherwise
3. Write each email using the context's validated angle for reporting, with the persona's preferred concision
4. Generate `Nurture_PostDemo_OperationsManager_Aug2026.docx`

Result: a ready-to-implement sequence using the product's actual validated language, not generic drip copy.

**Example 2 — No persona definition available**

User says: "I need a re-engagement sequence for cold leads."

Actions:
1. Check context — no persona or pain trigger defined for "cold leads" specifically
2. Ask which existing persona these cold leads map to, or offer to help define one
3. Resume once clarified

Result: the sequence isn't built against an undefined audience with guessed pain points.

## Troubleshooting

**Issue: Context has no tone/voice guidance for the target persona**
Cause: the persona framework wasn't documented with communication preferences.
Solution: default to a consultative, concise tone and flag "[Tone assumption — validate against persona preferences]" rather than guessing a more aggressive sales voice.

**Issue: The requested email count doesn't match the type's standard**
Cause: the user has a specific constraint (e.g., platform limit, team bandwidth).
Solution: honor the user's number but flag if it's unusually short/long for the type and what risk that carries (e.g., "3 emails for onboarding may not reach activation — consider 5").

**Issue: Same pain trigger used for every email in the sequence**
Cause: didn't vary the angle across touches, making the sequence feel repetitive.
Solution: keep the core pain trigger consistent but vary the proof point or angle per email — this should be checked explicitly in Step 6.
