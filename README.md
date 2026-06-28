# Kulshan

**Local-first AWS bill investigation CLI.**

Kulshan v0.1 helps explain AWS bill movement locally before deeper FinOps investigation. It runs with your AWS credentials and focuses on what changed, why spend moved, who likely owns the cost, and what evidence supports the answer.

No SaaS account. No telemetry. Read-only AWS API posture.

## v0.1 scope note

This repository snapshot is the public MissionFinOps website and sample artifacts. It includes the read-only IAM policy and synthetic sample report. It does not include the Python package source, so this README avoids claiming CLI flags or runtime behavior that cannot be verified from the files here.

## PyPI quickstart

```bash
pip install kulshan
aws login
kulshan report
```

If your AWS CLI does not support `aws login`, use:

```bash
aws sso login
```

or configure credentials with:

```bash
aws configure
```

## Current capabilities

Supported by the public docs and sample artifacts in this repo:

- Local-first AWS bill investigation workflow.
- Read-only IAM policy published at [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json).
- AWS Cost Explorer API coverage in the IAM policy, including cost and usage, anomaly history, forecasts, RI/SP utilization, and recommendations.
- Synthetic sample report artifacts in HTML and JSON under [`samples/`](samples/).
- Local report output intended for finance and engineering review, ownership discussion, and follow-up investigation.
- No telemetry claim in public copy: no SaaS account, no analytics, no crash reports, and no usage tracking.
- Apache 2.0 open-source positioning. The IAM policy file is additionally offered under CC BY 4.0.

## Roadmap / not yet current

The public changelog lists these as v0.2 or future work, not v0.1 promises:

- SQLite scan history with score deltas.
- Deeper cost checks such as CloudWatch Logs ingestion analysis, S3 request decomposition, AWS Config cost awareness, and cross-AZ data transfer detection.
- AWS Tax rollup for Config, GuardDuty, Security Hub, Inspector, and CloudTrail.
- Richer HTML report visualizations such as Sankey diagrams, cost treemaps, and severity heatmaps, if they ship.
- TOML configuration support, if confirmed.

## What Kulshan is

Kulshan is a free, open-source AWS bill investigation CLI. The v0.1 positioning is deliberately narrow: understand the bill first, capture evidence locally, and decide what needs deeper review.

It is not a hosted platform, a compliance certification, a legal opinion, a managed remediation tool, or a generic cloud cleanup scanner.

## Outputs

This repo includes sample HTML and JSON report artifacts:

- [`samples/sample-report.html`](samples/sample-report.html)
- [`samples/sample-report.json`](samples/sample-report.json)

Treat them as sample artifacts, not a guarantee that every runtime format, flag, or report section is available in every installed version.

## Read-only IAM model

The IAM policy is published at [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json) and on the website at [missionfinops.com/policy/](https://missionfinops.com/policy/).

Every action in the composed policy is a read-style AWS API action such as Get, List, or Describe. The policy includes no Put, Create, Update, Modify, or Delete actions. The policy page publishes a SHA256 hash and downloadable JSON.

## No telemetry

Kulshan does not phone home. No analytics. No crash reports. No usage tracking. No network calls except to the AWS APIs you point it at.

## Sample report

A synthetic sample report is available at [missionfinops.com/sample/](https://missionfinops.com/sample/).

The sample uses fixture data. Real reports reflect your AWS account data. Kulshan v0.1 focuses on local AWS bill investigation evidence and early cost movement signals. Deeper diagnostics and richer report visuals are roadmap items.

## MissionFinOps advisory

Kulshan is the local bill evidence artifact. MissionFinOps is the advisory work that follows.

The advisory workflow builds on Kulshan evidence to help teams prepare cost review notes, track exceptions, and identify next actions.

Interested? hello@missionfinops.com

## Links

- Website: [missionfinops.com](https://missionfinops.com)
- Sample report: [missionfinops.com/sample/](https://missionfinops.com/sample/)
- IAM policy: [missionfinops.com/policy/](https://missionfinops.com/policy/)
- Changelog: [missionfinops.com/changelog/](https://missionfinops.com/changelog/)
- GitHub: [github.com/azz-kikkr/kulshan](https://github.com/azz-kikkr/kulshan)

## License

Kulshan is Apache 2.0. Free and open source. The IAM policy file is additionally offered under CC BY 4.0.

## Contact

- General: hello@missionfinops.com
- Security: security@missionfinops.com
