## Spec-driven development (since 01.09.2026)

Long initiatives live in `specs/NNN-slug/` (spec-kit, lean preset; constitution:
`.specify/memory/constitution.md`, read it before working with specs). The source of truth for an
initiative's state = its `spec.md` (header: Статус / Обновлено / Следующий шаг, rewritten as a whole;
the labels stay in Russian because the spec-freshness pre-commit hook parses them).
Finished a step of an initiative - update the spec header in the same pass. A large initiative starts with
`/speckit-specify`; small stuff goes without a spec.
