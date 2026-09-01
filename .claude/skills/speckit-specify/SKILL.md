---
name: speckit-specify
description: Create a feature branch and specification (Nikita workflow).
argument-hint: "Describe the feature you want to specify"
compatibility: Requires spec-kit project structure with .specify/ directory
metadata:
  author: github-spec-kit
  source: preset:nikita
user-invocable: true
disable-model-invocation: false
---

# Speckit Specify Skill

## User Input

```text
$ARGUMENTS
```

## Outline

1. Read `.specify/memory/constitution.md` and follow it (language, status block, bans).

2. Generate a short name for the feature: 2-4 English words, kebab-case (e.g. `symptom-insights`).

3. **Branch (code features only).** If the initiative touches product code, run from the repo root:
   ```bash
   .specify/extensions/git/scripts/bash/create-new-feature-branch.sh --json --short-name "<short-name>" "<feature description>"
   ```
   Parse `BRANCH_NAME` (format `NNN-short-name`) from the JSON. The script creates and switches
   to the branch. If the initiative does not touch code (marketing, ASO, store, docs, presale),
   do NOT create a branch - stay on main and derive `NNN` as highest existing `specs/NNN-*` plus one.

4. Create `specs/<NNN-short-name>/` and write `.specify/feature.json`:
   ```json
   { "feature_directory": "specs/<NNN-short-name>" }
   ```

5. Write `specs/<NNN-short-name>/spec.md`:
   - Header status block per constitution: `**Статус**: черновик`, `**Обновлено**: <today>`,
     `**Следующий шаг**: <one line>`, plus the overwrite comment.
   - Sections: Проблема; User Stories (P1-P3); Success Criteria (SC-001..., measurable,
     technology-agnostic); Функциональные требования (FR-001..., each testable);
     Edge Cases; **Out of Scope** (mandatory); Assumptions.
   - Prose in Russian, IDs and section keywords in English, no em-dash.
   - Make informed defaults for unspecified details; at most 3 `[NEEDS CLARIFICATION]` markers
     for genuinely unknowable decisions.

6. If the initiative is long-running (more than one feature or more than ~2 weeks), also write
   `specs/<NNN-short-name>/roadmap.md`: table `ID | что | статус | заметка`,
   statuses planned / in-progress / waiting / done, IDs immutable.

7. Report: branch (or "main, no branch"), spec path, and open `[NEEDS CLARIFICATION]` questions.
