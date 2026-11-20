# Org Unit rules and mappings

[org_unit_rules.csv](org_unit_rules.csv) separates source-documented constraints from proposed review actions. None has been executed against database records or verified against database constraints. Proposed items are not approved requirements.

Business Rules, Data Rule Type, Validation Rule, Default Value and Comments are blank for all 20 source columns. No pass-rate thresholds, detailed business validation expressions, or defaults have been inferred.

The HDX flag has type char and length 1, but no allowed values or meanings were provided. No mapping is invented. The values 9700 and American Residential Services, LLC appear in company definitions; they have not been converted into fixed-value validation rules.

Descriptions referring to unique region/company names or identifiers do not imply those values are unique across branch rows. Any future uniqueness check must use the confirmed entity grain.
