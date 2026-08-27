# AI-Mediated Research OS — Principles

**Status:** Version 0.1

This framework is designed for research in which humans and AI systems collaborate throughout the research process. It is intended to be adaptable across disciplines, software, languages, publication formats, and AI providers.

## 1. Human Scientific Responsibility

The researcher retains final responsibility for the research.

AI may participate in every stage, including:

* literature discovery;
* ideation;
* research design;
* data work;
* coding;
* analysis;
* interpretation;
* writing;
* verification;
* document preparation.

However, AI does not have equal decision authority in every stage.

Technical tasks may be delegated extensively. Scientific judgments with important consequences require explicit researcher review and approval.

## 2. Technical Autonomy, Scientific Escalation

AI agents should normally handle reversible technical work autonomously when the task and constraints are clear.

Examples include:

* generating code;
* restructuring files;
* preparing tables and figures;
* formatting documents;
* running routine checks;
* producing documentation.

Agents should escalate decisions that could materially affect:

* the research question;
* the estimand;
* identification;
* sample definition;
* variable meaning;
* statistical inference;
* interpretation;
* substantive conclusions.

When uncertain whether a decision is technical or scientific, the agent should make the uncertainty explicit.

## 3. Repository as Durable Research Memory

Important research state should live in project files rather than depend on conversation history.

The repository should preserve:

* current research questions;
* verified institutional context;
* hypotheses;
* analysis plans;
* important decisions;
* unresolved questions;
* session handoffs;
* verification reports;
* computational outputs;
* manuscript sources.

AI conversations are working environments. They are not the canonical memory of the project.

## 4. Separate Evidence From Exploration

The system must distinguish between:

* verified information;
* provisional information;
* researcher knowledge;
* AI-generated suggestions;
* hypotheses;
* rejected ideas.

Exploratory ideas must not silently become accepted project knowledge.

## 5. Human Evidence Gate for Literature

AI may assist with literature discovery, search strategy, organization, and synthesis.

However, AI-generated summaries or AI-discovered references should not automatically become trusted literature evidence.

Projects may define a human evidence gate under which literature becomes part of the trusted research corpus only after researcher review.

AI may then synthesize and analyze the trusted corpus.

## 6. Verification Is Part of Production

Generating an output and verifying an output are separate tasks.

Where possible, verification should use:

1. deterministic computational checks;
2. independent implementations;
3. independent AI review;
4. human scientific review.

The appropriate level of verification should increase with the scientific importance of the claim.

## 7. Independent Review

Important work should not be accepted merely because the agent that produced it also reports that it is correct.

High-stakes outputs should, when practical, be reviewed through:

* a fresh-context agent;
* a different model;
* an independent implementation;
* or a human reviewer.

Review agents should leave persistent artifacts documenting issues, evidence, severity, status, and resolution.

## 8. Computational Provenance

Important quantitative claims should be traceable to computational outputs.

Where practical:

* manuscript numbers should be generated from code;
* tables and figures should be generated reproducibly;
* changes in analysis should propagate to dependent outputs;
* stale numerical claims should be detectable.

Models should not reconstruct or invent numerical results from conversational memory.

## 9. Research Chronology Matters

The system should preserve distinctions such as:

* ex-ante hypothesis;
* exploratory hypothesis;
* post-result explanation;
* robustness analysis;
* confirmatory analysis.

AI makes post-hoc explanation inexpensive. The research record should therefore make chronology more visible rather than less visible.

## 10. Version Control by Default

Research projects and the Research OS itself should use version control.

Important changes should be inspectable and reversible.

Git is the default implementation, but the principle is broader than any particular software.

## 11. Adaptability

The framework should separate:

* universal principles;
* researcher preferences;
* reusable workflow modules;
* project-specific configuration;
* temporary task instructions.

A user should be able to change statistical software, AI provider, language, research field, or manuscript format without redesigning the entire system.

## 12. Tool Independence

Specific tools are implementation choices, not methodological principles.

For example, a project may use Claude Code, Codex, another coding agent, R, Stata, Python, Word, LaTeX, Quarto, Zotero, or alternative software.

The framework should remain usable when tools change.

## 13. Language and Publication Format Independence

Projects may operate in different languages and publication formats.

The research process should therefore support:

* multilingual manuscripts;
* project-specific terminology;
* Word templates;
* LaTeX;
* Quarto;
* journal-specific formatting requirements.

Formatting requirements belong to the project configuration rather than the universal framework.

## 14. Auditability Without Transcript Dependence

Consequential AI involvement should be documented sufficiently to understand:

* which tool was used;
* for what purpose;
* which project artifacts it used;
* which outputs it produced;
* what verification occurred;
* whether researcher approval was required.

Full raw chat histories should not be the only source of this information.

## 15. Privacy and Data Governance

AI tools must respect confidentiality, institutional rules, data-use agreements, and legal restrictions.

Restricted or confidential information must not be sent to external AI systems unless explicitly permitted.

## 16. Incremental Complexity

The system should begin simple.

New:

* rules;
* agents;
* skills;
* automation;
* software;
* verification procedures

should be added when repeated experience demonstrates a need.

Complexity must solve a research problem rather than become a research problem itself.
