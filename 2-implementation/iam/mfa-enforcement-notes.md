# IAM MFA Enforcement Policy — Usage Notes (Reference)

This document explains how to safely apply the MFA enforcement policy:
`enforce-mfa-policy.json`

⚠️ The policy uses **Deny** logic. A wrong attachment can lock users out.

---

## Objective

Enforce that IAM users must enable MFA before performing any AWS actions.

This reduces the impact of:
- password leaks
- credential stuffing
- compromised access keys (partial mitigation)

---

## Policy Behavior (Important)

The policy denies **all actions** unless MFA is present, except a limited set of actions required to:
- set up MFA
- view user/MFA devices
- request STS session tokens
- change password

Meaning:
✅ Without MFA → user can only do MFA setup actions  
✅ With MFA → user can work normally

---

## Where to Attach the Policy (Best Practice)

✅ Recommended:
- Create a group: `RequireMFA`
- Attach this policy to that group
- Add IAM users to that group

Avoid attaching directly to:
- root (not applicable)
- roles
- service accounts used by automation

---

## Safe Rollout Plan (No Lockouts)

### Step 1 — Test with 1 user
1. Create `test-mfa-user`
2. Add it to group `RequireMFA`
3. Ensure user can still:
   - login
   - setup MFA
   - after MFA: access console/services

### Step 2 — Gradual rollout
- move users in small batches (2–5 users)
- confirm MFA enrolled
- then add remaining users

### Step 3 — Cleanup
- remove IAM users not needed
- rotate/revoke unused access keys
- move to AWS IAM Identity Center (SSO) for long term

---

## How to Validate (Proof Checklist)

After rollout:
- IAM credential report shows MFA enabled for all active users
- AWS Config MFA rule becomes compliant
- No users with active access keys without MFA

---

## Common Mistakes (Avoid These)

❌ Attaching the policy to admin users before they enroll MFA  
→ they get blocked and panic starts.

❌ Applying to automation users/service accounts  
→ pipelines break immediately.

❌ No emergency access plan  
→ you waste hours fixing lockouts.

---

## Emergency Access Tip (Professional)

Keep ONE break-glass admin user:
- strong password stored securely
- MFA enabled
- access keys disabled unless required
- monitored for usage

This is standard security practice.
