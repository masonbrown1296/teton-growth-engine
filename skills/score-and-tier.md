# Skill: Score and Tier

## Purpose
Evaluate an operator from the conference attendee list and assign a tier 
with a recommended engagement approach. The tier determines which skills 
to run and how much personalization to invest.

## Inputs to Read
1. The campaign's attendee-targets.csv
2. The operator's profile.md (if it exists)
3. The operator's hubspot-record.json (if it exists)
4. The operator's engagement/ data (if any exists)
5. brand/competitor-landscape.md

## Tier Criteria

### Tier 1 (Full Personalization)
Operator meets ANY of the following:
- 20+ communities
- Known tech-forward posture (verified tech stack, public statements 
  on AI/innovation, named technology partnerships)
- Competitive displacement opportunity (currently using SafelyYou or 
  another direct Teton competitor)
- Existing sales contact (intro call, demo request, or form fill)

Tier 1 operators get every skill run against them with full 
contact-level personalization.

### Tier 2 (Segment-Level Personalization)
Operator does not meet any Tier 1 criteria but has:
- 5-19 communities, OR
- Some technology adoption signals (EHR vendor known, has deployed 
  visitor management or other care tech), OR
- A contact who engaged with a campaign (ad click, email open) but 
  no sales conversation

Tier 2 operators get pre-event emails and a one-pager, but with 
segment-level messaging (by persona, not by individual research). 
Post-event followup only if they engage during the campaign.

### Tier 3 (Standard Campaign)
Operator has:
- Under 5 communities, OR
- No actionable intelligence beyond a name on the attendee list

Tier 3 operators receive the default landing page and standard email 
sequence. No individual research investment.

## Override Flags

### Stalled Deal
If the operator has a HubSpot record with deal_stage "stalled" AND 
days_since_last_activity > 30, flag this regardless of tier. Stalled 
deals require a different re-engagement approach than new leads, even 
if the tier is the same. Note the specific objections from sales notes 
and recommend whether the conference is the right re-engagement moment 
or whether a different trigger (product update, new proof point, 
integration launch) should come first.

### Limited Intelligence
If no profile.md exists for an operator (only CSV row data), cap the 
tier at Tier 2 regardless of other criteria. Full personalization 
requires verified research. Flag that a profile needs to be built 
before running Tier 1 skills.

### Engagement Without Relationship
If an operator has engagement data (ad clicks, email opens, website 
sessions) but no sales contact and no HubSpot record, flag this as 
an opportunity. Someone at this company is researching Teton. Identify 
the engaged contacts and recommend adding them to the sales pipeline.

## Output Format
For each operator, produce:
- Tier assignment (1, 2, or 3)
- Which criteria triggered the tier (list all that apply)
- Override flags (stalled deal, limited intelligence, engagement 
  without relationship) if applicable
- Rationale (2-3 sentences summarizing the case)
- Recommended approach (which skills to run, in what order)
- Primary and secondary contacts to target
- Key messaging angle based on their specific situation
- CRM actions needed (rep assignment, stage update, data gaps to fill)

## Calibration Note
These criteria are rules-based. With real pipeline data across multiple 
conference cycles, the tier logic should be calibrated against actual 
conversion rates: which criteria predicted deals that closed, and which 
didn't. That calibration turns rules into a weighted model over time.

## Output Location
Save to the operator's output/ folder as tier-assessment.md
