# Skill: Pre-Event Email Sequence

## Purpose
Generate a 3-email sequence to send before the conference. Each email 
is personalized to the operator and the specific contact receiving it.

## Inputs to Read
1. brand/positioning.md
2. brand/proof-points.md
3. brand/persona-messaging.md
4. brand/competitor-landscape.md
5. The operator's profile.md
6. The operator's contacts.md
7. The operator's engagement/ data (if any exists)
8. The operator's sales/ data (if any exists)
9. The campaign's context.md

## Operator Classification

Before writing emails, classify the operator into one of four paths 
based on available data. This determines the sequence structure.

### Path A: COLD (no prior engagement, no sales contact)
The operator appeared on the attendee list. We have a researched profile 
but no relationship. They haven't seen our content.

- Touch 1 (THE PROBLEM): Lead with a pain point relevant to their acuity 
  mix and size. Don't mention Teton by name until the second paragraph. 
  Make them feel seen first.
- Touch 2 (THE PROOF): Select the proof point most relevant to their 
  situation. If they're a SafelyYou customer, choose proof points that 
  highlight capabilities SafelyYou doesn't have (sleep, respiration, 
  predictive). Include a specific case study reference.
- Touch 3 (THE ASK): Direct ask to meet at the conference. Reference the 
  event by name. Include a booking link placeholder. Keep it under 4 sentences.

### Path B: WARM (prior engagement or sales contact exists, active)
The operator has engaged with content, had a sales conversation, or 
both. The relationship is alive.

- Touch 1: Reference their specific situation. Lead with something new 
  (a recent proof point, a product update, the August Health integration 
  if relevant to their stack).
- Touch 2: Address the specific interests or questions from their engagement 
  history or sales notes. If they clicked a technical ad, go technical. If 
  they visited the pricing page, address ROI.
- Touch 3: Direct ask to connect at the conference. Frame it around the 
  specific topic they've engaged with most, not a generic "let's meet."

### Path C: STALLED (prior sales contact exists, gone dark)
The operator had a real conversation (intro call, demo request) and 
stopped responding. This is the most sensitive path. Getting it wrong 
burns the relationship.

- Touch 1: Acknowledge the gap without being pushy or apologetic. Lead 
  with something genuinely new since the last conversation (a product 
  update, a new integration, a new proof point). Never open with "just 
  following up" or "checking in." The new information is the reason for 
  the email, not the conference.
- Touch 2: Address the specific objections from their sales notes. Don't 
  be defensive. Show you understand their concern and offer evidence that 
  the concern is addressable. If the objection was budget timing, show how 
  a pilot fits their cycle. If the objection was switching cost, show the 
  additive model.
- Touch 3: Low-commitment ask. "15 minutes to show you what changed since 
  we last talked." Frame the conference as a convenient moment, not a 
  deadline. No urgency language.

### Path D: LIMITED INTELLIGENCE (profile only, no engagement data)
The operator has a researched profile but no engagement data and no 
sales history. This is common for Tier 2 operators where we invested 
in research but haven't run campaigns yet.

- Touch 1 (THE PROBLEM): Same as Path A Touch 1, but rely more heavily 
  on the profile research. Use their public quotes if available. Reference 
  their specific acuity mix, geographic footprint, or recent news.
- Touch 2 (THE PROOF): Select proof points based on their company profile 
  alone. Match by acuity (memory care operators get fall data, IL/AL 
  operators get wellness monitoring data), by size (large portfolios get 
  Aquinas expansion story, smaller operators get ROI data), or by 
  competitive dynamic (SafelyYou customers get proactive-vs-reactive).
- Touch 3 (THE ASK): Same as Path A Touch 3.

## Multi-Stakeholder Logic

When generating emails for multiple contacts at the same operator, 
apply these rules:

### Contact Persona Matching
- COO / VP of Operations: operational visibility, liability, staffing ROI, 
  portfolio-wide consistency
- VP of IT / Director of Technology: architecture, privacy, integration, 
  implementation burden
- Clinical leader (CNO, VP Clinical, Director of Nursing): staff burden, 
  care quality, documentation, adoption
- CFO / Owner: ROI, CapEx, insurance impact, liability
- Sales/Marketing leader: family-facing data, census impact, competitive 
  differentiation in sales process

### Proof Point Rotation
Do NOT use the same lead proof point for multiple contacts at the same 
operator. If Touch 2 for the COO leads with Sagora (74% fall reduction), 
Touch 2 for the VP of IT should lead with a different proof point 
(Aquinas adoption, staff retention, privacy architecture). The operator 
will compare notes internally. Identical emails to different people 
signal a mass blast, not personalization.

### Engagement-Informed Divergence
If engagement data shows one contact is highly active and another is 
not engaging, adjust the sequence:
- For the active contact: accelerate. Reference their specific engagement 
  ("I noticed you downloaded the whitepaper"). Make the ask more direct.
- For the inactive contact: don't reference the active contact's 
  engagement. Keep the sequence standard. The goal is to create a second 
  entry point, not to pressure someone by implying their colleague is 
  already interested.

## For ALL Emails
- Personalize to the specific contact's persona
- Reference their company by name
- No more than 150 words per email
- Subject lines: specific, not clever. No clickbait.
- Sign off as the Teton sales rep, not the marketing team
- No em dashes anywhere. Use commas or periods.
- Never use "just following up," "touching base," "circling back," or 
  "hope this finds you well"

## Output Format
For each contact at the operator, produce:
- Classification path (A, B, C, or D) with brief justification
- Email 1: Subject line + body
- Email 2: Subject line + body
- Email 3: Subject line + body

## Output Location
Save to the operator's output/ folder as pre-event-emails.md
