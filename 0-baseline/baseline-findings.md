# Baseline Findings — AWS Config Compliance (Anonymized)

This document captures major security and compliance gaps identified in the baseline AWS Config compliance report.

---

## Baseline Overview

- **Region:** ap-south-1
- **Total Rules:** 22
- **Total Resources Checked:** 333
- **Compliance Rate:** 39.9%
- **Non-Compliant Resources:** 200

---

## Findings Summary (P0 / P1)

### P0 — Critical Findings
| Finding | Why it matters | Impact |
|---|---|---|
| CloudTrail governance gap | Audit visibility missing | Incident forensics becomes impossible |
| CloudWatch logs unencrypted | Logs contain sensitive metadata | High breach impact |
| IAM MFA gaps | Password-only access exists | Account compromise risk |
| Root posture issue | Root is ultimate privilege | Full account takeover possible |
| S3 public access misconfig | Common breach vector | Accidental data exposure risk |

### P1 — High Findings
| Finding | Why it matters | Impact |
|---|---|---|
| DynamoDB not encrypted with KMS | Weak encryption baseline | Data-at-rest risk |
| EBS default encryption disabled | Unencrypted volumes possible | Compliance + data leak risk |
| Lambda not in VPC | Weak segmentation | Governance + outbound control risk |

---

## Recommended Priority Fix Order

1) Root MFA + IAM MFA enforcement  
2) CloudTrail enablement (multi-region, validation)  
3) CloudWatch log encryption using KMS  
4) S3 Block Public Access corrections  
5) EBS encryption-by-default  
6) DynamoDB encryption migration  
7) Lambda network hardening (VPC + endpoints)
