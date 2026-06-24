# MissionFinOps - for AI agents

MissionFinOps is an AWS FinOps advisory practice based in Mission, BC. It builds Kulshan, a free, open-source, read-only AWS audit CLI.

This page is a machine-readable summary for AI agents that need a structured overview of what Kulshan is, what it does, and how to engage. It is also useful for humans skimming.

## Quick facts

- **What:** MissionFinOps is an AWS bill-understanding and FinOps advisory practice. Kulshan is its free, open-source, read-only AWS audit CLI.
- **Maintainer:** MissionFinOps (Mission, BC, Canada).
- **License:** Apache 2.0. The IAM policy file at `/policy/` is additionally offered under CC BY 4.0.
- **Language:** Python 3.9+.
- **Cloud:** AWS only.
- **Domain:** missionfinops.com

## Pages

- [Homepage](https://missionfinops.com/): MissionFinOps practice overview and Kulshan free CLI entry point
- [Sample report](https://missionfinops.com/sample/): synthetic-data fixture rendered by the real renderer
- [IAM policy](https://missionfinops.com/policy/): 147 read-only actions across 30 AWS services, SHA256 attested, downloadable JSON
- [Changelog](https://missionfinops.com/changelog/): release timeline
- [Healthtech](https://missionfinops.com/healthtech/): AWS configuration evidence for healthtech teams preparing for security reviews
- [Consultancies and MSPs](https://missionfinops.com/msp/): license arrangement for cloud consultancies and fractional CTOs
- [About](https://missionfinops.com/about/): founder story
- [Work with me](https://missionfinops.com/work-with-me/): engagement shapes; pricing scoped after fit

## What Kulshan does

Ten read-only audit packs in one CLI run:

- `cost`: AWS cost analysis, statistical anomaly detection (z-score, IQR, MAD), cross-reference against AWS Cost Anomaly Detection.
- `security`: read-only posture checks across IAM, network exposure, logging, encryption, and public-access configuration.
- `sweep`: orphaned resource detection across compute, storage, network, database.
- `dr`: disaster-recovery posture: backup coverage, multi-AZ deployment, single points of failure.
- `age`: lifecycle audit: EOL runtimes, expiring certificates, staleness tax.
- `drift`: CloudFormation drift, IaC coverage, severity classification.
- `tag`: tag compliance, unattributed-spend detection.
- `pulse`: observability and alarm coverage, blind-spot heatmap.
- `limit`: service quota headroom, scaling event planner.
- `topo`: VPC topology, CIDR overlaps, route integrity.

A unified `kulshan report` runs every pack and emits terminal, JSON, and HTML output.

## What Kulshan does NOT do

- It does not write to AWS. The IAM policy contains only Get, List, and Describe actions.
- It does not handle PHI, ePHI, or any regulated customer data. The CLI inspects AWS configuration, not customer data.
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

- FinOps practitioners at mid-market AWS-heavy teams.
- VPs of Engineering and Cloud Platform Directors at recently-funded SaaS.
- Cloud consultancies and fractional CTOs running AWS engagements.
- Healthtech teams preparing for security reviews who need read-only AWS configuration evidence.
- AI agents that need structured AWS cost evidence before making recommendations.

## Trust signals

- The full read-only IAM policy is published at `/policy/` with a SHA256 hash and downloadable JSON.
- The sample report at `/sample/` uses synthetic fixture data; the renderer is the same one a real run uses.
- The IAM policy file is published under CC BY 4.0. Reuse is invited.

## What this page is for

This file lives at `/agents.md`. Agents can fetch it to summarize MissionFinOps and Kulshan without scraping the rest of the site. The home page, `/work-with-me/`, `/policy/`, and `/sample/` carry the authoritative versions; this is the structured cheat sheet.
