# AI-Mediated Research OS — Current Implementation

**Status:** Version 0.1

This document records the current implementation choices of the Research OS.

These are not universal requirements. Other researchers may use different AI systems, statistical software, storage providers, editors, or publication tools while following the same underlying principles.

---

## 1. Local Research Workspace

Primary workspace:

* **Visual Studio Code**

VS Code is used as the common interface for:

* project files;
* R scripts;
* Git version control;
* Claude Code;
* Codex;
* terminal access;
* manuscript and research-document editing.

The goal is to keep the main research repository visible and inspectable in one workspace.

---

## 2. Statistical Environment

Primary statistical software:

* **R**

R is used for:

* data preparation;
* statistical analysis;
* econometrics;
* simulations;
* tables;
* figures;
* reproducible numerical outputs.

The researcher may choose to execute important R scripts manually on the local computer even when an AI agent generated the code.

Package-environment reproducibility will later be handled using **renv** or an equivalent system.

### Cross-Platform R Execution

The Research OS may run on both macOS and Windows.

For shell-based or agent-based execution:

- macOS/Linux: prefer `Rscript`
- Windows: prefer `Rscript.exe`

On Windows PowerShell, the command `R` may be reserved as an alias for `Invoke-History`, so automated workflows should not assume that plain `R` invokes R.

Agents should detect the operating system when constructing shell commands and use the appropriate executable.

R analysis code itself should remain platform-independent whenever practical.

---

## 3. Primary AI Systems

### Claude

Primary project agent:

* **Claude Code**

Claude Code is the main repository-aware operational agent.

Its responsibilities may include:

* project organization;
* technical planning;
* R code generation;
* data-work implementation;
* document preparation;
* routine verification;
* maintaining project state;
* delegating appropriate work to specialized subagents.

Claude Code should operate from the project repository rather than from isolated copied code snippets whenever possible.

### ChatGPT

Primary external AI collaborator:

* **ChatGPT Plus**

ChatGPT is used mainly for:

* research ideation;
* conceptual discussion;
* external research;
* identification-strategy discussion;
* interpretation;
* alternative explanations;
* independent criticism;
* second opinions.

ChatGPT is not required to act as a message relay between the researcher and Claude Code.

### Codex

Secondary coding and verification agent:

* **Codex**

Codex may be used for:

* independent code review;
* alternative implementation;
* replication;
* technical verification;
* second-model checks.

Its independence from the primary Claude workflow is particularly valuable for important verification tasks.

---

## 4. Agent Architecture

The initial system uses four conceptual roles.

### Project Steward

Maintains awareness of the overall project.

Responsibilities include:

* reading current project state;
* maintaining plans;
* organizing work;
* deciding when specialist review is needed;
* recording important developments;
* escalating scientific decisions to the researcher.

The Project Steward is normally implemented through the main Claude Code session.

### Executor

Carries out technical work.

Examples:

* R programming;
* scraping;
* cleaning;
* database preparation;
* estimation;
* tables;
* figures;
* document generation.

The Executor may be the main Claude session or a specialized subagent.

### Critic

Challenges scientific or methodological reasoning.

Examples:

* identification strategy;
* estimand definition;
* inference;
* robustness;
* alternative explanations;
* interpretation.

The Critic should not merely confirm the reasoning of the Executor.

### Verifier

Checks whether important work is correct and reproducible.

Verification may involve:

* deterministic tests;
* independent implementation;
* fresh-context AI review;
* another AI model;
* human review.

Important verification agents should leave persistent written artifacts in the project repository.

---

## 5. Model Routing

The system should not use the most expensive model for every task.

Current Claude model-routing principle:

### Lower-cost model

Use for:

* simple file operations;
* routine formatting;
* mechanical checks;
* short summaries of completed work.

### Mid-tier model

Use as the default workhorse for:

* R coding;
* data processing;
* routine debugging;
* documentation;
* ordinary technical execution;
* project management.

### Frontier model

Use for high-ambiguity or high-stakes reasoning, including:

* research ideation;
* research design;
* identification strategy;
* difficult debugging;
* interpretation;
* methodological criticism;
* major manuscript reasoning;
* independent scientific review.

Current practical default:

* **Sonnet** for routine project work;
* **Opus** for difficult scientific or strategic reasoning;
* **Haiku or equivalent lower-cost model** for simple mechanical tasks when appropriate.

Model selection may be automated later.

---

## 6. Version Control

Version-control system:

* **Git**

Remote repository provider:

* **GitHub**

Each research project should normally have its own Git repository.

Git tracks:

* R code;
* research documents;
* manuscript sources;
* project configuration;
* decision records;
* verification reports;
* AI-generated review artifacts;
* reproducibility files.

Large research datasets should normally remain outside Git.

---

## 7. Multi-Computer Workflow

The system is designed for research across:

* macOS;
* Windows.

Each computer keeps its own local clone of the project repository.

Project files are synchronized through GitHub:

```text
Mac local repository
        ↕
      GitHub
        ↕
Windows local repository
```

Normal switching procedure:

1. finish work;
2. commit changes;
3. push to GitHub;
4. move to the other computer;
5. pull the latest changes;
6. continue working.

The same active Git repository should not normally be synchronized directly through Google Drive or another file-sync service.

### Researcher checkpoints

Agents should prompt the researcher explicitly at four points:

* **SAVE** — write modified files in the editor. Unsaved buffers are not committed.
* **COMMIT** — record a completed unit of work.
* **PUSH** — end of every session, without exception.
* **PULL** — start of every session, before editing.

A project must not be edited on two machines without synchronizing between them first.

`pull.ff only` is recommended so divergence fails loudly instead of merging silently.

---

## 8. Research Data Storage

Current cloud-storage provider:

* **Google Drive**

Main data root:

```text
ResearchData/
```

Active research-data folders should be available offline on each working computer.

Google Drive is responsible for synchronizing data files.

GitHub is responsible for synchronizing code and research-project files.

Conceptual architecture:

```text
                     Research Project

             GitHub                 Google Drive
               |                         |
       code / manuscript             research data
               |                         |
          Mac / Windows              Mac / Windows
```

---

## 9. Data Categories

Projects should distinguish at least:

### Raw data

Original source data.

Rules:

* immutable;
* never overwritten;
* stored outside Git;
* synchronized through approved storage when permitted.

### Intermediate data

Cleaned, merged, transformed, or harmonized datasets.

These may be synchronized through Google Drive when regeneration is costly.

### Temporary/generated data

Files that can be recreated easily.

These do not necessarily need cloud synchronization.

Individual projects may modify this structure.

---

## 10. Cross-Platform File Paths

Research code must not rely on hard-coded computer-specific paths.

Avoid paths such as:

```text
/Users/name/Google Drive/...
```

or:

```text
G:/My Drive/...
```

Instead, each computer should define a local environment variable such as:

```text
RESEARCH_DATA_ROOT
```

The Mac and Windows computers may point this variable to different local locations.

R projects should then access data using the common variable rather than machine-specific paths.

This configuration will be introduced when the first project template is implemented.

---

## 11. Literature System

Canonical literature manager:

* **Zotero**

Current discovery tools:

* conventional academic databases;
* **Consensus**;
* **ResearchRabbit**.

Other tools may be used temporarily when helpful.

The current policy is:

1. AI-assisted tools may discover papers;
2. the researcher screens and reads important papers;
3. Zotero holds the canonical library and reading notes;
4. researcher-reviewed notes form the trusted literature corpus;
5. AI may synthesize and critique this trusted corpus.

Elicit, Litmaps, Scite, or similar tools may be added when a project creates a concrete need.

---

## 12. Manuscript Production

Projects may use:

* Microsoft Word;
* LaTeX;
* Quarto;
* other reproducible document systems.

The required manuscript format is a project-level setting.

For journals supplying Word templates or detailed submission instructions, the project repository should store:

* the supplied template;
* journal instructions;
* submission requirements;
* a project-specific checklist.

The Research OS should adapt to the journal rather than assuming one publication format.

---

## 13. Languages

Current supported research languages:

* English;
* Turkish.

The manuscript language is configured separately for each project.

Technical project documents may remain in English by default.

Projects may maintain a terminology or translation glossary when consistent bilingual terminology matters.

---

## 14. Current Software Not Required

The following are not required in Version 0.1:

* Cursor;
* GitHub Copilot;
* complex MCP infrastructure;
* elaborate external agent frameworks;
* Docker-based execution.

Docker is already available and may later be introduced for isolation or reproducibility if it solves a concrete need.

---

## 15. Development Philosophy

The implementation should remain intentionally lightweight.

New software, agents, rules, and automation should be introduced only when:

1. a repeated problem is observed;
2. the proposed addition clearly solves that problem;
3. the added complexity is justified.

The Research OS itself should evolve through version control and documented revisions.
