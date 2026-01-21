# Remediation Roadmap (Phased)

This roadmap prioritizes fixes based on risk reduction and fast compliance uplift.

---

## Phase 1 — Quick Wins (0–24 hours)
**Goal:** close P0 issues immediately.

- Root MFA + root hardening
- Enforce IAM MFA policy
- Enable CloudTrail (multi-region + validation)
- Fix S3 Block Public Access misconfiguration
- Enable EBS encryption by default

---

## Phase 2 — Security Baseline (2–5 days)
**Goal:** encryption + hygiene standardization.

- Encrypt CloudWatch log groups using KMS
- Set log retention standards
- IAM cleanup (unused users/keys)
- DynamoDB encryption migration plan

---

## Phase 3 — Architecture Hardening (5–10 days)
**Goal:** reduce attack surface and add guardrails.

- Move Lambda to VPC private subnets
- Configure VPC endpoints (S3, DynamoDB, Secrets Manager, etc.)
- Enable SecurityHub + GuardDuty
- Add SCP guardrails (if Organizations used)
