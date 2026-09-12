# Collection Template v1.0

Status: **finalized for Pilot Batch 01**

This specification defines the working collection template for the first empirical phase of **American Multilingual Publics and the Digital State**.

The canonical field definitions remain in `docs/METADATA_CODEBOOK.md`. The working CSV header is in `data/templates/public_benefit_collection_template.csv`.

## Workbook structure

A companion Excel workbook has four sheets:

1. **Collection** — 73 structured fields with 100 ready-to-use rows.
2. **Controlled Vocab** — standardized categorical values used by dropdowns.
3. **Field Guide** — field purpose, collection stage, coding note, and allowed format.
4. **QA Checklist** — record-level quality checks before a batch is accepted.

## Defaults

- `country` = `United States`
- `record_version` = `1.0`
- dates use `YYYY-MM-DD`
- new records should normally begin as `release_status = internal_only`

## Required-at-collection fields

At minimum, collect:

- `item_id`
- `record_version`
- `collection_batch`
- `country`
- `state_or_territory`
- `jurisdiction_level`
- `agency_name`
- `benefit_domain`
- `program_name`
- `communication_type`
- `communication_channel`
- `document_title`
- `date_accessed`
- `source_url`
- `source_language`
- `translation_available`
- `translation_method`
- `human_review_status`
- `risk_level`
- `provenance_status`
- `release_status`

## Multi-label fields

Use semicolon-separated values for:

- `risk_basis`
- `error_tags`
- `human_review_trigger`

## Translation-quality fields

The following are intentionally left for validated review rather than initial collection:

- `semantic_fidelity`
- `pragmatic_fidelity`
- `institutional_fidelity`
- `actionability`
- `error_tags`
- `reviewer_id`
- `adjudication_status`

Scores use the established 1–5 scale.

## Communicative-burden fields

These are also later-stage coding fields and use a 1–5 scale:

- `finding_burden`
- `navigation_burden`
- `interpretation_burden`
- `verification_burden`
- `action_burden`

## Coding safeguards

- Do not infer undocumented translation workflows.
- `none_documented` is not equivalent to proof that no human review occurs.
- Keep legal vital-document designation separate from researcher-coded `likely_vital` status.
- Distinguish live agency AI/MT systems from browser tools and research-model conditions.
- Do not treat official translations as perfect gold standards.
- Preserve source text before normalization.
- Document uncertainty instead of resolving it by assumption.
- Keep Amharic and Afaan Oromo high-consequence evaluation human-reviewed and adjudicated.

## Pilot readiness

The template is frozen at **v1.0** for the first pilot batch. Changes to field names, controlled vocabularies, or coding rules after collection begins should be versioned rather than silently overwritten.
