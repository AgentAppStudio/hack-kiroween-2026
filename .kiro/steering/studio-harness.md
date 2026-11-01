---
inclusion: always
---
# Studio Harness Integration (SDD -> VSDD -> CoDD)

This workspace integrates **AgentAppStudio Studio Harness** (`/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`) with **Kiro Spec-Driven Development**:
1. **SDD (Spec-Driven)**: Create `.kiro/specs/veriguard-studio/requirements.md` (using EARS syntax: `WHEN ... THE SYSTEM SHALL ...`), `design.md` (defining formal **Correctness Properties** `P1..P6` for Property-Based Testing), and `tasks.md`, alongside `DESIGN.md` and `SPEC.md` (`- AC-1: ...` to `- AC-8: ...`).
2. **VSDD (Verified Spec-Driven)**: Follow `.claude/commands/build.md` (Red-Green-Verify). Every task in `.kiro/specs/veriguard-studio/tasks.md` and every `AC-*` in `SPEC.md` must be verified by automated unit + `fast-check` Property-Based Tests.
3. **CoDD (Constraint-Driven Validation)**: Follow `.claude/commands/validate.md` and `.claude/commands/cto.md` to produce `VALIDATION.md`, `README.md` (with Mermaid diagrams), and `SUBMISSION.md`.
