---
name: "pmm-competitive-update"
description: "Reactive workflow for a specific competitive move (feature launch, pricing change, new entrant) for any product/company: analyzes the impact, proposes concrete battlecard changes for approval, and drafts a ready-to-send message for the sales team. Never edits files without explicit approval. Pulls competitor mapping and current differentiators from the active project context in memory/projects/. Use when the user shares news or a specific competitor move — not for building CI programs or battlecards from scratch. Triggers: \"[competitor] launched X\", \"how does this affect us\", \"what do I tell sales about this\"."
---

# Competitive Update (generic)

Processes a specific competitive move and translates it into concrete changes to sales materials, with user approval before touching any file.

## Instructions

### Step 1: Load context

Look for the active project's brief in `memory/projects/`. Identify the current competitor mapping and the differentiators currently in play. If no context exists, ask for the competitive positioning or battlecard reference before proceeding.

### Step 2: Understand the move

If not specified, ask **in a single message**: which competitor and what type of move (feature, pricing, campaign, acquisition, new entrant); what source is available (link, screenshot, text); and which segment it affects, if not obvious. If the information was already shared, work with it directly.

### Step 3: Impact analysis

Produce these four sections:

**What the competitor did** — objective 3–4 line summary, no interpretation.

**What changes** — assess three things: whether the move shrinks, indirectly pressures, or doesn't affect the current differentiator; what new objections the sales team will hear (max 3, in the prospect's actual language); and which segment or buying-committee persona is most exposed.

**What doesn't change** — which differentiators remain intact and what the competitor can't replicate with this move. This is what sales should reinforce, and it's as important as the previous section.

**Recommendation** — one of three: update the battlecard (the change is material), monitor (relevant but no action yet, revisit in 30 days), or no action.

### Step 4: Propose battlecard changes (only if recommendation is "update")

Look for the competitor's battlecard in the project folder. If it doesn't exist, say so and offer to create one with `b2b-battlecard-generator`. If it exists, propose each change showing the exact section, current text, proposed text, and one line explaining the rationale. Do not touch the file until every change is explicitly approved.

### Step 5: Apply changes (only after approval)

Apply exactly the approved changes, save the file in the same location with the same name, and confirm how many sections were modified. If adjustments are requested before approval, revise the proposal and repeat Step 4.

### Step 6: Sales team message

Regardless of whether the battlecard was updated, draft a short message for the team: what the competitor did and why it matters (2–3 lines), which differentiators still hold (this is the most important part for the team), up to 3 new objections with recommended responses, and one concrete instruction for what to do if this comes up in a sales conversation. Show the message before sending.

## Examples

**Example 1 — Material pricing change**

User says: "[Competitor] just announced a 30% price cut on their enterprise tier."

Actions:
1. Load context, confirm this competitor is in the current mapping
2. Ask which segment it affects if not obvious from the announcement
3. Run the 4-section impact analysis, recommending "update battlecard" given the material pricing pressure
4. Find the existing battlecard, propose the pricing-objection section update with current/proposed text side by side
5. Wait for approval before editing the file
6. Draft the sales message after approval, covering the objection and what still differentiates

Result: a fast, structured response that doesn't touch any file without sign-off, and gives sales a ready message the same day.

**Example 2 — Move that doesn't warrant action**

User says: "[Competitor] added a minor UI update to their dashboard."

Actions:
1. Load context
2. Run the impact analysis — conclude the move doesn't touch any current differentiator
3. Recommend "no action," explain why in the "what doesn't change" section
4. Skip Steps 4–5, still draft a brief internal note in Step 6 so sales has context if a prospect mentions it

Result: no overreaction to a minor move, but sales still has a heads-up.

## Troubleshooting

**Issue: No battlecard exists for the competitor and the recommendation is "update"**
Cause: this competitor hasn't been formally tracked yet.
Solution: say so explicitly and offer to create one with `b2b-battlecard-generator` before proposing incremental changes to a document that doesn't exist.

**Issue: User wants the file updated immediately, skipping the approval step**
Cause: urgency, often from an active deal needing an answer fast.
Solution: still show the proposed changes, even briefly, and get an explicit yes before editing — draft the sales message first if speed matters more than the battlecard update, since that's the more time-sensitive deliverable.

**Issue: The competitive move touches a differentiator not yet documented in context**
Cause: the positioning/messaging framework hasn't caught up with a newer differentiator.
Solution: flag this gap directly — the analysis can still proceed using what's documented, but note that the messaging framework may need updating separately.
