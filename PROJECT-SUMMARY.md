# Project Summary — AWS Compliance & Security Hardening (Anonymized)

## Overview
This repository is an anonymized AWS compliance case study based on an AWS Config compliance report.  
It documents key security gaps and a phased remediation roadmap to improve audit readiness and security posture.

## Baseline Snapshot
- AWS Config Rules Assessed: 22
- Resources Evaluated: 333
- Compliance Rate: 39.9%
- Non-Compliant Resources: 200

## Key Findings (Risk-Based)
**P0 Critical**
- CloudTrail governance/audit logging gaps
- CloudWatch log groups not encrypted
- IAM users without MFA enforcement
- Root account security posture issue
- S3 public access control misconfiguration

**P1 High**
- DynamoDB tables missing KMS encryption
- EBS encryption-by-default disabled
- Lambda functions not deployed in VPC (segmentation gap)

## Remediation Plan
**Phase 1 (0–24h):**
Root MFA + IAM MFA enforcement, CloudTrail enablement, S3 public access fixes, enable EBS default encryption

**Phase 2 (2–5d):**
KMS encryption for CloudWatch log groups, IAM cleanup, DynamoDB encryption migration plan

**Phase 3 (5–10d):**
Lambda → VPC private subnets, VPC endpoints, governance guardrails (SecurityHub/GuardDuty/SCPs if applicable)

## Skills Demonstrated
AWS Config compliance analysis, security-first prioritization (P0/P1), IAM governance, audit readiness (CloudTrail),
KMS encryption baselines, S3 security posture, remediation planning.

## Disclaimer
Client/account identifiers are removed. Content is shared for learning and professional showcasing only.
