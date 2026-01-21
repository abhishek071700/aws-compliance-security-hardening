# Client-Safe Anonymization Checklist

Before publishing:
- [ ] Remove AWS Account ID from screenshots/PDF
- [ ] Remove ARNs from screenshots/PDF
- [ ] Remove IAM usernames
- [ ] Remove bucket names
- [ ] Remove IPs/domains/VPC IDs
- [ ] Replace with placeholders like:
  - AWS_ACCOUNT_ID
  - BUCKET_NAME
  - IAM_USER
  - VPC_ID

Golden rule:
> If it can help an attacker, remove it.
