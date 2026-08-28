# Existing Project Migration

This procedure migrates an existing research project into the AI-Mediated Research OS without altering or reorganizing the original project before inspection.

The objective is to preserve existing work, reconstruct provenance, identify uncertainty, and create a clean working repository for continued research.

## 1. Preserve the Original

Treat the existing project directory as source material.

Before migration:

* do not rename files;
* do not delete files;
* do not reorganize folders;
* do not overwrite existing scripts or outputs;
* do not assume the latest-looking file is the correct version.

The original project should remain available as an untouched reference until migration and replication are complete.

## 2. Gather Minimum Migration Information

Determine:

* working project title;
* short project ID;
* research type;
* field/subfield;
* current project stage;
* working language;
* intended manuscript language;
* intended output;
* manuscript format;
* target journal or conference if known;
* primary statistical software;
* data sensitivity;
* execution mode;
* location of the existing project files;
* location and status of the existing data.

Unknown items may remain `undecided` or `unverified`.

## 3. Create a Clean Research OS Project

Create a new project from `templates/project/` using the normal Research OS structure.

Use:

`RESEARCH_PROJECTS_ROOT/<PROJECT_ID>/`

for the new Git repository.

Use:

`RESEARCH_DATA_ROOT/<PROJECT_ID>/`

for external project data when the default data architecture is permitted.

Do not modify the original project directory.

## 4. Perform a Read-Only Inventory First

Before copying or restructuring source material, inspect the existing project and create an inventory.

Record at least:

* manuscripts;
* thesis or report versions;
* R scripts;
* notebooks;
* data files;
* generated tables;
* figures;
* logs;
* saved model objects;
* bibliographies;
* documentation;
* duplicate or similarly named files;
* modification dates when informative.

Do not infer provenance solely from filenames or timestamps.

Create a migration inventory artifact under:

`research/`

or:

`sessions/`

as appropriate.

## 5. Classify Source Files

For each important source file, classify its likely role:

* canonical old manuscript;
* alternative manuscript version;
* thesis/report version;
* candidate analysis script;
* data-cleaning script;
* figure/table script;
* obsolete or uncertain;
* generated output;
* literature material;
* unknown.

Use confidence labels where useful:

* HIGH;
* MEDIUM;
* LOW;
* UNKNOWN.

Do not silently choose one uncertain source as canonical.

## 6. Identify Current Canonical Research Record

When code provenance is uncertain, distinguish between:

* canonical record of what was reported;
* canonical code that generated it.

For example, a submitted manuscript or thesis may be the best evidence of previously reported results even when the exact generating script is unknown.

Record this distinction explicitly.

## 7. Copy Source Material Conservatively

After inventory and researcher approval, copy relevant source materials into the new project.

Prefer preserving original filenames initially.

Suitable destinations may include:

* `manuscript/legacy/`;
* `R/legacy/`;
* `research/legacy/`;
* `output/legacy/`.

Do not overwrite files when multiple versions exist.

Do not copy large datasets into Git.

## 8. Reconstruct Computational Provenance

For empirical projects, identify which scripts plausibly generated which reported results.

Use:

* code contents;
* object names;
* table/figure labels;
* numerical matches;
* modification history;
* output files;
* saved objects;
* manuscript numbers;
* researcher knowledge.

Create a provenance report describing:

* result or manuscript claim;
* likely generating script;
* evidence;
* confidence;
* unresolved discrepancies.

Do not claim exact provenance without sufficient evidence.

## 9. Attempt Replication Before Redesign

Where feasible, first try to reproduce the previously reported analysis before changing the research design.

The replication stage should answer:

* Can the old results be reproduced?
* Which code reproduces them?
* Which results cannot be reproduced?
* Are discrepancies numerical, coding-related, data-related, or methodological?
* Are required source files missing?

Preserve failed replication attempts when they are informative.

## 10. Separate Replication From Revision

Do not mix old-result reconstruction with new methodological changes.

Use explicit stages such as:

1. legacy reconstruction;
2. replication;
3. design review;
4. revised analysis;
5. updated manuscript.

This preserves the ability to distinguish:

* what the old project did;
* what was later changed;
* why it was changed.

## 11. Scientific Design Audit

After the legacy analysis is sufficiently understood, conduct a fresh scientific review.

Possible review areas include:

* research question;
* institutional context;
* estimand;
* treatment definition;
* comparison group;
* identification;
* timing;
* sample construction;
* variable measurement;
* inference;
* robustness;
* interpretation;
* contribution.

Use independent methods review where appropriate.

Design changes require researcher approval.

## 12. Literature Refresh

Do not assume the original literature review remains current.

Use the project's normal literature policy:

1. discover relevant newer literature;
2. researcher screens and reads important papers;
3. trusted Zotero notes enter the project evidence base;
4. AI may synthesize and use the trusted corpus for reframing and design review.

Preserve a distinction between literature used in the old project and literature added during revision.

## 13. New Data or Additional Waves

Treat additional data as a scientific change, not merely a mechanical append operation.

Before adding new waves or sources, check:

* comparability;
* variable definitions;
* sampling changes;
* missing periods;
* institutional timing;
* treatment exposure;
* changes in survey design;
* implications for identification.

Record consequential decisions.

## 14. Revised Computational Pipeline

After replication and scientific review, create a clean current pipeline.

The revised pipeline should:

* use clear file structure;
* avoid unnecessary duplication;
* preserve raw data;
* document transformations;
* generate important outputs reproducibly;
* trace manuscript numbers to computational artifacts;
* remain portable across supported operating systems.

Legacy scripts should remain available until the revised pipeline is verified.

## 15. Independent Verification

Important reconstructed and revised results should receive appropriate independent verification.

This may include:

* deterministic numerical checks;
* alternative implementation;
* Codex or another independent agent;
* fresh-context review;
* researcher review.

Important reviewers should leave persistent artifacts.

## 16. Manuscript Reconstruction and Updating

Do not treat the old manuscript as disposable.

Identify:

* content that remains valid;
* claims requiring revision;
* outdated literature;
* stale numbers;
* old framing;
* sections tied to superseded analysis.

The updated manuscript should draw only on verified current analysis when reporting quantitative findings.

If the old work exists in another language, preserve its substantive content while allowing the new manuscript language and format to differ.

## 17. Initial Migration Checkpoint

Create a checkpoint recording:

* original project location;
* new Research OS project location;
* data location;
* canonical old manuscript or thesis;
* identified candidate scripts;
* unresolved provenance questions;
* replication status;
* immediate next actions.

## 18. Git Initialization

Initialize the migrated project as its own Git repository.

The initial commit should represent the clean migration baseline.

Suggested commit message:

`Initialize <PROJECT_ID> migrated research project`

Do not publish or push to GitHub without researcher authorization.

## 19. Migration Completion Criteria

Migration is complete when:

* the original source remains preserved;
* the new project structure exists;
* important source files are inventoried;
* canonical old outputs are identified;
* provenance uncertainty is documented;
* replication status is explicit;
* unresolved scientific questions are recorded;
* the project has a clear next action.

Migration does not require that the old analysis already be reproduced or that the new design already be finalized.

## Core Rule

Migration is forensic before it is transformative.

First understand what exists and what produced the existing research record. Only then redesign, rewrite, or simplify.
