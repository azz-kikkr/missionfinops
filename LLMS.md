# LLMS.md

This is a repo-root summary for AI agents and humans browsing the MissionFinOps website repository. The web-facing version lives at /agents.md.

## Quick facts

- **What:** MissionFinOps is an AWS bill-understanding and FinOps advisory practice. Kulshan v0.1 is its free, open-source, local-first AWS bill investigation CLI.
- **Maintainer:** MissionFinOps (Mission, BC, Canada).
- **License:** Apache 2.0. The IAM policy file is additionally offered under CC BY 4.0.
- **Cloud:** AWS only.
- **Domain:** missionfinops.com

## Repo orientation

This repository contains the MissionFinOps website (GitHub Pages). Key files:

- [`index.html`](index.html): MissionFinOps practice homepage and Kulshan free CLI entry point
- [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json): read-only IAM policy
- [`kulshan/iam/per-check/`](kulshan/iam/per-check/): per-pack IAM policies
- [`samples/sample-report.html`](samples/sample-report.html): synthetic-data sample report
- [`samples/sample-report.json`](samples/sample-report.json): synthetic JSON sample artifact
- [`agents.md`](agents.md): web-facing agent summary
- [`llms.txt`](llms.txt): llms.txt-spec sitemap
- [`CNAME`](CNAME): custom domain configuration

## Positioning

Kulshan v0.1 produces local AWS bill investigation evidence. MissionFinOps is the advisory work that helps teams turn that evidence into ownership, decisions, and operating rhythm.

## Current Kulshan v0.1 capabilities

Current public artifacts support these claims:

- Local-first AWS bill investigation workflow.
- Read-only AWS API posture through the published IAM policy.
- AWS Cost Explorer API coverage in the policy, including cost and usage, anomaly history, forecasts, RI/SP utilization, and recommendations.
- Basic sample report artifacts in HTML and JSON.
- Early cost investigation signals for human review.
- No telemetry, hosted account, or data upload claims in public copy.

Kulshan should not be positioned as a generic cloud hygiene scanner, cleanup tool, idle resource finder, or broad waste scanner. Waste belongs in the copy only when it supports bill investigation and evidence-backed follow-up.

## Roadmap / not yet current

The changelog describes these as v0.2 or future-facing items:

- SQLite scan history with score deltas.
- Deeper cost checks.
- AWS Tax rollup.
- Richer HTML report visualizations, if they ship.
- TOML config support, if confirmed.

Avoid presenting these as shipped unless current CLI code confirms them.

## What Kulshan does NOT do

- It does not write to AWS. The published IAM policy contains read-style actions and no Put, Create, Update, Modify, or Delete actions.
- It does not handle PHI, ePHI, or regulated customer data.
- It is not a compliance certification or substitute for a security officer.
- It does not phone home, send telemetry, or require a SaaS account.
- It is not multi-cloud. AWS only.

## Trust signals

- The full read-only IAM policy is at [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json). SHA256 hash and verification are at https://missionfinops.com/policy/.
- The sample report at [`samples/sample-report.html`](samples/sample-report.html) uses synthetic fixture data.
- The IAM policy is published under CC BY 4.0. Reuse is invited.

## What this file is for

`LLMS.md` lives at the repo root as the orientation summary for agents browsing the codebase. The web-facing equivalent is /agents.md.
