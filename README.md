# AI-Mediated Research OS

A framework repository for AI-assisted academic research. It is not itself a
research project — it holds the rules, current tool choices, and templates
from which individual research projects are created.

## Layers

* `PRINCIPLES.md` — the framework's rules, independent of any tool.
* `IMPLEMENTATION.md` and `researcher/PROFILE.md` — current tool choices and
  researcher preferences.
* `templates/project/` — copied to create each new project.

## Creating or migrating a project

* Starting fresh: follow `NEW_PROJECT.md`.
* Bringing an existing project into this framework: follow
  `MIGRATE_PROJECT.md`.

Each created project is its own, separate Git repository, initialized from
`templates/project/`. Research data is never stored in Git — it lives outside
the repository, under `RESEARCH_DATA_ROOT`.

## For AI agents

Start at `START_HERE.md`. It sets the reading order and the authority
boundaries for working in this repository or in a project created from it.
