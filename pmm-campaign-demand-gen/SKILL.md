---
name: "pmm-campaign-demand-gen"
description: "Designs a complete demand generation campaign for any product/company: targeting, per-channel messages, execution calendar, and funnel metrics — delivered as a Word document. Pulls ICP, sales motion, and canonical messages from the active project context in memory/projects/. Use when the user says \"I need to generate leads\", \"how do we attract new prospects\", \"build a demand gen campaign\", \"campaign for new logos\", \"outbound campaign\", \"content to attract our ICP\", or any variant of building pipeline with accounts that aren't customers yet."
---

# Campaign Demand Gen (generic)

Designs demand generation campaigns aligned with the active product's ICP, approved messaging, and sales motion.

## Instructions

### Step 1: Load context

Look for the active project's brief in `memory/projects/`. If unclear which project applies, ask. If no context file exists, ask for the ICP definition, messaging framework, or positioning doc before proceeding — do not invent segments, pain triggers, or benchmarks.

From the context, identify:
- The target segment(s) and their defining traits (size, vertical, buying signals)
- The applicable sales motion (PLG, sales-led, or hybrid)
- The pain trigger(s) that apply per segment
- The canonical content angles and messages already validated

### Step 2: Define the campaign approach

Two approaches. If not specified, determine which applies from context, or ask:

| Approach | When | Primary mechanism |
|---|---|---|
| **Inbound / content** | Audience actively searching for solutions, or time to build presence | Organic social + educational content + SEO |
| **Outbound / direct prospecting** | Specific new-logo target, urgency trigger (regulatory, competitive), or well-defined segment | SDR sequence + paid social + industry events |

If the context indicates one motion is validated for one approach (e.g., outbound works better for sales-led new logos, inbound for PLG installed base), use that as the default and say so.

### Step 3: Gather missing input

If not specified, ask **in a single message**:

1. **Target segment?** (from context's ICP, or "all")
2. **Approach?** (inbound/content, outbound/prospecting, or hybrid)
3. **Business objective?** (qualified leads, demos booked, trials, pipeline in $)
4. **Campaign duration?** (weeks)
5. **Available channels?** (LinkedIn, email, events, SDR, paid, in-app)
6. **Constraints?** (budget, resources, dates)

### Step 4: Build the campaign

**Block A — Targeting**
- Target account profile: size, type, geography (from ICP in context)
- Target contact profile: title, buying signals
- Estimated audience size within the addressable market
- How to find them: sourcing channels (sales intelligence tools, industry lists, associations, events)

**Block B — Per-channel messages**

For each active channel: entry angle (channel-specific hook, not the same message everywhere), format, frequency, single CTA.

Pull pain triggers and content angles from context — do not invent new ones. If context has none for the chosen segment, flag as an assumption and suggest validating with the messaging framework first.

**Block C — Execution calendar**

Table: Week | Actions | Channel | Owner | Progress metric | Milestone. Numbered 1 to N. Every week needs at least one visibility action and one conversion/outreach action.

**Block D — Metrics and funnel**

Full funnel: reach (impressions/emails sent/accounts contacted) → engagement (clicks/replies/opens) → qualified leads → opportunities → pipeline generated. Use benchmarks from context if they exist; otherwise mark as "[Assumption — validate after first campaign]". Include an early-warning signal: what red flag in week 2 means the message or targeting needs adjusting.

### Step 5: Produce the Word document

Use the `docx` skill. Save in the active project's folder.

File name: `DemandGen_[Segment]_[Approach]_[MonthYear].docx`

Structure: cover page · executive summary (objective, segment, approach, duration, primary KPI) · Block A · Block B (table + example copy per channel) · Block C · Block D · appendix with prospecting sources.

### Step 6: Consistency check

Verify before delivering: pain trigger matches segment and motion; content angles derive from approved messaging; funnel uses context's canonical benchmarks; targeting matches the approved ICP.

## Examples

**Example 1 — Outbound for new logos**

User says: "Build a demand gen campaign to reach mid-market operators who don't know us yet."

Actions:
1. Load context, find ICP segment matching "mid-market operators" and its validated pain trigger
2. Confirm outbound is the right approach given the urgency trigger in context
3. Ask the single clarifying message for objective, duration, channels, constraints
4. Build the 4 blocks using the context's SDR-ready messaging
5. Generate `DemandGen_MidMarketOperators_Outbound_Aug2026.docx`

Result: an outbound campaign plan grounded in the actual ICP and validated pain trigger, not a generic template.

**Example 2 — No ICP defined yet**

User says: "I want a demand gen campaign for our new segment."

Actions:
1. Check context — no ICP definition exists for "new segment"
2. Ask the user to run ICP/segmentation work first, or share a definition
3. Resume once provided

Result: no campaign is built against an undefined audience.

## Troubleshooting

**Issue: The context has no validated content angles for the chosen channel**
Cause: the messaging framework hasn't been extended to that channel yet.
Solution: derive the angle from the core message and pain trigger in context, flag it as "[New angle — not yet validated, review before launch]" rather than presenting it as proven.

**Issue: User wants to target a segment not defined in the ICP**
Cause: either the ICP is incomplete or this is a new market test.
Solution: ask directly whether this is a deliberate expansion test — if so, proceed but flag every targeting assumption; if not, suggest checking the ICP first.

**Issue: Funnel benchmarks look inconsistent with the context's numbers**
Cause: the campaign duration or channel mix differs from what the benchmark assumes.
Solution: note the mismatch explicitly and adjust the target range rather than copying the benchmark verbatim.
