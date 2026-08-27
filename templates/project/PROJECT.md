# Project Configuration

**Project title:** [PROJECT TITLE]
**Project ID:** [SHORT PROJECT ID]
**Status:** [IDEA / LITERATURE / DESIGN / DATA / ANALYSIS / WRITING / REVISION / COMPLETE]
**Last updated:** [YYYY-MM-DD]

This file contains project-specific context. It overrides researcher defaults when explicitly stated.

---

## 1. Project Summary

**Research type:**
[Empirical paper / theoretical paper / experiment / policy report / teaching / other]

**Field:**
[Field and subfield]

**Primary research question:**
[Current research question]

**Why this matters:**
[Short substantive motivation]

---

## 2. Current Research Stage

Current stage:

[Describe what is currently being worked on.]

Immediate objective:

[What should happen next?]

Current blockers:

* [BLOCKER]
* [BLOCKER]

---

## 3. Language and Output

**Working language:**
[English / Turkish / mixed]

**Manuscript language:**
[English / Turkish]

**Primary output:**
[Journal article / report / working paper / course material / other]

**Manuscript format:**
[Word / LaTeX / Quarto / undecided]

**Target journal or outlet:**
[NAME / undecided]

If journal-specific instructions or templates exist, store them in the manuscript area of the project.

---

## 4. Data

**Primary statistical software:**
R

**Data sensitivity:**
[Public / confidential / restricted / mixed]

**Data location:**
External project data directory under `RESEARCH_DATA_ROOT`.

Expected project data structure:

```text
raw/
intermediate/
external/
```

### Raw-data rule

Raw data are immutable.

AI agents and scripts may read raw data but must not overwrite or silently modify source files.

### Important datasets

* [DATASET — description]
* [DATASET — description]

### Known data issues

* [ISSUE]
* [ISSUE]

---

## 5. Institutional and Substantive Context

Important verified context:

* [FACT]
* [FACT]

Important context still requiring verification:

* [CLAIM / QUESTION]
* [CLAIM / QUESTION]

Project-specific terminology or definitions:

* [TERM → DEFINITION]

Longer institutional documentation should be stored separately in the research directory rather than making this file excessively long.

---

## 6. Literature

Canonical literature system:

**Zotero**

The project distinguishes between discovered literature and researcher-reviewed literature.

### Trusted literature

Only literature that has passed the project's human evidence gate should be treated as trusted evidence.

Trusted literature synthesis and reading-note exports should be stored separately from discovery material.

### Current core literature

* [ZOTERO KEY / PAPER / NOTE]
* [ZOTERO KEY / PAPER / NOTE]

### Literature questions

* [QUESTION]
* [QUESTION]

---

## 7. Research Design

### Current hypothesis or hypotheses

* [HYPOTHESIS]
* [HYPOTHESIS]

Mark whether each is:

* ex ante;
* exploratory;
* post-result.

### Current estimand

[Define clearly if applicable.]

### Candidate identification strategy

[Current strategy or strategies.]

### Main identifying assumptions

* [ASSUMPTION]
* [ASSUMPTION]

### Major threats

* [THREAT]
* [THREAT]

### Unresolved scientific decisions

* [DECISION NEEDED]
* [DECISION NEEDED]

Scientific decisions in this section require researcher review before implementation when they materially affect the research.

---

## 8. Analysis Plan

Current approved analysis:

1. [STEP]
2. [STEP]
3. [STEP]

Exploratory analyses should be clearly distinguished from approved/confirmatory analyses.

Detailed analysis plans may be stored separately under the project research or plans directory.

---

## 9. Current Findings

This section records only findings that have actually been produced by the computational workflow.

### Main results

* [RESULT + pointer to output]
* [RESULT + pointer to output]

### Unexpected results

* [RESULT]

### Interpretation status

[Not interpreted / exploratory interpretation / reviewed interpretation]

Do not enter numerical results from conversational memory. Refer to generated outputs or reproducible computational artifacts.

---

## 10. Important Decisions

Important decisions should also receive separate decision records when consequential.

Current high-level decisions:

* [DATE — DECISION — rationale]
* [DATE — DECISION — rationale]

---

## 11. Open Questions

Scientific:

* [QUESTION]

Technical:

* [QUESTION]

Institutional:

* [QUESTION]

Literature:

* [QUESTION]

---

## 12. Verification Status

Completed:

* [CHECK]

Pending:

* [CHECK]

High-stakes results should receive independent verification when practical.

---

## 13. AI Collaboration Settings

### Execution Mode

**Current execution mode:**
[RESEARCHER_EXECUTES_CONSEQUENTIAL]

Available modes:

* `AGENT_EXECUTES` — AI agents may execute analysis when technically appropriate.
* `RESEARCHER_EXECUTES_CONSEQUENTIAL` — agents may run diagnostics, tests, and routine code, but consequential/final empirical analyses are prepared for researcher execution.
* `RESEARCHER_EXECUTES_ALL` — agents prepare code but do not execute substantive analysis unless explicitly authorized.

The project may change execution mode during different research stages.

When uncertain whether an execution is consequential, ask the researcher.


Default project autonomy:

**High technical autonomy with scientific escalation.**

AI agents may normally perform reversible technical tasks without repeated approval when instructions are clear.

Escalate decisions that materially affect:

* the research question;
* estimand;
* identification;
* sample definition;
* substantive variable meaning;
* inference;
* interpretation;
* central conclusions.

Important critic and verifier agents should leave persistent written artifacts.

---

## 14. Project-Specific Overrides

List any explicit departures from Research OS defaults here.

Examples:

* different statistical software;
* different literature policy;
* restricted-data constraints;
* special journal requirements;
* project-specific verification rules;
* different AI-tool permissions.

Current overrides:

* None.

---

## 15. Next Actions

1. [NEXT ACTION]
2. [NEXT ACTION]
3. [NEXT ACTION]
