# 🎃 Hướng dẫn Chạy Dự Án 100% E2E Trực Tiếp Trong Môi Trường Kiro

Dự án này được cấu hình để chạy **100% End-to-End bên trong Kiro (Kiro IDE / Kiro CLI / Kiro Crew)** nhằm tuân thủ tuyệt đối thể lệ Kiroween 2026 và tối ưu hóa ngân sách **1.000 Kiro Credits**.

---

## Cách 1: Chạy Tự Động E2E Qua `kiro-cli` (Headless Spec -> Build -> Verify)

1. Đăng nhập tài khoản Kiro của bạn trên terminal:
   ```bash
   ~/.local/bin/kiro-cli login
   ~/.local/bin/kiro-cli whoami
   ```
2. Cài đặt Custom Power `studio-harness` vào Kiro (tốn 0 credit):
   ```bash
   ~/.local/bin/kiro-cli powers install ./.kiro/powers/studio-harness
   ```
3. Chạy toàn bộ quy trình 4 Issues trực tiếp bằng `kiro-cli` (tự động dùng `--v3 --mode spec` và `.kiroignore`):
   ```bash
   /Volumes/AllySSD/Projects/devpost-factory/run.sh build /Volumes/AllySSD/Projects/devpost-factory/hackathons/hack-kiroween-2026 kiro
   ```

---

## Cách 2: Mở Trực Tiếp Trong **Kiro IDE (`Kiro.app`)** Hoặc **Kiro Crew (`KiroCrew.app`)**

1. Mở dự án trong Kiro IDE:
   ```bash
   /opt/homebrew/bin/kiro /Volumes/AllySSD/Projects/devpost-factory/hackathons/hack-kiroween-2026
   ```
   *(Hoặc mở `/Applications/KiroCrew.app` và trỏ vào thư mục `hack-kiroween-2026`)*.
2. Chọn mô hình **Auto (1.0x)** để tối ưu hóa 1.000 credits.
3. Chuyển sang chế độ **Spec** trong Kiro IDE và nhập Prompt khởi tạo Spec:
   > *"Read `.kiro/steering/` and `HACKATHON_BRIEF.md`. Create the Kiro Spec for `veriguard-studio` (`requirements.md` using EARS syntax, `design.md` with formal Correctness Properties P1..P6 for `fast-check` Property-Based Testing, and `tasks.md`) along with `DESIGN.md` and `SPEC.md` (`- AC-1` to `- AC-8`)."*
4. Nhấn **Execute Tasks** trong `tasks.md` của Kiro IDE để Kiro lần lượt thực thi:
   - Xây dựng bộ khung lõi `packages/veriguard-core` + MCP Server (`mcp-server.mjs`).
   - Xây dựng 2 ứng dụng độc lập `app-finops-guard/` và `app-sre-healer/` kèm bộ test `fast-check` PBT.
   - Xây dựng giao diện Web Dashboard trực quan ở cổng `3000` và xuất `VALIDATION.md` + `SUBMISSION.md`.
