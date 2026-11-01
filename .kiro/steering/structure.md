---
inclusion: always
---
# Repository Structure (Mandatory Skeleton Crew Layout)

```text
/
├── .kiro/                        # Kiro Specs, Steering, Hooks, Agents, Powers, MCP settings
├── packages/
│   └── veriguard-core/           # Lean Skeleton Core (Copy-on-Write Kernel, fast-check PBT Fuzzer, Time-Travel Ledger, MCP Server)
├── app-finops-guard/             # Separate App Folder #1: FinOps & Refund Compliance War-Room (Port 3001 / Unified UI)
├── app-sre-healer/               # Separate App Folder #2: Cloud SRE Self-Healing & Blast-Radius Guard (Port 3002 / Unified UI)
├── DESIGN.md                     # Visual & UX Design System (Studio Harness)
├── SPEC.md                       # Master Acceptance Criteria (- AC-1..AC-8)
├── VALIDATION.md                 # Verification & PBT Evidence Report
└── SUBMISSION.md                 # Complete Devpost Submission & "How Kiro Was Used" Write-Up
```
