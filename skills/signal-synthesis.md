# Skill: Signal Synthesis (Weekly Intelligence Brief)

## Purpose
Aggregate engagement data across ALL operators and produce an actionable 
intelligence brief for the growth team and sales team.

## Inputs to Read
1. ALL operator engagement/ folders
2. ALL operator sales/ folders
3. ALL operator hubspot records
4. brand/proof-points.md (to reference which proof points are performing)
5. The campaign's context.md (for timeline awareness)

## Analysis Framework

### Creative Performance Analysis
For each ad creative across all operators:
- Calculate CTR and compare across operators
- Identify whether performance differences are creative-driven or 
  audience-driven (same creative, different CTR by operator = audience 
  difference, not creative problem)
- Flag any creative below 2.0% CTR for review
- Flag any creative above 3.5% CTR for increased investment
- Note which proof points appear in top-performing creatives

### Email Sequence Analysis
For each email touch across all operators:
- Open rate and click rate by touch number (to identify where sequences 
  lose momentum)
- Open rate and click rate by subject line theme (problem, proof, ask)
- Per-contact engagement trajectory (improving, declining, or flat 
  across touches)
- Identify the specific touch where contacts disengage, if applicable

### Website Behavior Analysis
For each identified website session:
- Categorize visitor intent by pages visited:
  - Product pages + pricing = evaluating (high intent)
  - Case studies only = researching (medium intent)
  - Homepage + product overview = exploring (low intent)
  - Privacy/architecture pages = technical diligence (role-specific)
  - Integration pages = stack compatibility check (role-specific)
- Flag contacts with multiple sessions (indicates sustained interest)
- Flag contacts who visited pricing (closest to buying intent)

### Pipeline Health Analysis
For each operator in HubSpot:
- Current stage vs. actual engagement level (flag mismatches, e.g., 
  "new" stage but heavy engagement means stage needs updating)
- Days since last sales-initiated activity vs. days since last 
  contact-initiated activity (a stalled deal where the contact is 
  still engaging is not dead)
- Rep assignment status (unassigned leads with engagement = urgent)

### Champion and Blocker Identification
Across all contacts at each operator:
- **Champion:** Highest engagement score, multiple channels, deep 
  content consumption, or positive sales conversation signals. This is 
  the person to build the relationship through.
- **Potential second champion:** Moderate engagement, different role 
  than the primary champion. Building a second champion de-risks the 
  deal if the primary goes dark.
- **Blocker:** Present in sales conversations but low/no digital 
  engagement afterward. Often the operations person concerned about 
  implementation or the finance person concerned about cost. Name the 
  likely objection based on their role and available sales notes.
- **Unknown influencer:** Unidentified visitors (IP matching only) or 
  contacts engaging from roles not in the target list. Flag for 
  identification and potential addition to the contact list.

## Output Format

### What's Working
- Which ad creatives are performing best (CTR comparison with table)
- Which email subject lines are driving opens and clicks
- Which proof points are generating the most engagement
- Which personas are engaging at the highest rate
- Which channels are most effective per persona type

### What's Not
- Which creatives are underperforming (with hypothesis on why)
- Where leads are stalling in the funnel (and whether the stall is 
  on the sales side or the contact side)
- Which contacts went dark and how long ago
- Mismatches between HubSpot stage and actual engagement level

### Champion/Blocker Map
- Per-operator table: contact, role, classification (champion, 
  researcher, connector, blocker, ghost), engagement score, 
  recommended action

### Pipeline Status
- Per-operator summary: tier, stage, last activity, next recommended 
  action, risk assessment

### Recommendations
- Budget reallocation suggestions based on creative performance 
  (with specific dollar amounts where data allows)
- Content gaps identified (what are people looking for that we 
  don't have? Inferred from engagement patterns.)
- Specific next actions per stalled lead
- New contacts to add to sequences based on engagement signals
- Skills that should be re-run if new data has come in since 
  last generation

## Output Location
Save to the campaign's output/ folder as weekly-report-[date].md
