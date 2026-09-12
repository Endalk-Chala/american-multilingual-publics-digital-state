# Metadata Codebook

## Purpose

This codebook defines the minimum metadata needed to build a reproducible dataset of multilingual public-benefit communication in the United States. The goal is to support later comparison across jurisdictions, agencies, languages, communication channels, translation systems, and human-review practices while preserving provenance.

The primary unit of analysis is a **public-benefit communication item**.

---

## A. Record identity

### `item_id`
Stable unique identifier for the communication item.

Recommended pattern:
`US-STATE-AGENCY-PROGRAM-DATE-####`

Example:
`US-MN-DHS-MEDICAID-20260912-0001`

Do not encode language into the base item ID if multiple language versions belong to the same communication item. Language-specific versions should use a separate version field or suffix.

### `record_version`
Version number for the metadata record.

Example: `1.0`

### `collection_batch`
Identifier for the collection wave or pilot batch.

Example: `pilot01-medicaid-mn`

---

## B. Jurisdiction and institution

### `country`
Country in which the institution operates.

Initial value: `United States`

### `state_or_territory`
Full state or territory name.

### `jurisdiction_level`
Controlled vocabulary:
- federal
- state
- county
- city
- tribal
- regional
- quasi_public
- other

### `agency_name`
Official name of the agency responsible for the communication.

### `agency_acronym`
Official acronym if one exists.

### `agency_unit`
Division, bureau, office, program unit, or subagency when relevant.

---

## C. Benefit/program domain

### `benefit_domain`
Controlled vocabulary for the first phase:
- health_coverage
- food_assistance
- unemployment
- workforce_services
- childcare
- housing
- cash_assistance
- disability
- tax_credit
- immigration_adjacent_guidance
- other

### `program_name`
Official program name.

Examples:
- Medicaid
- SNAP
- Unemployment Insurance

### `program_acronym`
Official acronym if applicable.

---

## D. Communication object

### `communication_type`
Controlled vocabulary:
- webpage
- pdf
- form
- notice
- faq
- application_instruction
- renewal_instruction
- eligibility_explanation
- appeal_information
- fraud_warning
- press_release
- social_media_post
- chatbot_response
- portal_message
- sms
- email
- phone_script
- video
- other

### `communication_channel`
Controlled vocabulary:
- website
- portal
- downloadable_document
- social_media
- chatbot
- email
- sms
- telephone
- in_person
- mail
- video_platform
- other

### `document_title`
Exact title as displayed by the agency.

### `source_date`
Date published or last updated if available.

ISO format: `YYYY-MM-DD`

### `date_accessed`
Date the research team accessed the item.

### `source_url`
Direct URL to the source when available.

### `archived_url`
Archived URL if preserved through a web archive or repository.

### `source_status`
Controlled vocabulary:
- live
- archived
- removed
- superseded
- unknown

---

## E. Language and translation

### `source_language`
Language of the institutional source text.

Use standardized names consistently.

### `target_language`
Language of the translated version.

Initial deep-evaluation languages:
- Amharic
- Afaan Oromo

### `language_code`
Recommended ISO code where available.

Examples:
- English: `en`
- Amharic: `am`
- Afaan Oromo: `om`

### `translation_available`
Boolean: `true` / `false`

### `translation_method`
Controlled vocabulary:
- official_human
- vendor_human
- staff_translation
- machine_translation
- ai_assisted_translation
- browser_translation
- unknown
- not_applicable

### `translation_provider`
Name of translation provider or system if publicly identifiable.

Examples may include a contracted translation vendor or a named machine-translation service.

Do not infer the provider solely from appearance.

### `translation_disclosure`
Controlled vocabulary:
- explicit
- implicit
- none
- unknown

Records whether the agency discloses how translation was produced.

---

## F. Human review and quality assurance

### `human_review_status`
Controlled vocabulary:
- none_documented
- discretionary
- required_selected_content
- required_vital_content
- required_all_public_content
- structured_quality_assurance
- unknown
- not_applicable

### `reviewer_role`
Who performs the review if documented.

Examples:
- bilingual staff
- professional translator
- certified translator
- language-access coordinator
- vendor reviewer
- community reviewer

### `reviewer_qualification_documented`
Boolean or unknown.

Values:
- true
- false
- unknown

### `second_review_required`
Values:
- true
- false
- unknown

### `community_validation`
Values:
- none_documented
- informal
- structured
- unknown

### `correction_mechanism`
Controlled vocabulary:
- public_feedback_form
- internal_quality_process
- vendor_revision
- language_access_office
- none_documented
- unknown

### `translation_error_tracking`
Values:
- yes
- no
- unknown

---

## G. Risk and consequence

### `risk_level`
Researcher-coded communication risk:
- low
- medium
- high

### `risk_basis`
Controlled multi-value field. Possible values:
- eligibility
- benefit_amount
- deadline
- documentation_requirement
- identity_verification
- renewal
- termination
- denial
- appeal_right
- hearing_right
- legal_consequence
- immigration_consequence
- health_consequence
- fraud_or_scam
- payment_instruction
- other

### `vital_document_status`
Values:
- designated_vital
- likely_vital
- not_vital
- unknown

Do not assume a legal designation without documentation. `likely_vital` is a research classification, not a legal conclusion.

---

## H. Information-integrity dimensions

These fields can be completed during later coding rather than initial collection.

### `accuracy_status`
- accurate
- inaccurate
- mixed
- not_assessed

### `completeness_status`
- complete
- material_omission
- minor_omission
- not_assessed

### `currency_status`
- current
- outdated
- uncertain
- not_assessed

### `consistency_status`
- consistent_with_agency_sources
- conflicting
- uncertain
- not_assessed

### `source_authority`
- primary_official
- official_partner
- secondary
- unclear

### `actionability_status`
- fully_actionable
- partly_actionable
- not_actionable
- not_assessed

---

## I. Translation-quality evaluation

For validated comparison studies, score each translated version separately.

### `semantic_fidelity`
1–5 ordinal score.

### `pragmatic_fidelity`
1–5 ordinal score.

### `institutional_fidelity`
1–5 ordinal score.

### `actionability`
1–5 ordinal score.

### `error_tags`
Multi-label controlled vocabulary:
- omission
- addition
- negation_flip
- modality_shift
- eligibility_shift
- deadline_or_number_error
- institutional_term_error
- register_or_tone_shift
- ambiguity
- cultural_pragmatic_loss
- actionability_failure

### `reviewer_id`
Pseudonymous reviewer identifier.

### `adjudication_status`
- not_required
- pending
- adjudicated

---

## J. AI and machine-translation governance

### `ai_or_mt_used`
Values:
- yes
- no
- unknown

### `system_name`
Named AI or machine-translation system if documented.

### `system_role`
- primary_translation
- draft_translation
- fallback_translation
- webpage_widget
- user_optional
- reviewer_support
- unknown

### `human_in_the_loop`
- yes
- no
- partial
- unknown

### `human_review_trigger`
Controlled multi-value field:
- all_content
- vital_content
- high_risk_content
- complaints
- sample_audit
- discretionary
- none
- unknown

### `ai_use_disclosed_to_public`
- yes
- no
- unknown

### `automated_translation_warning`
Exact warning text or summary if the public is told that automated translation may contain errors.

---

## K. Communicative administrative burden

These variables operationalize the project's communication-centered burden concept.

### `finding_burden`
How difficult it is to locate the relevant multilingual information.

Scale:
1 = very easy
2 = easy
3 = moderate
4 = difficult
5 = very difficult

### `navigation_burden`
Difficulty moving through the site, portal, or document structure.

1–5 scale.

### `interpretation_burden`
Difficulty understanding the content even after translation.

1–5 scale.

### `verification_burden`
Effort required to determine whether the information or translation is trustworthy and current.

1–5 scale.

### `action_burden`
Effort required to determine the next required action.

1–5 scale.

### `burden_notes`
Short qualitative explanation supporting the scores.

---

## L. Provenance and rights

### `provenance_status`
Controlled vocabulary:
- official_source
- archived_official_source
- official_translation
- researcher_transcription
- researcher_alignment
- machine_generated
- secondary_source
- unknown

### `capture_method`
- manual_download
- manual_copy
- scraper
- api
- screenshot
- browser_capture
- other

### `raw_file_path`
Path to preserved raw source in the repository or archival system.

### `checksum`
Optional cryptographic hash of preserved file.

### `rights_note`
Source-specific copyright, public-domain, reuse, or licensing note.

### `release_status`
- internal_only
- review_pending
- release_candidate
- public_release
- restricted

---

## M. Research notes

### `collector_id`
Pseudonymous or team identifier for collector.

### `collection_notes`
Short factual notes about capture conditions.

### `uncertainty_flag`
- none
- low
- medium
- high

### `uncertainty_notes`
Explain ambiguity, unresolved provenance, unclear translation method, or other limitations.

---

# Coding principles

1. **Do not infer hidden translation workflows.** If human review is not documented, code it as unknown or none documented, not absent as fact.
2. **Separate institutional facts from researcher judgments.** For example, `designated_vital` requires evidence; `likely_vital` is an analytic classification.
3. **Preserve exact source wording before normalization.** Raw text should never be overwritten by cleaned text.
4. **Date-stamp legal and policy claims.** Language-access obligations and agency practice can change.
5. **Treat machine-translation conditions precisely.** A research model, browser translation tool, and production agency translation workflow are different conditions.
6. **Do not treat official translations as perfect gold standards.** They are institutional reference translations until independently validated.
7. **Keep Amharic and Afaan Oromo evaluation reviewer-based.** Human adjudication remains essential for high-consequence evaluation.
8. **Document missingness.** Absence of public documentation is itself analytically relevant, but it is not proof that a practice does not exist.

# Recommended minimum fields for every collected item

At minimum, every row should contain:
- `item_id`
- `country`
- `state_or_territory`
- `jurisdiction_level`
- `agency_name`
- `benefit_domain`
- `program_name`
- `communication_type`
- `communication_channel`
- `document_title`
- `source_date`
- `date_accessed`
- `source_url`
- `source_language`
- `target_language`
- `translation_method`
- `human_review_status`
- `risk_level`
- `provenance_status`
- `release_status`

This minimum set should be stable before large-scale collection begins.
