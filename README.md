# Teton Growth Engine

Conference-to-pipeline system that processes operator intelligence and 
multi-channel engagement signals to produce personalized campaign assets.

## Structure

```
teton-growth-engine/
  brand/              <- permanent, evolves slowly
  skills/             <- permanent, evolves slowly
  campaigns/
    nic-fall-2026/    <- one folder per conference cycle
      context.md
      attendee-targets.csv
      operators/
        benchmark-senior-living/
          profile.md, contacts.md
          engagement/   (ad, email, web, linkedin data)
          sales/        (call notes, forms, hubspot)
          output/       (generated assets)
        bickford-senior-living/
          ...same structure
      output/           (cross-operator reports, landing page)
  site/                <- HTML dashboard for viewing outputs
```

Brand layer and skills are shared across all campaigns. Each campaign 
is self-contained with its own operators, engagement data, and outputs.

## How It Works

1. Create a campaign folder under campaigns/
2. Research operators and create profiles
3. Drop engagement signals into each operator's engagement/ folder
4. Add any sales context into their sales/ folder
5. Run a skill against the operator to generate campaign assets

## Available Skills

- score-and-tier: Evaluate and prioritize an operator from the attendee list
- pre-event-sequence: Generate a 3-email pre-conference sequence
- post-event-followup: Generate personalized follow-up based on engagement + sales data
- landing-page-copy: Generate conference landing page copy (default or operator-specific)
- one-pager-brief: Generate a sales leave-behind tailored to the operator
- signal-synthesis: Cross-operator intelligence brief (what's working, what to adjust)

## Running a Skill

claude "Read the skill at skills/pre-event-sequence.md, then read the brand 
layer files in brand/, the operator profile at 
campaigns/nic-fall-2026/operators/benchmark-senior-living/profile.md 
and contacts.md, and any engagement data in their engagement/ folder. 
Generate the pre-event email sequence and save to their output/ folder."

## Viewing Outputs

Open site/index.html in a browser. The dashboard shows all generated 
assets organized by operator with the intelligence report and landing 
page copy.

## Data Notes

- Brand layer and operator profiles contain real, verified research
- Engagement and sales data is SIMULATED for demonstration purposes
- All simulated files are marked with a _SIMULATED.md notice
