# dw_t.dim_branch

Dimension table providing descriptive attributes for reporting and analytics related to branches.

Table ID: `edw_prd.dw_t.dim_branch`. Domain: Organization. Type: Dimension. Review status: Draft.

## Field inventory

| Column | Attribute | Data type | Null option | Surrogate key | Primary key | Foreign key | Required |
| --- | --- | --- | --- | --- | --- | --- | --- |
| branch_sk | Branch SK | int | Not Null | Y | N | N | Y |
| branch_id | Branch ID | int | Null | N | N | N | N |
| branch_number | Branch Number | varchar(4) | Null | N | N | N | N |
| branch_name | Branch Name | varchar(50) | Null | N | N | N | N |
| branch_short_name | Branch Short Name | varchar(20) | Null | N | N | N | N |
| region_number | Region Number | varchar(4) | Null | N | N | N | N |
| region_name | Region Name | varchar(50) | Null | N | N | N | N |
| region_short_name | Region Short Name | varchar(20) | Null | N | N | N | N |
| division_number | Division Number | varchar(4) | Null | N | N | N | N |
| division_name | Division Name | varchar(50) | Null | N | N | N | N |
| division_short_name | Division Short Name | varchar(20) | Null | N | N | N | N |
| zone_number | Zone Number | varchar(4) | Null | N | N | N | N |
| zone_name | Zone Name | varchar(50) | Null | N | N | N | N |
| zone_short_name | Zone Short Name | varchar(50) | Null | N | N | N | N |
| company_number | Company Number | varchar(4) | Null | N | N | N | N |
| company_name | Company Name | varchar(50) | Null | N | N | N | N |
| service_group_id | Group ID | int | Null | N | N | N | N |
| service_group_name | Group Name | varchar(200) | Null | N | N | N | N |
| ishdx_flg | HDX Flag | char(1) | Null | N | N | N | N |
| last_processed_dttm | Last Processed Date Time Stamp | datetime | Not Null | N | N | N | Y |

Types and lengths are metadata supplied by the workbook, not verified database DDL. See [column_metadata.csv](column_metadata.csv) for all 27 original properties, including definitions, classifications and rules.

## Keys, grain and relationships

`branch_sk` is marked as a surrogate key and described as unique per row, but Is Primary Key is N for every column. No primary key is declared in the supplied metadata; confirm database constraints and intended grain before defining joins or uniqueness tests.

Every Is Foreign Key value is N; parent table and parent column fields are blank. No database relationships are asserted. Region, division, zone, company and service group columns describe context within the branch table; they do not establish separate entities or foreign keys.

No history/effective-date strategy, incoming references, or join cardinalities are supplied. An ER diagram would require additional evidence.
