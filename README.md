# American Multilingual Publics and the Digital State

**Public Benefits, Language Access, and AI-Mediated Communication**

This repository is the research-data infrastructure for a comparative communication project examining how public institutions communicate public benefits to multilingual publics, with particular attention to language access, digital systems, AI/machine translation, human oversight, information integrity, and communicative administrative burden.

## Geographic scope

The first empirical phase focuses on the **United States**, treating the American digital state as a comparative institutional environment for studying multilingual public-benefit communication, language access, AI translation, and human oversight. The conceptual framework is designed so that later phases can extend cross-nationally.

## Current status

Early infrastructure stage. Conceptual framework preserved; data collection has not yet begun at scale.

## Core research question

How do public institutions communicate benefits to multilingual publics, and how do language-access regimes, digital systems, AI translation, and human oversight distribute communicative access and burden across different institutional contexts?

## Repository architecture

- `docs/` — conceptual framework, methods, protocols, and research notes
- `data/raw/` — untouched source records and source metadata
- `data/processed/` — normalized and transformed records
- `data/annotations/` — human coding and evaluation layers
- `data/release/` — validated release-ready datasets
- `schemas/` — machine-readable data schemas and codebooks
- `scripts/` — collection, validation, transformation, and analysis scripts
- `models/` — model-development notes, experiments, and evaluation plans
- `huggingface/` — files prepared specifically for Hugging Face datasets/models

## Initial language focus

The first model-development track will focus on **Amharic** and **Afaan Oromo**, especially high-consequence public-service communication.

## Design principles

1. Preserve provenance.
2. Separate source data from derived data.
3. Never treat machine-translated or assistant-aligned text as gold without human validation.
4. Keep legal/policy status date-stamped and jurisdiction-specific.
5. Distinguish official institutional reference translations from independently validated translations.
6. Keep development, annotation, adjudication, and public-release layers separate.
7. Document all AI and machine-translation conditions precisely.
8. Require explicit human-oversight metadata for high-consequence translations.

## Related project

The existing project **When Translation Is Not Access: AI Translation Infrastructure and Communicative Inequality in Under-Resourced Languages** remains a related computational study and methodological testbed.
