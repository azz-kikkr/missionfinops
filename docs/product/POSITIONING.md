# Kulshan Positioning: Bill Investigation, Not Cloud Cleanup

Kulshan is a local-first AWS bill investigation and evidence engine.

It helps explain AWS bill movement before a team jumps into optimization work. The core questions are:

- What changed?
- Why did spend move?
- Who likely owns the cost?
- What evidence supports the answer?

Kulshan should lead with AWS spend explanation, cost evidence, and MTTE: Mean Time To Explanation.

## What Kulshan is

- A local AWS bill investigation CLI.
- A cost evidence engine for finance and engineering conversations.
- A way to create the first local artifact before deeper FinOps review.
- A read-only workflow that uses the customer's AWS credentials.

## What Kulshan is not

- A generic cloud hygiene scanner.
- A cleanup tool.
- An idle resource finder as its primary identity.
- A broad cloud waste scanner.
- A managed remediation platform.

## Messaging Rule

Lead with bill investigation. Waste should appear only where it supports a specific explanation of bill movement or a follow-up investigation path.

CleanCloud-style scanners find idle resources. Kulshan explains AWS cost changes and produces evidence for the people who need to discuss them.

## Conservative v0.1 Claims

Public copy can say Kulshan v0.1:

- Runs locally with the customer's AWS credentials.
- Uses a read-only AWS API posture through the published IAM policy.
- Includes AWS Cost Explorer API coverage in the policy.
- Produces local sample report artifacts in HTML and JSON.
- Surfaces early cost investigation signals for human review.
- Does not require a SaaS account, telemetry, or data upload.

Do not describe roadmap items as shipped unless current CLI code or release notes confirm them.