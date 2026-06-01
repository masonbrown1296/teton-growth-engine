# Skill: Post-Event Follow-Up

## Purpose
Generate personalized follow-up emails after the conference, informed by 
engagement data and any sales conversation that happened at the event.

## Inputs to Read
1. All brand/ files
2. The operator's profile.md and contacts.md
3. ALL engagement/ data (meta, linkedin, email, website)
4. ALL sales/ data (call notes, form fills, hubspot record)
5. The campaign's context.md

## Signal Scoring

Before writing emails, score each contact's engagement depth. This 
determines the CTA intensity and follow-up urgency.

### Engagement Depth Score
For each contact, count signals across channels:

**High-value signals (3 points each):**
- Clicked meeting booking link
- Submitted a demo request form
- Visited pricing page
- Had a sales conversation (intro call, booth meeting)

**Medium-value signals (2 points each):**
- Clicked through an email to a specific page
- Visited a case study page
- Clicked a retargeting ad more than once
- Downloaded a whitepaper or resource
- Multiple website sessions (2+)

**Low-value signals (1 point each):**
- Opened an email but didn't click
- Single retargeting ad click
- Liked or engaged with a LinkedIn post
- Single website session under 2 minutes

### Engagement Depth Tiers
- **Hot (8+ points):** This contact is actively evaluating. CTA should be 
  specific and time-bound: book a demo this week, schedule a live community 
  visit, send a custom ROI projection.
- **Warm (4-7 points):** This contact is interested but not yet in buying 
  mode. CTA should offer value: send a relevant case study, share the 
  technical whitepaper, introduce them to a peer operator.
- **Cool (1-3 points):** This contact has shown surface interest. CTA 
  should be low-friction: send a single resource, keep them on the 
  nurture list. Do not push for a meeting.
- **No engagement (0 points):** Do not send a follow-up unless they 
  were part of a sales conversation at the event. Unsolicited follow-ups 
  to contacts who showed zero engagement waste credibility.

## Cross-Reference Process

For each contact who qualifies for a follow-up:
1. What ads did they click? (tells you which proof points resonate)
2. What emails did they open/click? (tells you which topics interest them)
3. What pages did they visit on the website? (tells you how deep they are)
4. What was discussed in any sales conversation? (tells you their specific 
   pain and objections)

Synthesize these signals into a SINGLE narrative for each contact. 
The follow-up email should feel like it was written by someone who 
understands their situation, not generated from a template.

## Contact Classification

### Champions (high engagement, positive signals)
Contacts who are actively engaging, clicking through to deep content, 
and showing buying behavior (pricing page, demo request, meeting booking). 
These contacts get the most personalized follow-up with the strongest CTA.

### Researchers (moderate engagement, information-gathering signals)
Contacts who are reading content but not taking action. Multiple website 
sessions, case study views, whitepaper downloads, but no demo request 
or meeting booking. These contacts get value-forward follow-ups that 
give them more of what they're already consuming.

### Connectors (light engagement, social signals)
Contacts whose engagement is primarily social (LinkedIn likes, single 
email opens) and who may not be the buyer but could influence internally. 
Often CMOs, VPs of Marketing, or people adjacent to the decision. 
Follow-up should give them shareable content.

### Blockers (on sales calls but not engaging digitally)
Contacts who attended a sales conversation but show low or no digital 
engagement afterward. They may have concerns they didn't voice or may 
be the person who needs convincing before the champion can move forward. 
Follow-up should address their likely objections (implementation burden 
for operations people, cost for finance people, staff disruption for 
clinical people) without being defensive.

### Ghosts (had prior relationship, zero current engagement)
Contacts from stalled deals who did not engage with the pre-event 
campaign and did not attend any conference interaction. Do NOT send a 
follow-up. They have opted out with their behavior. Add them to a 
long-cycle nurture (quarterly proof point emails) and wait for a 
re-engagement signal.

## Proof Point Selection

Cross-reference the proof points used in the pre-event email sequence 
with what the contact actually engaged with. If they clicked through 
to the Sagora case study, the follow-up can reference Sagora but should 
add depth (specific data they haven't seen yet). If they ignored the 
Sagora email but clicked the Aquinas email, pivot to Aquinas.

Do NOT repeat the same proof point at the same depth. If the pre-event 
email said "74% fewer falls," the follow-up should go deeper: "74% fewer 
falls, and when we look at the night shift data specifically, response 
times improved 95%." Add a layer, don't echo.

## For ALL Follow-Ups
- Send within 48 hours of event close
- Under 200 words
- One specific CTA matched to engagement depth tier
- Reference the conference naturally ("Great seeing the Benchmark team 
  at NIC" or "Wanted to follow up from NIC")
- No em dashes
- Never use "just following up" or "circling back"

## Output Format
One section per engaged contact. Include:
- Contact name and title
- Engagement depth score (with breakdown)
- Contact classification (Champion, Researcher, Connector, Blocker, Ghost)
- Signal summary (what they engaged with, in 2-3 bullets)
- Email: subject line + body
- For Ghosts: note "No follow-up recommended" with rationale

## Output Location
Save to the operator's output/ folder as post-event-followup.md
