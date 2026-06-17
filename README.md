# Mission FinOps

**One command. Read-only AWS access. Local report. No data egress.**

Mission FinOps is an AWS audit advisory practice. Reckoner is its product: a local-first, read-only CLI that audits your AWS account across ten operational dimensions and produces a scored report — without sending any data off your machine.

## Install

```bash
git clone <repo>
cd mission-finops
bash setup.sh
```

## Quickstart

```bash
reckoner report --quick
```

Produces a scored report covering cost, security, waste, DR readiness, lifecycle, drift, tagging, observability, quotas, and network topology. Output formats: terminal (default), JSON (`--format json`), HTML (`--format html`).

## What Reckoner Is

- Read-only AWS audit CLI (ten check packs in one run)
- Local execution — nothing leaves your machine
- Published IAM policy: 147 read-only actions, SHA256-attested
- Terminal, JSON, and HTML report output
- Scored 0-100 with letter grade per audit dimension
- Exit codes for CI/CD: 0 = clean, 1 = critical findings

## What Reckoner Is Not

- Not a platform, not a dashboard, not a SaaS
- Not multi-cloud (AWS only)
- Not autonomous (read-only — audits and reports, does not modify)
- Not an AI agent (local SLM narration is on the roadmap, not shipped)

## IAM Policy

The read-only IAM policy is published at [`reckoner/iam/reckoner-readonly.json`](reckoner/iam/reckoner-readonly.json) and on the website at [missionfinops.com/policy/](https://missionfinops.com/policy/).

147 actions across 30 AWS services. All Get, List, or Describe. No Put, Create, Update, or Delete.

## Sample Report

A synthetic-data sample report is available at [`samples/sample-report.html`](samples/sample-report.html) and on the website at [missionfinops.com/sample/](https://missionfinops.com/sample/).

## Documentation

- [Reckoner README](reckoner/README.md) — detailed feature list, CLI reference, architecture
- [Changelog](https://missionfinops.com/changelog/) — release timeline
- [IAM Policy](https://missionfinops.com/policy/) — full policy with verification instructions

## License

Kulshan is Apache 2.0 — free and open source. The IAM policy file is additionally offered under CC BY 4.0.

## Contact

- General: hello@missionfinops.com
- Security: security@missionfinops.com
- Web: https://missionfinops.com
