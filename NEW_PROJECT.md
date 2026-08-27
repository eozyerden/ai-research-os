# New Project Initialization

This procedure creates a new project using the AI-Mediated Research OS.

The objective is to minimize manual configuration while preserving explicit researcher control over important project settings.

## 1. Gather Minimum Project Information

Before creating files, determine:

* working project title;
* short project ID;
* research type;
* field/subfield;
* current research stage;
* working language;
* expected manuscript language;
* manuscript format if known;
* target journal/outlet if known;
* primary statistical software;
* data sensitivity;
* execution mode.

Do not require information that is genuinely unknown at project creation.

Use `undecided` where appropriate.

## 2. Confirm the Project ID

Propose a short filesystem-safe project ID.

Example:

`municipal-debt`

rather than:

`My New Municipal Debt Research Project 2026`

The researcher should approve or modify the proposed ID.

## 3. Determine Local Locations

Use:

`RESEARCH_PROJECTS_ROOT`

for the local Git repository.

Use:

`RESEARCH_DATA_ROOT`

for external project data.

Do not hard-code machine-specific absolute paths in project files.

Expected locations:

`RESEARCH_PROJECTS_ROOT/<PROJECT_ID>/`

and:

`RESEARCH_DATA_ROOT/<PROJECT_ID>/`

## 4. Create the Project Repository

Copy the contents of:

`templates/project/`

into:

`RESEARCH_PROJECTS_ROOT/<PROJECT_ID>/`

Do not modify the original template when creating an individual project.

Initialize the new project directory as its own Git repository.

Do not create or publish a GitHub remote unless the researcher authorizes it.

## 5. Create External Data Directories

For projects using the default external-data architecture, create:

`RESEARCH_DATA_ROOT/<PROJECT_ID>/raw/`

`RESEARCH_DATA_ROOT/<PROJECT_ID>/intermediate/`

`RESEARCH_DATA_ROOT/<PROJECT_ID>/external/`

`RESEARCH_DATA_ROOT/<PROJECT_ID>/generated/`

Do not create these directories automatically for confidential or restricted projects until the approved storage arrangement has been confirmed.

## 6. Populate PROJECT.md

Replace the relevant placeholders in `PROJECT.md` using the information collected from the researcher.

Do not invent unknown scientific information.

Use explicit statuses such as:

* `undecided`;
* `unverified`;
* `not yet defined`.

The initial `PROJECT.md` should remain concise.

## 7. Preserve Template Separation

Do not copy researcher-specific machine paths into the project.

Do not copy raw datasets into the Git repository.

Do not convert temporary task instructions into permanent project rules.

Project-specific requirements belong in `PROJECT.md` or appropriate project artifacts.

## 8. Initialize Git

After project creation:

1. inspect the created files;
2. initialize Git;
3. stage the initial project structure;
4. prepare an initial commit.

Recommended initial commit message:

`Initialize <PROJECT_ID> research project`

Do not push to GitHub without researcher authorization.

## 9. Create Initial Project State

Create an initial session/checkpoint record describing:

* project creation;
* known current state;
* unresolved setup questions;
* immediate next actions.

If consequential scientific decisions already exist, create decision records as appropriate.

## 10. Report Completion

When initialization is complete, report:

* local repository location;
* external data location;
* Git status;
* project language;
* manuscript format;
* execution mode;
* unresolved setup issues;
* recommended next action.

Do not overwhelm the researcher with implementation details unless something requires attention.

## Core Rule

Project initialization should reduce administrative burden.

Ask only questions required to create a safe and usable project. Unknown research details can be developed collaboratively after initialization.
