# Data Layer

This project separates data by lifecycle stage.

## raw/
Untouched source text and metadata. Never overwrite.

## processed/
Normalized records derived from raw sources.

## annotations/
Human ratings, coding, adjudication, and quality-assurance records.

## release/
Only validated records cleared for public or controlled release.

Every record should carry:
- stable item ID
- jurisdiction
- agency
- program/benefit domain
- source date
- source URL
- source language
- target language
- document/channel type
- provenance status
- translation method
- human review status
- risk level
- licensing/rights note
