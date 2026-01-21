# Phase 2 — Security Baseline (2–5 Days)

## Objective
Standardize encryption and identity hygiene to improve compliance.

---

## Tasks Checklist

### 1) CloudWatch Log Encryption
- [ ] Create KMS CMK for CloudWatch logs
- [ ] Encrypt existing log groups
- [ ] Apply retention policy (30/90/180 days)

### 2) IAM Cleanup
- [ ] Remove unused IAM users
- [ ] Rotate/remove stale access keys
- [ ] Review least privilege

### 3) DynamoDB Encryption Plan
- [ ] Identify non-encrypted tables
- [ ] Apply CMK encryption for new tables
- [ ] Migration approach:
  - export/import OR streams-based migration

---

## Output / Evidence to Capture
- Screenshot: KMS key created
- Screenshot: Log group encryption enabled
- IAM credential report summary
- DynamoDB encryption proof
