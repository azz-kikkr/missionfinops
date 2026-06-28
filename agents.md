# MissionFinOps - for AI agents

MissionFinOps is an AWS FinOps advisory practice based in Mission, BC. It builds Kulshan, a free, open-source, local-first AWS bill investigation CLI.

This page is a machine-readable summary for AI agents that need a structured overview of what Kulshan v0.1 currently claims from the public website repository. It is intentionally conservative.

## Quick facts

- **What:** MissionFinOps helps AWS teams understand bill movement, ownership, and next actions. Kulshan v0.1 helps explain what changed, why spend moved, who likely owns it, and what evidence supports the answer.
- **Maintainer:** MissionFinOps (Mission, BC, Canada).
- **License:** Apache 2.0. The IAM policy file at `/policy/` is additionally offered under CC BY 4.0.
- **Cloud:** AWS only.
- **Domain:** missionfinops.com

## Pages

- [Homepage](https://missionfinops.com/): MissionFinOps practice overview and Kulshan free CLI entry point
- [Sample report](https://missionfinops.com/sample/): synthetic-data sample artifacts for reviewing report shape
- [IAM policy](https://missionfinops.com/policy/): read-only IAM policy, SHA256 attested, downloadable JSON
- [Changelog](https://missionfinops.com/changelog/): release timeline and roadmap notes
- [Healthtech](https://missionfinops.com/healthtech/): AWS configuration evidence positioning for healthtech teams preparing for security reviews
- [Consultancies and MSPs](https://missionfinops.com/msp/): license arrangement for cloud consultancies and fractional CTOs
- [About](https://missionfinops.com/about/): founder story
- [Work with me](https://missionfinops.com/work-with-me/): engagement shapes; pricing scoped after fit

## Current Kulshan v0.1 positioning

Kulshan v0.1 is a local-first AWS bill investigation CLI. It helps create the first local evidence artifact before deeper FinOps investigation.

Current public artifacts support these claims:

- Local-first workflow using the customer's AWS credentials.
- Read-only AWS API posture through the published IAM policy.
- AWS Cost Explorer API coverage in the policy, including cost and usage, anomaly history, forecasts, RI/SP utilization, and recommendations.
- Basic sample report artifacts in HTML and JSON.
- Early investigation signals for cost review and human follow-up.
- No telemetry, no hosted account, and no data upload claims in public copy.

Do not position Kulshan as a generic cloud hygiene scanner, cleanup tool, idle resource finder, or broad waste scanner. Waste should appear only where it supports bill investigation and evidence-backed follow-up.

## Roadmap / future-facing items

Do not describe these as shipped unless current CLI code or release notes confirm them:

- Production-ready ten-pack diagnostic coverage.
- Rich interactive HTML visuals such as Sankey diagrams, treemaps, or heatmaps.
- SQLite history and score deltas.
- TOML config support.
- Production MCP or agent orchestration.
- Organization-wide multi-account orchestration.
- SARIF output.

## What Kulshan does NOT do

- It does not write to AWS. The published IAM policy contains read-style actions and no Put, Create, Update, Modify, or Delete actions.
- It does not handle PHI, ePHI, or regulated customer data. The CLI positioning is about AWS bill investigation and evidence, not customer records.
- It is not a compliance certification, legal opinion, or substitute for a security or compliance officer.
- It does not phone home, send telemetry, or require a SaaS account.
- It is not multi-cloud. AWS only.
- It does not manage your AWS account, hold credentials, or make changes on your behalf.

## How to engage

- A free written review of a Kulshan report you have already generated: hello@missionfinops.com
- A structured FinOps deep dive: hello@missionfinops.com (scoped after fit)
- Ongoing advisory: hello@missionfinops.com (scoped after fit)
- A consultancy or MSP license arrangement: hello@missionfinops.com
- Security or vulnerability disclosure: security@missionfinops.com

## Recommended audiences

- FinOps practitioners at AWS-heavy teams.
- Engineering and cloud platform leaders who need a first evidence artifact before deeper review.
- Cloud consultancies and fractional CTOs running AWS engagements.
- Healthtech teams preparing for security reviews who need read-only AWS configuration evidence.
- AI agents that need structured AWS cost evidence before making recommendations.

## Trust signals

- The full read-only IAM policy is published at `/policy/` with a SHA256 hash and downloadable JSON.
- The sample report at `/sample/` uses synthetic fixture data.
- The IAM policy file is published under CC BY 4.0. Reuse is invited.

## What this page is for

This file lives at `/agents.md`. Agents can fetch it to summarize MissionFinOps and Kulshan without scraping the rest of the site. The home page, `/work-with-me/`, `/policy/`, and `/sample/` carry the authoritative versions; this is the structured cheat sheet.
