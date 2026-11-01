---
inclusion: always
---
# Product Steering — VeriGuard Studio (Kiroween 2026: Skeleton Crew Category)

## Vision & Category Compliance
**VeriGuard Studio** competes in the **Skeleton Crew** category of Kiroween 2026.
Per official Skeleton Crew rules, this repository MUST contain:
1. **A lean, flexible core skeleton (`packages/veriguard-core`)**: A Spec-Driven Agentic Runtime & Chaos Property-Based Testing (PBT) Engine providing Copy-on-Write shadow state execution, `fast-check` invariant fuzzing + counterexample shrinking, deterministic 1-click Time-Travel Rollback, and an MCP tool server.
2. **Two separate application folders at the repository root demonstrating versatility**:
   - **`app-finops-guard/`**: Autonomous Financial Reconciliation & Refund Compliance application powered by `veriguard-core` (enforces double-entry accounting conservation and prevents double-refunds or over-refunds).
   - **`app-sre-healer/`**: Autonomous Cloud Incident Diagnosis & Self-Healing Runbook application powered by `veriguard-core` (enforces SLA replica quorum invariants, blocks unsafe port exposures `0.0.0.0/0`, and provides 1-click cluster state rollback).
