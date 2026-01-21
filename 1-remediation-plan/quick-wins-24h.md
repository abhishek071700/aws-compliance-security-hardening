# Phase 1 — Quick Wins (0–24 Hours)

## Objective
Immediately reduce the highest risks (P0).

---

## Tasks Checklist

### 1) Root Security
- [ ] Enable MFA on root account
- [ ] Remove root access keys (if any)
- [ ] Restrict root usage (billing/emergency only)

### 2) IAM MFA Enforcement
- [ ] Attach MFA enforcement policy
- [ ] Identify IAM users without MFA
- [ ] Force MFA enrollment

### 3) CloudTrail Enablement
- [ ] Enable multi-region CloudTrail
- [ ] Enable log file validation
- [ ] Central encrypted S3 bucket for logs

### 4) S3 Public Access Controls
- [ ] Enable Block Public Access (account + bucket)
- [ ] Audit bucket policies and ACLs

### 5) EBS Encryption Baseline
- [ ] Enable EBS encryption-by-default in region
- [ ] Ensure snapshot encryption standard

---

## Output / Evidence to Capture
- Screenshot: Root MFA enabled
- Screenshot: CloudTrail enabled
- Screenshot: Account-level S3 block public access
- Screenshot: EBS encryption-by-default enabled
