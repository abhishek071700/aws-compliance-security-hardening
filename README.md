# AWS Compliance & Security Hardening — AWS Config Case Study (Anonymized)

A structured AWS compliance and security hardening case study based on an anonymized AWS Config Compliance report.

This repository documents:
- baseline compliance posture (before)
- key risk findings (P0/P1)
- remediation roadmap (phased)
- implementation notes/templates (reference)

> ✅ Client-safe / anonymized  
> ✅ Educational case study + professional documentation  
> ❌ No account IDs, ARNs, bucket names, IAM usernames

---

## 🎯 Objective

To analyze an AWS Config compliance report and create a practical remediation plan for improving AWS security posture across:
- IAM governance (MFA, root hardening)
- Audit readiness (CloudTrail)
- Encryption baselines (CloudWatch Logs, DynamoDB, EBS)
- Public exposure prevention (S3)
- Network posture improvements (Lambda in VPC)

---

## 📌 Scope

- **Region:** ap-south-1
- **Rules evaluated:** 22
- **Resources evaluated:** 333

---

## 📊 Baseline Compliance Snapshot (Before)

| Metric | Value |
|---|---|
| Compliance Rate | **39.9%** |
| Compliant Rules | 2 |
| Non-Compliant Rules | 20 |
| Total Resources | 333 |
| Non-Compliant Resources | 200 |

---

## 🔥 Key Findings (Risk-Based)

### P0 — Critical
- CloudTrail governance gap (audit logging missing/incomplete)
- CloudWatch Log Groups not encrypted at rest
- IAM users without MFA enforcement
- Root account security posture non-compliant
- S3 Public Access Block misconfiguration (high risk exposure)

### P1 — High
- DynamoDB tables not encrypted with AWS KMS
- EBS encryption-by-default disabled
- Lambda functions not deployed inside VPC (segmentation gap)

---

## 🛠️ Remediation Roadmap

### Phase 1 — Quick Wins (0–24h)
- Root MFA enablement + root hardening
- Enforce IAM MFA policy
- Enable CloudTrail (multi-region + validation)
- Fix S3 public access controls
- Enable EBS encryption by default

### Phase 2 — Security Baseline (2–5 days)
- Encrypt CloudWatch logs using KMS
- IAM cleanup (stale users/keys)
- DynamoDB encryption migration plan

### Phase 3 — Architecture Hardening (5–10 days)
- Move Lambda functions into VPC private subnets
- Configure VPC endpoints for AWS services
- Add guardrails (SecurityHub, GuardDuty, SCPs where applicable)

---

## 📁 Repository Structure

- `0-baseline/` → baseline summary, findings, evidence
- `1-remediation-plan/` → phased remediation plan
- `2-implementation/` → implementation notes + templates (reference)
- `3-results/` → before/after tracker + evidence slots
- `templates/` → executive summary + anonymization checklist

---

## ✅ Skills Demonstrated

- AWS compliance report analysis (AWS Config)
- Security-first remediation planning (P0/P1 prioritization)
- IAM governance & MFA enforcement understanding
- Audit readiness concepts (CloudTrail)
- Encryption baselines (KMS, EBS, DynamoDB)
- S3 public exposure prevention
- Cloud architecture hardening approach (Lambda → VPC)

---

## 🔒 Disclaimer

This repository is published for learning and professional showcasing only.
All details are anonymized to maintain confidentiality.
