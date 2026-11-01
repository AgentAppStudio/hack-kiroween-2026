# AGENTS.md — Kiroween 2026

Hướng dẫn cho OpenAI Codex CLI (`codex`) & Studio Harness làm việc trên repo này.

## Project

Sản phẩm dự thi Hackathon **Kiroween 2026** (Đã được người dùng phê duyệt ý tưởng):
- **Tên sản phẩm**: VeriGuard Studio (Hạng mục: Skeleton Crew — Core PBT Runtime + 2 Apps: FinOps Guard & SRE Healer)
- **Mô tả**: VeriGuard Studio (Hạng mục: Skeleton Crew — Core PBT Runtime + 2 Apps: FinOps Guard & SRE Healer): Bộ khung lõi Spec-Driven Agentic Runtime & Chaos PBT Engine (packages/veriguard-core) tích hợp Property-Based Fuzzing (fast-check), Copy-on-Write Sandbox và Time-Travel Rollback để kiểm chứng và chặn đứng hành vi sai lệch của AI Agent trước khi thực thi. Chứng minh khả năng tái sử dụng qua 2 ứng dụng hoàn chỉnh trong 2 thư mục độc lập: (1) apps/finops-guard (Tự động đối soát tài chính, xử lý hoàn tiền & kiểm toán bảo toàn bất biến kế toán) và (2) apps/sre-healer (Tự động chẩn đoán, kiểm thử sandbox & tự phục hồi sự cố hạ tầng Cloud/DevOps có hoàn tác 1-click), kèm đầy đủ bộ đặc tả /.kiro (specs, hooks, steering, MCP).
- **Góc độ thắng giải**: Tối ưu hóa tỷ lệ thắng ở hạng mục Skeleton Crew (nộp 1 Core Foundation + 2 ứng dụng độc lập trong repo), phô diễn trọn vẹn Kiro Specs, Steering, Hooks, MCP và Property-Based Testing, đồng thời để lại bộ thư viện lõi tái sử dụng lâu dài cho Studio Harness & Devpost Factory.
- **Quy trình kỹ thuật**: **SDD → VSDD → CoDD** của `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`.

## Architectural decisions (đọc trước khi sửa)

| Quyết định | Lý do | Ngày |
|---|---|---|
| Chốt ý tưởng `VeriGuard Studio (Hạng mục: Skeleton Crew — Core PBT Runtime + 2 Apps: FinOps Guard & SRE Healer)` | Đã qua bước Human Approval Gate trước khi build | 2026-10 |
| Áp dụng Studio Harness (`SDD → VSDD → CoDD`) | Đảm bảo mọi tính năng đều có `DESIGN.md`, `SPEC.md` (`AC-1..N`), test tự động và `VALIDATION.md` | 2026-10 |

## Known gaps (đừng "sửa nhầm")

- Chưa có (cập nhật trong quá trình chạy `/build` và `/validate`).

## Structure aliases (SPEC ↔ code)

- `SPEC.md` → Đặc tả hệ thống & danh sách `- AC-1: ...`
- `DESIGN.md` → Hệ thống thiết kế UI/UX
- `VALIDATION.md` → Báo cáo nghiệm thu theo chuẩn Studio Harness
- `SUBMISSION.md` → Bài thuyết trình nộp Devpost
