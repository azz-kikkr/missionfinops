# LLMS.md

This is a repo-root summary for AI agents and humans browsing the MissionFinOps website repository. The web-facing version lives at /agents.md.

## Quick facts

- **What:** Kulshan is a free, open-source, read-only AWS audit CLI.
- **Maintainer:** MissionFinOps (Mission, BC, Canada).
- **License:** Apache 2.0. The IAM policy file is additionally offered under CC BY 4.0.
- **Language:** Python 3.9+.
- **Cloud:** AWS only.
- **Domain:** missionfinops.com

## Repo orientation

This repository contains the MissionFinOps website (GitHub Pages). Key files:

- [`index.html`](index.html): website homepage
- [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json): read-only IAM policy
- [`kulshan/iam/per-check/`](kulshan/iam/per-check/): per-pack IAM policies
- [`samples/sample-report.html`](samples/sample-report.html): synthetic-data sample report
- [`agents.md`](agents.md): web-facing agent summary
- [`llms.txt`](llms.txt): llms.txt-spec sitemap
- [`CNAME`](CNAME): custom domain configuration

## What Kulshan does

Ten read-only audit packs in one CLI run:

- `cost`: AWS cost analysis, statistical anomaly detection, cross-reference against AWS Cost Anomaly Detection.
- `security`: read-only posture checks across IAM, network exposure, logging, encryption.
- `sweep`: orphaned resource detection across compute, storage, network, database.
- `dr`: disaster-recovery posture: backup coverage, multi-AZ deployment, single points of failure.
- `age`: lifecycle audit: EOL runtimes, expiring certificates.
- `drift`: CloudFormation drift, IaC coverage, severity classification.
- `tag`: tag compliance, unattributed-spend detection.
- `pulse`: observability and alarm coverage.
- `limit`: service quota headroom.
- `topo`: VPC topology, CIDR overlaps, route integrity.

A unified `kulshan report` runs every pack and emits terminal, JSON, and HTML output.

## What Kulshan does NOT do

- It does not write to AWS. The IAM policy contains only Get, List, and Describe actions.
- It does not handle PHI, ePHI, or any regulated customer data.
- It is not a compliance certification or substitute for a security officer.
- It does not phone home, send telemetry, or require a SaaS account.
- It is not multi-cloud. AWS only.

## Trust signals

- The full read-only IAM policy is at [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json). SHA256 hash and verification at https://missionfinops.com/policy/.
- The sample report at [`samples/sample-report.html`](samples/sample-report.html) uses synthetic fixture data.
- The IAM policy is published under CC BY 4.0. Reuse is invited.

## What this file is for

`LLMS.md` lives at the repo root as the orientation summary for agents browsing the codebase. The web-facing equivalent is /agents.md.
