# Skill: Sales One-Pager Brief

## Purpose
Generate a one-page sales leave-behind tailored to a specific operator. 
This is what the sales rep hands to the operator at the conference booth 
or sends as a PDF after a conversation.

## Inputs to Read
1. All brand/ files
2. The operator's profile.md and contacts.md
3. The operator's sales/ data (if any exists)
4. The operator's engagement/ data (if any exists, for proof point selection)

## Operator Intelligence Levels

The one-pager adapts based on how much we know about the operator.

### Full Intelligence (profile + sales data + engagement data)
Maximum personalization. Reference their specific situation, their 
public quotes, their tech stack, their stated objections. Proof points 
are selected based on what we know they care about from engagement 
patterns and sales conversations.

### Partial Intelligence (profile only, no sales or engagement data)
Personalize to their company profile: community count, acuity mix, 
geographic footprint, known technology stack. Proof points are selected 
by matching operator characteristics to the proof point selection guide 
in brand/proof-points.md. No references to specific conversations or 
engagement behavior.

### Minimal Intelligence (CSV row data only, no profile)
Do not generate a full one-pager. Instead, generate a segment-level 
brief based on their tier and acuity from the attendee CSV. Use 
persona-messaging.md to match the primary contact's title to the 
right messaging angle. Flag that a researched profile is needed 
before running this skill at full depth.

## Proof Point Selection

Select 3 proof points for the Key Outcomes section. Apply these rules:

1. **Match to pain.** If sales notes mention specific concerns (falls, 
   staffing, ROI, adoption), select proof points that directly address 
   those concerns.
2. **Match to acuity.** Memory care operators get fall-focused data. 
   IL/AL operators get wellness and quality-of-life data. SNF operators 
   get clinical documentation and response time data. Mixed-acuity 
   operators get the broadest proof point (Sagora or European).
3. **Match to objection.** If the operator raised adoption/rollout 
   concerns, include Aquinas (99.8% adoption). If they raised ROI 
   concerns, include the 5x ROI stat. If they raised staffing concerns, 
   include 28% retention.
4. **Deduplicate against emails.** If the pre-event email sequence 
   led with Sagora, the one-pager should either go deeper on Sagora 
   (add detail they haven't seen) or lead with a different proof point 
   (European 83% or Aquinas). The operator should feel like they're 
   learning something new, not re-reading the email.

## Output Format
- Headline: Operator-specific value proposition (1 line)
- Opening paragraph: 2-3 sentences connecting Teton to their specific 
  situation. If full intelligence is available, reference their own 
  language or public statements. If partial, reference their company 
  size, acuity, and market position.
- Key Outcomes section: 3 proof points selected per the rules above, 
  with specific numbers
- How It Works section: 3-4 bullet points on the product (sensor, edge 
  compute, privacy, EHR integration). Keep it simple.
- If COMPETITIVE DISPLACEMENT: "Going Beyond [Current Solution]" section. 
  2-3 sentences on what Teton adds that their current vendor doesn't 
  provide. Not negative. Additive framing: "In addition to fall detection, 
  Teton provides..." If sales notes captured the operator's own positive 
  language about their current vendor ("good at what it does"), echo that 
  and build from it.
- If AUGUST HEALTH customer: Call out the integration specifically. 
  "Teton integrates directly with August Health, which means [specific 
  benefit]." If the operator reacted positively to the integration in a 
  sales conversation, reference that reaction.
- CTA: "See It Live" + demo booking placeholder. Match CTA intensity 
  to relationship depth. New lead gets "Book a demo." Stalled deal gets 
  "See it in a live community, not a demo environment."
- Footer: Teton contact info placeholder

## Output Location
Save to the operator's output/ folder as one-pager-brief.md
