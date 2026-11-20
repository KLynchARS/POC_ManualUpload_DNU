# Contributing

This repository holds reviewed business context (definitions, rules, metadata, decisions) for ARS data. **Demo draft:** the process below is illustrative.

## How to propose a change
1. Create a branch and edit the relevant files. If you change a definition or column property, update the matching glossary, metadata and rules files in the same pull request.
2. Open a pull request. Describe what changed and why, and link any related review item (for example, RV-001).
3. The data steward for the domain reviews the business content; a technical owner reviews the data-model content.
4. After approval, record the decision in `decisions/<domain>/` and update Review Status.

## Ground rules
- Do not paste PII, passwords, API keys or cardholder data into any file.
- Leave unknown values blank. Do not guess.
- Keep Review Status as Draft until a real review has happened.
- Do not edit generated or exported files by hand without noting it in the pull request.

## Reviewers
Reviewers and approvers are not yet assigned. See `decisions/organization/org_unit_review_items.csv`.
