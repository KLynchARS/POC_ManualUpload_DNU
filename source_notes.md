# Source and conversion notes

- Workbook: `ARS_EDW_Metadata_Template_branchsampledata.xlsx`
- Workbook SHA-256: `801e456c1ae0f4dfa21cbc6a1003dcbeb95f00eb5c28855fd63adc13c6953863`
- Content used: `Table_Metadata` and `Column_Metadata` only.
- Records included: Table_Metadata row 4; Column_Metadata rows 4–23.
- Row 3 supplies headers; rows 1–2 are template guidance rather than entity records. Guidance was used only to interpret properties within these two sheets.
- Legend, Property_Dictionary and Allowed_Values were not read for content or included.
- Empty template rows and formula-only rows with no physical column name were excluded.
- Formula-backed IDs and table summary values were read from workbook cached values and independently checked against the populated metadata records; Excel formulas are not included in the CSVs.
- Original property names, populated values and blank values are preserved in the two metadata CSVs. Nonbreaking spaces in supplied text are preserved.
- Table summary checks: 20 populated columns; 20 CDE flags Y; 20 PII flags N, consistent with supplied CDE Count 20 and Contains PII N. This verifies metadata consistency only, not actual records.
- Table ID includes edw_prd; source guidance describes that database prefix as an assumption. Column IDs use schema.table.column and are not changed to include the database prefix.
- Five missing business definitions have proposals in the glossary; original blank definitions remain blank in column_metadata.csv.
- All imported content retains Draft status. Package creation does not establish steward review or approval.
- No source-system lineage, mappings, hierarchy order, or database constraints have been invented.

## Field mapping

| Source | Destination | Treatment |
| --- | --- | --- |
| Table_Metadata row 4 | data-models/organization/dim_branch/table_metadata.csv | All 13 properties preserved |
| Column_Metadata rows 4–23 | data-models/organization/dim_branch/column_metadata.csv | All 27 properties preserved for all 20 columns |
| Attribute Name / Attribute Definition | glossary/organization/org_unit_terms.csv | 20 terms; 15 supplied definitions and 5 labeled proposals |
| Null Option / Required Field / Length | business-rules/organization/org_unit_rules.csv | Documented constraints with provenance; proposals separately labeled |
| Blank or ambiguous metadata | decisions/organization/org_unit_review_items.csv | Review actions without silently changing the source |
