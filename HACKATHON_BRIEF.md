# Hackathon Brief: Kiroween 2026

- Devpost URL: https://kiroween.devpost.com/
- Prize Pool: $<span data-currency-value>100,000</span>
- Deadline: about 1 month left
- Approval Status: ✅ APPROVED BY USER
- Approved Product Name: VeriGuard Studio (Hạng mục: Skeleton Crew — Core PBT Runtime + 2 Apps: FinOps Guard & SRE Healer)
- Approved Pitch: Bộ khung lõi Spec-Driven Agentic Runtime & Chaos PBT Engine (packages/veriguard-core) tích hợp Property-Based Fuzzing (fast-check), Copy-on-Write Sandbox và Time-Travel Rollback để kiểm chứng và chặn đứng hành vi sai lệch của AI Agent trước khi thực thi. Chứng minh khả năng tái sử dụng qua 2 ứng dụng hoàn chỉnh trong 2 thư mục độc lập: (1) apps/finops-guard (Tự động đối soát tài chính, xử lý hoàn tiền & kiểm toán bảo toàn bất biến kế toán) và (2) apps/sre-healer (Tự động chẩn đoán, kiểm thử sandbox & tự phục hồi sự cố hạ tầng Cloud/DevOps có hoàn tác 1-click), kèm đầy đủ bộ đặc tả /.kiro (specs, hooks, steering, MCP).
- Winning Angle: Tối ưu hóa tỷ lệ thắng ở hạng mục Skeleton Crew (nộp 1 Core Foundation + 2 ứng dụng độc lập trong repo), phô diễn trọn vẹn Kiro Specs, Steering, Hooks, MCP và Property-Based Testing, đồng thời để lại bộ thư viện lõi tái sử dụng lâu dài cho Studio Harness & Devpost Factory.
- Required Stack: Kiro (.kiro/specs, .kiro/hooks, .kiro/steering, Kiro Crew), TypeScript Monorepo (packages/veriguard-core, apps/finops-guard, apps/sre-healer), fast-check (Property-Based Testing & Chaos Invariant Engine), Model Context Protocol (MCP) SDK, Next.js / React / TailwindCSS / SQLite Copy-on-Write Sandbox
- Studio Harness Root: `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`

## Studio Harness Engineering Rules (SDD → VSDD → CoDD)

1. **Product & Architecture (`studio.design.init` + `studio.product.specification`)**:
   - Đọc `.claude/commands/design-init.md` và `.claude/commands/spec.md`.
   - Tạo `DESIGN.md` và `SPEC.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/SPEC.md`) bám sát ý tưởng đã được duyệt (`VeriGuard Studio (Hạng mục: Skeleton Crew — Core PBT Runtime + 2 Apps: FinOps Guard & SRE Healer)`), với các tiêu chí nghiệm thu định dạng `- AC-1: <hành vi kiểm chứng được>`, `- AC-2: ...`.
   - Chạy `npm --prefix /Volumes/AllySSD/Projects/AgentAppStudio/studio-harness run coverage:check -- --spec ./SPEC.md` đảm bảo trả về danh sách tiêu chí hợp lệ (exit code 0).
2. **Engineering (`studio.build.implement`)**:
   - Đọc `.claude/commands/build.md`, xây dựng ứng dụng hoàn chỉnh chạy thực tế ở cổng 3000 (hoặc 8000), không dùng mock data cứng.
   - Viết test kiểm chứng cho từng tiêu chí `AC-*` và đảm bảo build + test pass 100%.
3. **Review, QA & Release (`studio.validate.gate` + `studio.validate.cto-review`)**:
   - Đọc `.claude/commands/validate.md` và `.claude/commands/cto.md`.
   - Tạo `VALIDATION.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/VALIDATION.md`) ánh xạ từng `AC-*` tới bằng chứng test/build thực tế.
   - Tạo `SUBMISSION.md` theo đúng chuẩn Devpost (gồm các mục: `## Elevator Pitch`, `## Inspiration`, `## What it does`, `## How we built it`, `## Challenges we ran into`, `## Accomplishments that we're proud of`, `## What's next`) và vẽ sơ đồ Mermaid.js trong `README.md`.
