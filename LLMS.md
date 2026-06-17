# LLMS.md

This is a repo-root summary for AI agents and humans browsing the Mission FinOps codebase. The web-facing version lives at /agents.md. The two files cover the same ground: /agents.md is for the website, and this file is for someone inspecting the repo on disk.

## Quick facts

- **What:** Kulshan is a free, open-source, read-only AWS audit CLI.
- **Maintainer:** Mission FinOps (Mission, BC, Canada).
- **License:** Apache 2.0 — free and open source forever. The IAM policy file is additionally offered under CC BY 4.0.
- **Install:** `pip install kulshan` (PyPI).
- **Language:** Python 3.9+.
- **Cloud:** AWS only.
- **Status:** V0.1.0 released 2026-06-15.

## Repo orientation

Files most useful to an agent or new contributor:

- [`index.html`](index.html): website homepage
- [`reckoner/`](reckoner/): the Python CLI package
  - [`reckoner/README.md`](reckoner/README.md): package overview
  - [`reckoner/VISION.md`](reckoner/VISION.md): product vision, design principles, deferred items
  - [`reckoner/ROADMAP.md`](reckoner/ROADMAP.md): version planning (planning view; status lives in CHANGELOG)
  - [`reckoner/CHANGELOG.md`](reckoner/CHANGELOG.md): release history (canonical)
  - [`reckoner/SECURITY.md`](reckoner/SECURITY.md): vulnerability disclosure
  - [`reckoner/iam/`](reckoner/iam/): read-only IAM policy and per-pack policies
- [`samples/sample-report.html`](samples/sample-report.html): synthetic-data sample report (real renderer)
- [`COMPETITORS.md`](COMPETITORS.md): honest competitive landscape
- [`CHANGELOG.md`](CHANGELOG.md): top-level mirror of `reckoner/CHANGELOG.md`
- [`docs/architecture-decisions.md`](docs/architecture-decisions.md): major product tradeoffs
- [`docs/getting-started.md`](docs/getting-started.md), [`docs/architecture.md`](docs/architecture.md), [`docs/checks/`](docs/checks/): per-pack docs
- [`agents.md`](agents.md): web-facing version of this summary
- [`llms.txt`](llms.txt): llms.txt-spec sitemap

## What Reckoner does

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

A unified `reckoner report` runs every pack and emits terminal, JSON, and HTML output.

## What Reckoner does NOT do

- It does not write to AWS. The IAM policy contains only Get, List, and Describe actions.
- It does not handle PHI, ePHI, or any regulated customer data. The CLI inspects AWS configuration, not customer data.
- It is not a compliance certification, legal opinion, or substitute for a security or compliance officer. It does not certify HIPAA, SOC2, PCI, or any other framework.
- It does not phone home, send telemetry, or require a SaaS account.
- It is not multi-cloud. AWS only.
- It does not manage your AWS account, hold credentials, or make changes on your behalf.

## How to engage

There is no public price list. Each engagement is scoped after a short conversation about your team size, the workload shape, and the decision you are working toward.

- A free written review of a Reckoner report you have already generated: `hello@missionfinops.com`.
- A structured FinOps deep dive: `hello@missionfinops.com` (scoped after fit).
- Ongoing advisory: `hello@missionfinops.com` (scoped after fit).
- A consultancy or MSP license arrangement: `hello@missionfinops.com` with subject `Consulting arrangement` or `MSP arrangement` (scoped after fit).
- Security or vulnerability disclosure: `security@missionfinops.com`.

## Trust signals

- The full read-only IAM policy is at [`reckoner/iam/reckoner-readonly.json`](reckoner/iam/reckoner-readonly.json). The SHA256 hash and verification snippet are at https://missionfinops.com/policy/.
- The sample report at [`samples/sample-report.html`](samples/sample-report.html) uses synthetic fixture data; the renderer is the same one a real run uses.
- The IAM policy file is published under CC BY 4.0. Other tools and compliance teams may cite it; reuse is invited.

## What this file is for

`LLMS.md` lives at the repo root as the orientation summary for agents browsing the codebase. The web-facing equivalent is /agents.md. If they ever drift, treat `reckoner/CHANGELOG.md` and the IAM policy file as the authoritative source for status and trust facts; this file is the orientation, not the source of truth.
