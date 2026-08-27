# Researcher Profile

**Status:** Version 0.1

This file records the researcher's default working preferences. Individual projects may override any preference when appropriate.

## Research Context

Primary field:

* Economics
* Public finance
* Primarily data-oriented and empirical research

Primary statistical environment:

* R

Several research and non-research projects may be active simultaneously.

## AI Collaboration Style

Preferred relationship with AI:

**Collaborative delegation.**

AI should handle a large share of technical execution while the researcher maintains oversight and approval.

Technical work should normally be delegated aggressively, including:

* code generation;
* routine calculations;
* data processing;
* tables;
* figures;
* document preparation;
* formatting;
* documentation;
* consistency checks;
* replication tasks.

Some code execution may be performed manually by the researcher on the local computer when appropriate.

## Scientific Collaboration

AI should actively participate in:

* research-question generation;
* brainstorming;
* research strategy;
* experimental or empirical design;
* identification-strategy development;
* robustness design;
* interpretation;
* evaluation of results;
* alternative explanations;
* criticism of the researcher's reasoning.

The preferred relationship is reciprocal: the researcher and AI should challenge and correct each other.

AI should not merely agree with the researcher.

## Scientific Decision Authority

High technical autonomy is preferred.

Explicit researcher review is expected for consequential scientific decisions involving:

* research questions;
* estimands;
* identification assumptions;
* important sample-definition changes;
* substantive variable interpretation;
* inference;
* interpretation of central findings;
* final research conclusions.

## Literature

The literature workflow is deliberately human-centered.

Preferred workflow:

1. discover candidate literature using conventional databases and AI-assisted discovery tools;
2. screen candidate papers;
3. read important papers personally;
4. annotate and take notes in Zotero;
5. treat researcher-reviewed notes as the trusted literature corpus;
6. use AI to synthesize, compare, organize, and critique that trusted corpus.

AI-generated summaries of unread papers should not ordinarily be treated as trusted evidence.

## Organization

The system should provide substantial organizational assistance.

AI should help maintain:

* orderly project folders;
* current project status;
* decision records;
* analysis plans;
* unresolved-question lists;
* session handoffs;
* verification reports;
* dependencies between analysis and manuscript outputs.

Important project knowledge should be stored in files rather than relying on the researcher to remember where it appeared in previous AI conversations.

## Verification

AI should be used extensively for verification.

Preferred hierarchy:

* deterministic computational checks where possible;
* AI technical review;
* independent AI review for important outputs;
* researcher review for scientifically consequential conclusions.

Human attention should be concentrated on high-value scientific checks rather than manually rechecking every mechanical operation.

## Languages

Research outputs may be produced in:

* English;
* Turkish.

The manuscript language should be configured separately for each project.

Technical project documentation may normally remain in English unless a project requires otherwise.

Terminology should remain consistent within each manuscript.

## Manuscript Formats

Potential formats include:

* Word;
* LaTeX;
* Quarto or related reproducible formats.

Turkish journals may require Microsoft Word and may provide:

* journal-specific formatting instructions;
* manuscript templates;
* reference requirements;
* bilingual abstracts or metadata.

These requirements should be handled at the project level.

## AI Tooling Experience

The researcher is developing familiarity with agentic coding and research workflows.

Instructions should therefore:

* be clear;
* use simple terminology initially;
* explain important new concepts;
* avoid unnecessary infrastructure;
* introduce complexity incrementally.

## Current Design Preference

The preferred architecture is:

**Researcher → Project Steward → technical execution / criticism / verification**

with additional independent AI systems used when their independence is valuable.

The repository, rather than any individual AI conversation, should serve as the durable center of each project.
