# Phase 3 — Architecture Hardening (5–10 Days)

## Objective
Reduce attack surface via network segmentation and guardrails.

---

## Tasks Checklist

### 1) Lambda Network Hardening
- [ ] Move Lambda functions to VPC private subnets
- [ ] Assign security groups
- [ ] Restrict outbound access where possible

### 2) VPC Endpoints
- [ ] Configure endpoints for:
  - S3
  - DynamoDB
  - Secrets Manager
  - CloudWatch Logs
- [ ] Reduce dependency on NAT gateway

### 3) Guardrails
- [ ] Enable GuardDuty
- [ ] Enable SecurityHub
- [ ] Add SCPs if Organizations used

---

## Evidence to Capture
- Screenshot: Lambda VPC configuration
- Screenshot: VPC endpoints list
- SecurityHub/GuardDuty enabled screenshot
