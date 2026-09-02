# START HERE — AI Research OS

## What this repository is

This is a framework repository, not a research project. It holds the rules and
templates from which individual research projects are created.

Three layers:

* `PRINCIPLES.md` — the framework's rules, independent of any tool.
* `IMPLEMENTATION.md` and `researcher/PROFILE.md` — current tool choices and
  researcher preferences.
* `templates/project/` — copied to create each project. Never edit it while
  creating one.

`NEW_PROJECT.md` and `MIGRATE_PROJECT.md` are procedures to execute, not
background reading.

## If you are an AI agent

Read in this order, stopping when you have what the task requires:

1. `PRINCIPLES.md`
2. `researcher/PROFILE.md`
3. `IMPLEMENTATION.md`
4. `NEW_PROJECT.md` (new project) or `MIGRATE_PROJECT.md` (existing project)

When working inside a project rather than on this framework, that project's
`PROJECT.md` is the current-state document, and its `CLAUDE.md` or `AGENTS.md`
governs your behaviour. Read those first, then the most recent artifacts in
`sessions/`, `plans/`, `decisions/`, and `verification/`.

## Authority

The researcher is the final scientific decision-maker. Technical work is
normally delegated; consequential scientific choices are escalated.

The boundary is defined in `PRINCIPLES.md` §2 and in each project's
`CLAUDE.md` §4. Read them rather than inferring the line.

## Durable memory

The repository is the project's memory, not the conversation. Reasoning that a
future session would need to reconstruct belongs in a file. See
`PRINCIPLES.md` §3 and §14.

An independent review is evidence for the researcher to weigh, not a decision.
Record material disagreements rather than resolving them silently.

## Data

Research data lives outside Git, under `RESEARCH_DATA_ROOT`. Raw data is
immutable. See `PRINCIPLES.md` §15 and `templates/project/data/README.md`.

## Git rhythm

Tell the researcher explicitly when to SAVE, COMMIT, PUSH, and PULL. The
sequence and its rationale are in `IMPLEMENTATION.md` §7.

## Before consequential work

State back to the researcher:

1. which documents govern this task;
2. which decisions you must not make alone;
3. what artifact you will produce, and when you will commit it.

If any of the three is unclear, ask rather than infer.
