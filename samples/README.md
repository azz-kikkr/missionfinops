# Sample Reckoner reports

These files demonstrate what `reckoner report` produces. **All data here is
synthetic.** No real AWS account IDs, no real customer data, no real ARNs.

## Files

- [`sample-report.html`](sample-report.html): the rendered HTML report (open in any browser)
- [`sample-report.json`](sample-report.json): the same data as JSON (parseable, pipeable through `jq`)

## Provenance

Generated from the committed fixture files at
`reckoner/tests/fixtures/checks/*.json`. The cost pack fixture contains three
synthetic findings: one critical EC2 anomaly, one high AWS-native overlap, one
medium RDS spike: plus a synthetic AWS Cost Anomaly Detection metadata block.
Other packs contribute scores and grades only.

The placeholder account ID is `000000000000`. Regions are `us-east-1`,
`us-west-2`, `eu-west-1`. Timestamp is frozen at `2026-04-30 12:00:00 UTC`.
Scan duration is frozen at `12.4s`.

## Regenerate

```
python reckoner/scripts/generate_sample_report.py
```

The output is deterministic: running it twice produces byte-identical files.
A pytest drift guard at `reckoner/tests/unit/test_sample_report.py` will fail
if the committed files do not match what regeneration would produce against
the current fixtures and renderer. When that test fails, re-run the script and
commit the updated artifacts.

## Sanitization

Sanitization is enforced on both sides:

- **Inputs:** `reckoner/tests/e2e/test_full_report_snapshot.py` rejects any
  fixture that contains a 12-digit number that is not the all-zeros placeholder.
- **Outputs:** `reckoner/tests/unit/test_sample_report.py` rejects committed
  artifacts that contain non-placeholder account IDs, ARNs with real account
  ids, or email addresses.

## What this is not

- Not a live demo. Numbers do not change.
- Not customer data. There is no source customer.
- Not a marketing page. It is the actual renderer output.
