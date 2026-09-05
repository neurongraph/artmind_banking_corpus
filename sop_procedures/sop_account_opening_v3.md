---
_artmind_id: 01a073f8-2690-77f0-b4e8-5b444f160394
_version: 1
_content_sha256: f95634a93e67aa34be82e93464e69ac54589ab1528e42eacca646f2446533c25
_domain: banking.sop_guides
_status: latest
_source_commit: 2a97cec269a536ec12918e6c2220cabffce55c95
_source_path: sop_procedures/sop_account_opening_v3.md
_source_type: md
_ingested_at: '2026-09-05T23:47:17.776972+00:00'
title: sop_account_opening_v3
declared_version: '3.0'
created_on: '2026-09-05T23:47:17.776972+00:00'
---

# FirstUK Bank — Account Opening Procedure

## Metadata

| Field | Value |
|---|---|
| Document ID | ACCT-OPEN-SOP-001 |
| Version | 3.0 |
| Effective Date | 2026-03-01 |
| Review Date | 2027-03-01 |
| Supersedes | Version 2.1, [[sop_account_opening]] |
| Superseded By | None |
| Owner | Head of Retail Banking |
| Status | Active |
| Audience | Branch, Digital Onboarding, Operations, Compliance |
| Related Documents | [[policy_customer_identification_v2]], [[policy_aml]], [[sop_kyc_verification]], [[enhanced_kyc_implementation_register]] |

---

## Purpose

Implement enhanced-KYC requirements from 2026-03-01. This procedure supersedes
Version 2.1 in full from that date.

## Step 1: Risk Classify Before Activation

1. Identify whether the applicant is an individual or entity.
2. Apply the standard customer-risk assessment.
3. Mark a high-risk customer as `Pending Enhanced Due Diligence`.
4. Do not issue credentials or accept an initial deposit until approval gates pass.

## Step 2: Enhanced Due Diligence Gate

| Check | Evidence to Record | Owner |
|---|---|---|
| Beneficial owners | Identity and ownership/control evidence for every owner above 25% | Onboarding Analyst |
| Source of funds | Credible evidence for an initial deposit above £10,000 | Onboarding Analyst |
| Enhanced screening | OFAC, EU, UN, HMT, PEP, sanctions, and adverse-media results | Financial Crime Analyst |
| Approval | Compliance approval and any documented exception decision | Head of Compliance / CRO |

## Step 3: Approval and Activation

- No material concern: Head of Compliance approves activation.
- Policy exception requested: document the rationale and obtain CRO approval.
- Positive match, suspicious funds, or unclear ownership: refer to Financial
  Crime; do not activate or tip off the customer.

After approval, set the next review three months from activation and store the
review date in the KYC record.

## Quality Control and Exceptions

A second reviewer checks high-risk files. A missing document is not a minor
exception: resolve it or escalate under `[[sop_exception_handling]]`. Apply
`[[policy_customer_identification_v2]]` if policy and training material differ.
