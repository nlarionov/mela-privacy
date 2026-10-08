# mela-privacy Constitution

Rules for every spec, plan and task list in this repository.
Solo project: author, reviewer and stakeholder are one person (Nikita). No team ceremony.

## Stack (do not repeat in plans)

- Jekyll privacy policy page for Mela (iPhone cycle tracker), hosted on GitHub Pages.
  Content is `index.md`, rendered through `_config.yml`. A push to main publishes the page directly.
- No tests - the green-test gate does not apply.

## How we write artifacts

- Prose in English. IDs (FR-001, SC-001, US1/AC2, T001), section headings and status markers `[ ]`/`[X]` in English.
  Russian stays only in content: UI copy and localizations, text for other people, verbatim quotes.
- Type, file and command names are written as in code.
- No em-dashes in any artifact. No filler slogans: only facts, steps, numbers.
- Every requirement is testable. Success Criteria are measurable and technology-agnostic.
- Every spec has an Out of Scope section: what we deliberately do NOT do.

## Status and progress (the main rule)

- Every spec header carries a rewritable block:
  `Status` (draft | in progress | waiting | done) / `Updated` (YYYY-MM-DD) / `Next step` (one line).
  The block is rewritten as a whole on every state change. Do not append history below it.
- Header limits (checked by the spec-freshness pre-commit hook whenever the header changes): `Status` starts with
  one of the values (or `closed`) and has at most 12 words; `Updated` = the date plus at most 12 words;
  `Next step` = one line, at most 40 words. Details go to the roadmap row notes.
- For the `waiting` state, name what we are waiting for and until what date; if there is objectively no deadline,
  write "no deadline set" explicitly.
- A long initiative (more than one feature or longer than a couple of weeks) keeps a `roadmap.md` in its folder:
  a subtask table `ID | What | Status (planned / in-progress / waiting / done) | Note`. Do not rename IDs.
- Execution progress lives in `tasks.md` as `[X]`; an external artifact is allowed instead of a file path.

## Command boundaries

- `/speckit-implement` and `/speckit-converge` - code features only. Non-code initiatives
  (marketing, docs, presale) run as spec + tasks + roadmap, without implement.
- Tests in tasks: mandatory for code (bug = red test first), not needed for non-code work.

## Branches and merge (Nikita's decision 01.09.2026)

- A spec'd feature that touches code = its own branch `NNN-slug` (created by `/speckit-specify` through the
  git extension). Small stuff (point fix, tweak, docs) goes straight to main.
- Merge to main only with green tests: a pack scaled to the change (/qa, testmap where present),
  full for a big wave. Red does not merge; it is fixed in the branch.
- Commit and push the branch as work progresses. A feature merges to main after Nikita's manual go-ahead
  if it is user-visible; technical branches can be merged without him after a green gate.
- The git extension's auto-commits are deliberately off: we commit ourselves, with our own messages.
