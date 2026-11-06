# Longevity Outreach System

A GTM automation workflow built in n8n. It scores longevity practices, runs a 6-touch outreach sequence over 18 days, and reacts to how each prospect behaves.

## What it does

- Sources 75 fictional NYC longevity practices from a fixed seed.
- Scores each practice 0 to 100: decision access 25, digital maturity 25, growth signals 20, product fit 20, size fit 10. Tier A is 80 and up.
- Runs a 6-touch, 18-day sequence: day 1 practice manager email, day 4 LinkedIn connection note to the founder, day 8 mailed one-pager, day 11 take-home example, day 15 video link plus LinkedIn message, day 18 closing email.
- Reacts to behavior: an open adds 4 points, a click adds 8 and pulls the day 11 example forward, a positive reply cancels automation and routes the account to a human, silence through day 11 subtracts 6 and moves the account to monthly nurture.

## Demo data only

Every practice, person, and message here is fictional sample data. The workflow contains no send nodes: every message is written to a file, never sent. In production, sourcing would come from the NPI registry and the CMS provider directory.

## How to use it

1. In n8n, go to Workflows and choose Import from file.
2. Select `Longevity_outreach_system.json`.
3. Run the "Run full pipeline" trigger to score clinics and build messages, or "Run reaction demo" to see the reaction logic.

## Files

- `Longevity_outreach_system.json`: the n8n workflow export (13 nodes, no credentials needed).
