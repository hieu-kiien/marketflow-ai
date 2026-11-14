# Mục Lục Tài Liệu Kỹ Thuật — MarketFlow

> Hệ thống: MarketFlow — AI Marketing Campaign Operations Platform  

---

## Danh Mục Tài Liệu Chính

| Tài liệu | Phạm vi | Nội dung trọng tâm |
|---|---|---|
| [**REQUIREMENTS_AND_DESIGN.md**](REQUIREMENTS_AND_DESIGN.md) | **Kiến trúc & Thiết kế Hệ thống** | Phân tích bài toán quản lý tiếp thị SME Việt Nam; xác định 2 vai trò người dùng (`MANAGER`, `MARKETER`); bảng yêu cầu chức năng (Input/Process/Output); yêu cầu phi chức năng; sơ đồ Use Case; thiết kế CSDL (ERD 14 bảng, ràng buộc toàn vẹn); sơ đồ kiến trúc phân tầng; luồng dữ liệu Trợ lý AI (Sequence Diagram) và cấu trúc Prompt ban đầu. |
| [**AI_ASSISTANT.md**](AI_ASSISTANT.md) | **Phân hệ Trợ lý AI & MCP** | Kiến trúc dịch vụ `ai-runner` nội bộ; tích hợp OpenCode Zen qua OpenCode CLI; danh mục công cụ MCP (Read tools vs Propose tools); cơ chế xác thực Run-Token JWT; luồng sự kiện SSE; tiến hóa prompt qua 4 giai đoạn tối ưu hóa có đo lường thực nghiệm; cơ chế xử lý lỗi (Timeout, Rate Limit, Empty); kiểm soát quyền truy cập dữ liệu và quy trình con người duyệt đề xuất (Human-in-the-Loop). |
| [**AI_ETHICS_AND_PRIVACY.md**](AI_ETHICS_AND_PRIVACY.md) | **An toàn & Quyền riêng tư AI** | Bảo vệ khóa API và bí mật hệ thống; phạm vi dữ liệu gửi tới LLM (chỉ dữ liệu kinh doanh công khai theo quyền, cấm gửi PII); công bố minh bạch điều khoản huấn luyện của mô hình miễn phí; các biện pháp kiểm soát và chống ảo giác số liệu (Grounding); bằng chứng thực nghiệm phòng thủ các kịch bản tấn công Prompt Injection trên máy chủ VPS. |
| [**TESTING.md**](TESTING.md) | **Kiểm thử & Đánh giá Tự động** | Hướng dẫn thực thi từng bộ kiểm thử (Backend Pytest, AI Runner Pytest, Frontend TypeScript strict typecheck, ESLint, Vite Production Build, và kịch bản đánh giá Prompt định lượng); số liệu đo lường thực tế; danh mục chi tiết các ca kiểm thử theo từng module nghiệp vụ bao gồm trường hợp bình thường (Normal), lỗi (Error) và biên (Boundary). |
| [**AI_IN_SDLC.md**](AI_IN_SDLC.md) | **Quy trình Kỹ thuật AI trong SDLC** | Ghi nhận ứng dụng AI xuyên suốt vòng đời phát triển: phân tích yêu cầu và kiểm định rủi ro kiến trúc; lập trình đa tác nhân bám sát Design Contract; đo đạc bộ nhớ RSS và khảo sát mô hình miễn phí trên VPS thực tế; các điểm kiểm chứng và hiệu chỉnh chất lượng mã nguồn. |
| [**DEPLOYMENT-VPS.md**](DEPLOYMENT-VPS.md) | **Triển khai & Vận hành Production** | Hướng dẫn triển khai thực tế trên máy chủ VPS Ubuntu 24.04 LTS qua Cloudflare Tunnel; cấu hình các dịch vụ hệ thống systemd (`marketflow-api`, `marketflow-ai-runner`, `nginx`, `postgresql`, `cloudflared`); phân quyền thư mục và giới hạn bộ nhớ an toàn. |
