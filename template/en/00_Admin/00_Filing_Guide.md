# Project Document Filing Guide

| Version | Created/Revised | Author | Change Summary |
|---------|-----------------|--------|----------------|
| 0.1     | 2025-05-01      | PMO    | Initial Draft  |

---

## 1. Purpose

This guide aims to manage project documents systematically and consistently, ensuring **searchability, authenticity, completeness, and preservation**.

## 2. Scope

* All *management documents*, *deliverables*, and *work information* generated in this project
* Official repositories such as shared repositories and designated storage

## 3. Folder Structure Overview

~~~text
<ProjectRoot>/
├─ 00_Admin            … This guide, contact list, policies
├─ 01_Initiating       … Initiating Process Group
├─ 02_Planning         … Planning Process Group (sub-hierarchy by knowledge area)
├─ 03_Executing        … Executing Process Group
├─ 04_Monitoring_Controlling
├─ 05_Closing
├─ 90_Deliverables     … WBS-mirrored deliverables repository
└─ 99_Archive          … Phase completion snapshots
~~~

**Important:**

* Folder names must have hierarchy numbers at the beginning to maintain fixed order.
* PMO approval is required for creating additional folders.

## 4. Folder Roles and Custodianship

| Level | Main Content | Custodian | View Access |
|-------|-------------|-----------|-------------|
| 00_Admin | Policies, procedures, contact list | PMO | All members |
| 01_Initiating | Project Charter, Stakeholder Register | PM, PMO | All members |
| 02_Planning | PMP, various plans, baselines | PMO | All members |
| 03_Executing | Work deliverables, reports, issue management | Team Leads | Relevant parties |
| 04_Monitoring_Controlling | Change management, monitoring metrics | PM, PMO | Relevant parties |
| 05_Closing | Final report, handover records | PM | All members |
| 90_Deliverables | Approved deliverables set | Team Leads | Including customer |
| 99_Archive | Version-controlled snapshots | PMO | PMO only |

## 5. File Naming Convention

~~~text
<ProjectCode>-<DeliverableName>-<YYMMDD>.<extension>
Example: XY123-Project_Charter-250501.docx
~~~

* Code is 3–6 alphanumeric characters as specified in *Project Charter*
* *Revision date* (Japan time) in 6 digits
* Suffix (e.g., `250501a`) is added only when multiple versions occur on the same day

## 6. Version Control

| Status | Storage Location | Version Numbering | Review Required |
|--------|-----------------|-------------------|-----------------|
| Draft | Personal repository / Draft folder | None | Optional |
| Review | Process folder root | `YYMMDD-rcN` | Required |
| Approved | *Approved* subfolder | `YYMMDD` | Approval record required |
| Obsolete | 99_Archive | Original version number | Not allowed |

* **Review/Approval** uses {{placeholder}}, with links recorded in metadata.
* Old versions remain in *Approved* with `_Old` suffix and "read-only" setting.

## 7. Document Registration/Update Flow

~~~mermaid
graph TD
A[Author Draft] -->|Review Request| B[Reviewer]
B -->|Comments| A
B -->|Approve| C[PM/PMO]
C -->|Confirm YYMMDD| D[Formal Storage]
D --> E{Change Needed?}
E -->|Yes| A
E -->|No| F[Release/Notify]
~~~

**Checklist** (excerpt)

1. File naming convention followed
2. Correct PMBOK process folder used
3. Metadata "Document Type", "Baseline", "Confidentiality" set

## 8. Access Rights/Review Rights

* Default: **View: All project members**, **Edit: Deliverable owners**
* `99_Archive` writable by PMO only
* External vendors access only NDA-signed folders (`_External`)

## 9. Storage/Backup/Archive

| Category | Retention Period | Storage Location | Notes |
|----------|-----------------|------------------|-------|
| Approved Deliverables | {{placeholder}} years | {{placeholder}} | Regulatory compliance |
| Drafts | {{placeholder}} years | {{placeholder}} | Deletable after versioning |
| WPD/WPI/WPR Logs | {{placeholder}} years | {{placeholder}} | — |

Backup: Server-side {{placeholder}}.
Phase completion: PMO ZIPs to `99_Archive`.

## 10. Change Management/Revision History

* This guide revisions follow **Configuration Management Plan (CMP)**.
* Change requests registered in `04_Monitoring_Controlling/Integration/4.6_Integrated_Change_Management/Approved_Changes`.
* Version numbering rules follow Section 5.

## 11. Audit/Compliance

* {{placeholder}} based on {{placeholder}} internal audits
* Non-conformities require **Corrective Action Report (CAR)** in `00_Admin`

## 12. References

* {{placeholder}}

---

*Contact for this guide: **{{placeholder}} ({{placeholder}})***
