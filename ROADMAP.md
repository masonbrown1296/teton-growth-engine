# Teton Growth Engine: Production Roadmap

## What This Prototype Demonstrates

The logic layer. How operator intelligence, multi-channel engagement 
signals, and sales context combine to produce personalized campaign 
assets that are genuinely different per operator and per contact.

This prototype uses simulated engagement data and manual skill 
invocation to demonstrate that logic independently of the integration 
layer. Everything below describes what production looks like.

## Integration Layer (Phase 1)

### Data Ingestion
The engagement/ and sales/ JSON files in this prototype mirror the 
schemas of real platform exports. In production:

- **HubSpot API** populates sales/ data: deal stage, lifecycle stage, 
  contact records, activity timeline, call notes, form submissions. 
  Scheduled pull via HubSpot API v3 (contacts, deals, engagements 
  endpoints). Normalize into the hubspot-record.json schema.
- **Meta Ads API** populates meta-retargeting.json: campaign performance, 
  creative-level metrics, matched contacts from custom audiences. 
  Pulled via Marketing API with breakdowns by creative and placement.
- **LinkedIn Campaign Manager** data (via CSV export, HubSpot sync, 
  or approved API access) populates linkedin-campaign.json: matched 
  audience engagement, content interactions, company-level engagement 
  signals. LinkedIn is the least automatable pipe in the stack. Day 
  one it's a CSV export. If the team has or can get Marketing API 
  access, it automates. If not, HubSpot's LinkedIn integration or a 
  connector tool like Supermetrics bridges the gap.
- **Email platform (HubSpot or dedicated ESP)** populates 
  email-engagement.json: per-recipient open/click/bounce data with 
  link-level tracking.
- **Website analytics (GA4 or HubSpot tracking)** populates 
  website-sessions.json: identified sessions via UTM parameters and 
  email click tracking, page-level engagement, time on site, 
  conversion events.

Each ingestion script normalizes source data into the existing JSON 
schemas. The skills don't change. The data layer becomes real instead 
of simulated.

### Operator Research
Profile.md files in this prototype were built from manual research. 
In production, the initial profile can be scaffolded from:
- Company database (PitchBook, Crunchbase, or NIC's own attendee data)
- Press release monitoring (for technology announcements, funding, 
  expansion plans)
- Public statement tracking (conference talks, podcast appearances, 
  published articles)

A researcher skill would pull from these sources and produce a draft 
profile for human review before it enters the system. The human review 
step is non-negotiable. Automated research generates plausible-sounding 
profiles that are sometimes wrong. Verified research is what makes the 
personalization defensible.

## Automation Layer (Phase 2)

### Pipeline Orchestration
Replace manual "claude [command]" invocation with a scheduled pipeline:

1. **Weekly data pull:** Ingestion scripts pull fresh data from all 
   platforms into the campaign's operator folders.
2. **Signal synthesis runs automatically** after data pull. Produces 
   the weekly intelligence brief and flags operators whose engagement 
   pattern has changed.
3. **Skill triggers based on campaign timeline:**
   - T-21 days: score-and-tier runs for all operators on the attendee 
     list. New Tier 1 operators get flagged for profile research.
   - T-14 days: pre-event-sequence runs for all Tier 1 and Tier 2 
     operators with completed profiles.
   - T+2 days: post-event-followup runs for all operators with 
     engagement data.
   - T+7 days: signal synthesis runs post-event to capture the full 
     engagement picture.
4. **Human review gate:** All generated content goes to a review 
   queue before sending. The system drafts. Humans approve and edit.

### Content Delivery
Generated emails are pushed to the email platform as drafts (not sent 
automatically). Generated one-pagers are rendered as PDFs via a 
template. Generated landing page copy is pushed to the CMS as a draft 
page. The growth team reviews, edits if needed, and publishes.

## Feedback Layer (Phase 3)

### Performance Tracking
After each campaign cycle, actual performance data (which emails were 
opened, which CTAs converted, which deals advanced) flows back into 
the system. This enables:

- **Proof point performance tracking:** Over three campaigns, we know 
  which proof points drive the most engagement by persona type, acuity 
  mix, and operator size. The skills can then select proof points based 
  on historical performance, not just logical matching.
- **Subject line testing:** With enough volume, A/B test subject line 
  approaches (problem-led vs. proof-led vs. ask-led) and feed the 
  results into the email skills.
- **Persona response patterns:** Track which personas engage at which 
  stage. If VPs of IT consistently engage at Touch 1 but COOs don't 
  engage until Touch 2, the skills can adjust timing and sequence 
  structure per persona.

### Skill Iteration
Skills are markdown files. Changes are tracked in git. After each 
campaign cycle, the signal synthesis report identifies what worked 
and what didn't. Those insights become skill updates:

- "Touch 3 subject lines with a direct meeting ask underperform" 
  becomes a rule in pre-event-sequence.md
- "Aquinas adoption proof point works in email but not in ads" 
  becomes a proof point selection rule
- "Stalled deals re-engage better with product update hooks than 
  with conference timing hooks" becomes a path refinement

The git history becomes the institutional memory of what the growth 
engine has learned.

## What This Gets You

After three conference cycles with real data:
- A targeting model that gets sharper every cycle
- Creative and proof point selection backed by performance data
- Personalization that scales to the full attendee list without 
  proportional headcount
- An institutional knowledge base that persists when people leave
- A measurable CAC per operator tier and per conference

The system doesn't replace the growth team. It gives the growth team 
a force multiplier that compounds.
