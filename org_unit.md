# Org Unit business context

Status: Draft, matching the source workbook. Generated definitions and review actions are proposals.

## Source-provided entity metadata

| Property | Value |
| --- | --- |
| Table ID | edw_prd.dw_t.dim_branch |
| Table Name | dw_t.dim_branch |
| Table Type | Dimension |
| Business Domain | Organization |
| Lifecycle Status | Active |
| Review Status | Draft |
| Table Description | Dimension table providing descriptive attributes for reporting and analytics related to branches. |
| Data Steward | Finance Department |
| Contains PII (derived) | N |
| CDE Count (derived) | 20 |
| Source System | Not provided |
| Refresh Frequency | Not provided |
| Last Reviewed Date | Not provided |

## Scope supported by the columns

The branch dimension includes branch identifiers and names, region/division/zone/company attributes, service group attributes, an HDX reporting indicator, and a processing timestamp. This is a summary of the supplied column metadata; no other systems or business processes were used to extend the scope.

## Interpretation limits

- The exact row grain and history strategy are not documented; do not assume one current row per branch.
- The organization levels appear as attributes on this table; their parent-child order and cardinality are not documented.
- Finance Department is listed as Data Steward; a separate accountable business owner is not supplied.
- All 20 columns are marked Is CDE = Y, Is PII = N, and Data Classification = Internal in the draft source; these are source assertions awaiting review.
- Source System, Refresh Frequency, and Last Reviewed Date are blank. No last-reviewed date has been invented.

Review the [open items](../../decisions/organization/org_unit_review_items.csv) before approval.
