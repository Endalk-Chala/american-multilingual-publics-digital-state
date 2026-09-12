# Pilot Domains

## Purpose

The first empirical phase should be narrow enough to support rigorous data collection, but broad enough to test the project's central claims about multilingual public-benefit communication, AI translation, human oversight, information integrity, and communicative administrative burden.

## Recommended pilot domains

### 1. Medicaid / public health coverage
Why include it:
- high-consequence eligibility and enrollment information;
- recurring multilingual communication needs;
- frequent deadlines, renewals, coverage changes, appeals, and documentation requirements;
- strong fit for testing whether translations preserve institutional meaning and actionability.

Priority communication types:
- eligibility explanations;
- enrollment and renewal instructions;
- notices about documentation;
- appeal and hearing information;
- coverage-change notices;
- fraud/scam warnings;
- web FAQs and automated help tools.

### 2. SNAP / food assistance
Why include it:
- direct relevance to benefit eligibility, documentation, reporting requirements, and administrative burden;
- substantial state-level implementation variation within a federal framework;
- recurring public discourse about fraud, deservingness, immigration, and benefit use.

Priority communication types:
- eligibility explanations;
- application instructions;
- interview requirements;
- reporting and recertification rules;
- notices of adverse action;
- fraud warnings;
- public-facing outreach materials.

### 3. Unemployment and workforce services
Why include it:
- combines benefits with employment-service communication;
- substantial digital-portal dependence;
- frequent identity verification, deadlines, appeals, and fraud-prevention communication;
- useful for studying how technological systems mediate access.

Priority communication types:
- eligibility information;
- application instructions;
- identity-verification notices;
- work-search requirements;
- denial and appeal information;
- fraud/scam warnings;
- workforce-service navigation.

## Secondary expansion domains

These should be added after the pilot infrastructure is stable:
- childcare assistance;
- housing assistance;
- cash assistance/TANF;
- disability-related public benefits;
- state tax credits and rebates;
- immigration-adjacent public-charge and benefit-eligibility guidance.

## Initial comparative design

The first pilot should begin with a small but deliberately contrasting set of states rather than all 50 states at once.

Recommended first-stage state logic:
- one state with relatively developed language-access infrastructure;
- one state with high linguistic diversity but more fragmented implementation;
- one state with strong digital-government infrastructure;
- one state where public-benefit and immigration rhetoric is politically salient;
- one state with a significant Amharic or Afaan Oromo population where feasible.

The state-selection criteria should be documented before collection begins. The project should avoid selecting states only because their materials are easy to find.

## Unit of analysis

The primary unit should be a **public-benefit communication item**, not simply a policy or state.

An item may be:
- a web page;
- a downloadable notice;
- an application instruction;
- an FAQ entry;
- an appeal-rights statement;
- a fraud warning;
- a translated form;
- a chatbot or automated-help response;
- a machine-translated page state;
- a social-media post from an official agency account.

Each item must be linked to the relevant jurisdiction, agency, program, channel, language, source date, provenance status, and translation/human-review conditions.

## Initial language focus

The infrastructure should support many languages from the start, but the first deep translation-quality track should prioritize:
- Amharic;
- Afaan Oromo.

English serves as the principal source-language reference in the first U.S. phase unless the original institutional source is produced in another language.

## Pilot success criteria

The pilot is successful if it can demonstrate that the infrastructure can reliably:
1. preserve provenance;
2. compare English and multilingual versions;
3. record translation method and human-review status;
4. identify high-consequence communication features;
5. support human annotation of semantic, pragmatic, institutional, and actionability fidelity;
6. document AI/machine-translation use without confusing research-model conditions with live production systems;
7. generate a release-ready subset suitable for later Hugging Face publication.
