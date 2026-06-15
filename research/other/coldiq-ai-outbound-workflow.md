# ColdIQ — AI-Powered Outbound Workflow

**Source**: ColdIQ Blog (https://coldiq.com/blog/)
**Authors**: Michel Lieben (CEO), Kenny Damian (Head of GTM), Alex Vacca
**Date**: April 2026

## The 6-API Claude Code Stack

ColdIQ runs outbound campaigns for 70+ B2B clients entirely through Claude Code. Kenny Damian built a full outbound campaign targeting 300 SaaS companies in under 20 minutes. The stack:

### API Layer 1: Company Sourcing — AI Ark
- 70M+ company database
- Filter by industry, size, tech stack, geography, growth signals
- Output: raw company list matching ICP criteria

### API Layer 2: Buying Signals — PredictLeads
- Layers real-time signals on top of the company list
- Key signals: hiring spikes, tech stack changes, funding rounds, geographic expansion
- Purpose: stop emailing companies that aren't ready. Focus on those actively building the team or stack your product supports.

### API Layer 3: Contact Enrichment — BlitzAPI
- Maps the buying committee inside each flagged account
- Returns verified decision-maker contacts with titles, emails, and LinkedIn profiles

### API Layer 4: Email Discovery — Limadata + FullEnrich
- Waterfall email enrichment: start with highest-confidence provider, cascade through alternatives for gaps
- This is the approach ColdIQ uses across all campaigns — verify at each layer to keep bounce rates under 3%

### API Layer 5: Campaign Launch — Instantly.ai
- Push finished campaign directly from Claude Code to Instantly
- Handles sending, warmup, rotation, and deliverability monitoring

### The Workflow in Practice
1. Define ICP in Claude Code (industry, size, signals)
2. Claude Code calls AI Ark → returns company list
3. Claude Code calls PredictLeads → filters by active buying signals
4. Claude Code calls BlitzAPI → identifies decision makers
5. Claude Code calls Limadata/FullEnrich → finds and verifies emails
6. Claude Code generates email copy (or uses templates)
7. Claude Code pushes campaign to Instantly → ready to send

**Total time**: ~20 minutes for a 300-company campaign

### ICP + Signal Mapping with Clay
ColdIQ also uses Clay for more complex workflows:
- Build Clay tables using real-time signals
- Signals tracked: hiring activity, funding rounds, tech stack changes, geographic expansion
- Each signal maps to a specific email angle

### Alternatives
- CompanyEnrich (database layer alternative)
- LeadsFactory (real-time contact lookups)
- Prospeo (email coverage alternative)
- Lemlist (multichannel sending alternative)

## Key Takeaway for Playbook
The ColdIQ approach represents the most automated end of the cold outreach spectrum. Compare with Jack Reamer's fully human approach at SalesBread. A complete playbook should include both: AI automation for Tier 2-3 prospects, human personalization for Tier 1 accounts.

## Source
- "The 6 APIs That Turn Claude Code Into a Cold Email Engine" (April 2026)
- "How Claude Code Builds an Entire Outbound Campaign in Under 20 Minutes"
- ColdIQ Sales Tech Lab Newsletter
- ColdIQ blog on cold email automation
