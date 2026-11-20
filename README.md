# ARS Org Unit business context

A GitHub-ready documentation package for `dw_t.dim_branch` in the Organization domain, based solely on the uploaded workbook's Table_Metadata and Column_Metadata sheets.

**Review status: Draft.** Includes one entity, 20 column records, and 20 glossary terms. Fifteen business definitions are supplied; five are proposed for steward review.

## Start here

| Folder | Contents |
| --- | --- |
| [business-context/organization](business-context/organization/org_unit.md) | Entity purpose, stewardship, scope and source provenance |
| [glossary/organization](glossary/organization/org_unit_terms.csv) | Business terms, definitions, review status and source references |
| [data-models/organization/dim_branch](data-models/organization/dim_branch/entity.md) | Entity documentation and full table/column metadata CSVs |
| [business-rules/organization](business-rules/organization/README.md) | Documented constraints and proposed rule reviews |
| [decisions/organization](decisions/organization/decision_log.md) | Decision template and open review items |
| [metrics/organization](metrics/organization/example_metric.md) | Metric definitions (placeholder example) |
| [processes/organization](processes/organization/example_process.md) | Business process documentation (placeholder example) |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to propose and review changes |

## Conventions

- Markdown files explain context; CSV files hold structured metadata. CSV encoding is UTF-8 with a header row.
- Empty source values remain empty in metadata CSVs. A blank is not N, None, an approved default or a confirmed absence.
- Source Attribute Definition and Column Description remain separate. Proposed glossary definitions do not replace blank source definitions.
- Source-documented means present in the draft workbook; it does not mean approved, deployed or tested.
- Stable references use the supplied Table ID and Column ID. Confirm the database prefix before extending IDs across databases.
- Do not infer joins from column names, impose unique constraints from descriptive wording, or treat CDE flags as non-null requirements.

## Manual handoff

1. Extract the ZIP, preserving folders; place this folder's contents at the repository root or inside an agreed documentation folder.
2. Review business-context/organization/org_unit.md and decisions/organization/org_unit_review_items.csv with the appropriate stewards and technical owners.
3. Include the files in a proposed repository change for review. Record approved decisions and update the affected metadata, glossary and rule files together.
4. Keep Review Status as Draft until actual review occurs; record the real reviewer and review date when available.

## Maintenance proposal

Confirm the authoritative source before routine updates. If the workbook, Purview or Profisee remains authoritative, maintain these files as a reviewed copy and update their provenance on each refresh. If GitHub is selected as authoritative for some content, document that decision explicitly.

The exported metadata CSVs preserve the supplied records. During future updates, edit those records deliberately and keep derived summaries consistent. Keep original column identifiers stable. Use the same folder pattern (metrics and processes are placeholders in this demo) and a separate entity subfolder for future tables.

See [source notes](business-context/organization/source_notes.md) for included ranges, conversion choices and metadata checks. No workbook template helper sheets or original workbook are included in this package.
