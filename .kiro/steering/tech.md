---
inclusion: always
---
# Technical Stack & Credit-Efficient Rules

- **Runtime & Workspaces**: Node.js 22+, TypeScript 5.x, npm workspaces (`packages/veriguard-core`, `app-finops-guard`, `app-sre-healer`).
- **Property-Based Testing (PBT)**: Use `fast-check` and `vitest` to translate every formal Correctness Property in `.kiro/specs/**/design.md` into executable randomized property tests (100+ runs per property with counterexample shrinking).
- **MCP Integration**: Expose `veriguard-core` capabilities (`veriguard_evaluate_action`, `veriguard_run_pbt_fuzzer`, `veriguard_time_travel_rollback`) via `@modelcontextprotocol/sdk` and configure `.kiro/settings/mcp.json`.
- **Credit Efficiency**: Write modular, clean code; keep responses concise; never read `node_modules` or lockfiles.
