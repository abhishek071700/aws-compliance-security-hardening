# Baseline Compliance Summary (Before Remediation)

**Region:** ap-south-1  
**Environment:** Test/Non-Prod (Anonymized)  
**Tool:** AWS Config Compliance Rules

---

## Summary Statistics

- Total Config Rules: 22
- Compliant Rules: 2
- Non-Compliant Rules: 20
- Total Resources: 333
- Compliant Resources: 133
- Non-Compliant Resources: 200
- Compliance Rate: **39.9%**

---

## High Impact Gaps (Top 8)

1. CloudTrail audit logging missing/incomplete
2. CloudWatch log groups not encrypted
3. IAM MFA not enforced for multiple users
4. Root account security posture non-compliant
5. DynamoDB tables not encrypted with KMS
6. EBS encryption-by-default disabled
7. Lambda functions not deployed in VPC
8. S3 public access configuration issues

---

## Priority Guidance

**Fix order:** Logging + IAM + Public access + Encryption  
P0 issues should be resolved first to reduce maximum risk exposure quickly.
