---
name: "studio-harness"
displayName: "Studio Harness (SDD -> VSDD -> CoDD) + PBT"
description: "Integrates AgentAppStudio Studio Harness (DESIGN.md, SPEC.md AC-1..N coverage check, Red-Green-Verify build loop, fast-check Property-Based Testing, and VALIDATION.md) natively into Kiro."
keywords: ["studio-harness", "sdd", "vsdd", "codd", "property-based-testing", "fast-check"]
---

# Studio Harness Power for Kiro

1. **Phase 1 (Spec & Design)**: Generate `.kiro/specs/veriguard-studio/` (`requirements.md` in EARS syntax, `design.md` with formal Correctness Properties `P1..P6`, `tasks.md`), `DESIGN.md`, and `SPEC.md` (`- AC-1` to `- AC-8`). Verify with `npm --prefix /Volumes/AllySSD/Projects/AgentAppStudio/studio-harness run coverage:check -- --spec ./SPEC.md`.
2. **Phase 2 (Skeleton Core & PBT)**: Implement `packages/veriguard-core` (Copy-on-Write State Sandbox, `fast-check` Chaos Fuzzer & Shrinker, Time-Travel Rollback Ledger, and MCP Server) + `app-finops-guard` + `app-sre-healer` backend logic with 100% passing unit & property-based tests.
3. **Phase 3 (Interactive UI & E2E)**: Build the unified interactive web console & per-app views running on port 3000 so judges can trigger live AI agent actions, run `fast-check` chaos fuzzing, inspect shrunk counterexamples, and trigger 1-click Time-Travel Rollback.
4. **Phase 4 (Validation & Devpost Write-Up)**: Generate `VALIDATION.md`, update `README.md` with Mermaid architecture diagrams, mark all tasks `[x]` in `.kiro/specs/veriguard-studio/tasks.md`, and write a comprehensive `SUBMISSION.md` covering every Kiro feature used.
