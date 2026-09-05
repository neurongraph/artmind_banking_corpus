---
_artmind_id: 01a072b4-1a8f-7214-b2b0-396be8e88db2
_version: 1
_content_sha256: 325adf2e6157ebbd2de37d757d4e260ef062c30e80e6891ab3be6d0fa884576e
_domain: banking.cases
_status: latest
_source_commit: 3449fb174ae621bc5cf3e5f4aea92c9648589051
_source_path: cases/case_2026_041_overview.md
_source_type: md
_ingested_at: '2026-09-05T17:53:21.039717+00:00'
title: case_2026_041_overview
declared_version: '1.0'
created_on: '2026-09-05T17:53:21.039717+00:00'
---

# CASE-2026-041 — Customer Data Exposure

| Field | Value |
|---|---|
| Case ID | CASE-2026-041 |
| Document ID | CASE-041-OVERVIEW |
| Version | 1.0 |
| Opened | 2026-07-02 |
| Owner | Incident Commander |
| Status | Open — forensic reconciliation pending |
| Supersedes | None |
| Superseded By | None |
| Related Documents | [[case_2026_041_incident_timeline]], [[case_2026_041_complaint_record]], [[case_2026_041_retention_decision]], [[incident_response_plan]], [[policy_privacy]], [[policy_retention]] |

A customer-document export configuration defect exposed statement PDFs outside the intended account scope. The service was disabled and logs preserved.

Initial Security assessment: **120 potentially affected customers**. Operations reconciliation: **118 confirmed affected customers**, after removing two failed-download events. This is unresolved: do not replace one count with the other. Attribute both figures and describe reconciliation as pending.

Workstream owners: CTO containment; Customer Service complaints; DPO privacy and holds; Financial Crime AML records; CRO governance reporting.
