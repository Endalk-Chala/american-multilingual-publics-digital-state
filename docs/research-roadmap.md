# Research Infrastructure Roadmap

## Stage 0 — Infrastructure
- Finalize repository layout.
- Define stable IDs and provenance fields.
- Create schemas and controlled vocabularies.
- Decide licensing boundaries for government text, annotations, and model outputs.

## Stage 1 — American public-benefit pilot
- Select benefit domains.
- Collect official English and multilingual public-facing materials.
- Record state, agency, program, channel, document type, date, and source URL.
- Document machine-translation and human-review practices where available.

## Stage 2 — Multilingual evaluation
- Prioritize Amharic and Afaan Oromo.
- Build validated evaluation sets.
- Use independent reviewers and adjudication.
- Preserve semantic, pragmatic, institutional, and actionability dimensions.

## Stage 3 — Cross-national extension
- Add selected countries with contrasting language regimes, welfare systems, and digital-government models.
- Harmonize metadata without erasing jurisdiction-specific distinctions.

## Stage 4 — Model development
Possible tasks:
1. public-service translation,
2. institutional terminology adaptation,
3. translation-quality estimation,
4. risk/error detection,
5. bilingual retrieval or question answering.

Do not choose the final model task until the dataset is large enough and licensing is clear.

## Stage 5 — Hugging Face release
- Dataset Card
- Model Card if/when a model is trained
- reproducible evaluation
- limitations and ethics
- versioned release data
