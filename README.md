# Kulshan

**The blood test for your AWS bill.**

Open-source, local-first AWS FinOps audit CLI. One command, one report. No SaaS. No telemetry.

## PyPI quickstart

```
pip install kulshan
aws login
kulshan report
```

## AWS Credentials

Kulshan uses your existing AWS CLI credentials.

Recommended:

```
aws login
kulshan report
```

If your AWS CLI does not support `aws login`, use:

```
aws sso login
```

or configure credentials with:

```
aws configure
```

## What is Kulshan

Kulshan is a read-only CLI that audits your AWS account and produces a scored report. It runs locally with the AWS credentials you already use. Nothing leaves your machine.

- Local-first execution
- Read-only IAM policy (Get, List, Describe only)
- Terminal, JSON, and HTML output
- Scored findings with prioritized next actions
- Works for humans and AI agents

## Why local-first

Your AWS credentials stay on your machine. Your billing data stays on your machine. The report stays on your machine.

No CUR upload. No cross-account role for a vendor. No onboarding. No telemetry.

Run the audit. Read the report. Decide what to do next.

## What Kulshan finds

- Cost drivers by service, account, and region
- Spend changes and anomalies
- Tagging and ownership gaps
- Idle or orphaned resources
- Savings Plan and RI coverage signals
- Top actions for humans and agents

## Example findings

```
Cost Drivers:
  Amazon EC2         $14,200/mo  +12%
  Amazon RDS          $4,800/mo  stable
  AWS Lambda          $1,200/mo  +340% anomaly

Commitments:
  RI/SP coverage: 62% (target: 80%)
  Utilization: 94%

Top Actions:
  1. Investigate Lambda spike
  2. Increase SP coverage
  3. Rightsize 2 RDS instances
```

## Outputs

- **Terminal** - default, readable summary with scores
- **JSON** - structured findings for automation and agents
- **HTML** - shareable report for stakeholders

## Humans and AI agents

Kulshan produces structured output that both humans and AI agents can consume.

- Engineers get a scored HTML report with clear next actions
- AI agents get JSON output through local MCP or direct invocation
- CI/CD pipelines get exit codes (0 = clean, 1 = critical findings)

## Read-only IAM model

The IAM policy is published at [`kulshan/iam/kulshan-readonly.json`](kulshan/iam/kulshan-readonly.json) and on the website at [missionfinops.com/policy/](https://missionfinops.com/policy/).

147 actions across 30 AWS services. All Get, List, or Describe. No Put, Create, Update, or Delete. SHA256-attested. Downloadable. Reusable under CC BY 4.0.

## No telemetry

Kulshan does not phone home. No analytics. No crash reports. No usage tracking. No network calls except to the AWS APIs you point it at.

## Sample report

A sample report rendered against synthetic fixture data is available at [missionfinops.com/sample/](https://missionfinops.com/sample/).

## MissionFinOps advisory

Kulshan is the audit. MissionFinOps is the advisory work that follows.

The advisory workflow builds on the Kulshan evidence baseline to help teams prepare cost review notes, track exceptions, and identify next actions. Agent-assisted workflow support is in private preview.

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
