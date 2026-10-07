# THI CHUYÊN AI V16 — ONLINE

V16 được thiết kế để biến dự án thành website thật mà người khác có thể mở bằng điện thoại.

## Điểm chính
- Frontend responsive + PWA.
- Node.js/Express backend.
- PostgreSQL: tài khoản, session, kế hoạch, tiến độ, đề đã tạo.
- AI Gia sư.
- AI tạo đề mới.
- Làm đề và chấm trắc nghiệm.
- API key chỉ ở server.
- Có `render.yaml` để triển khai trên Render.

## Chạy thử
1. Cài Node.js 20+.
2. Tạo PostgreSQL database.
3. `npm install`
4. Sao chép `.env.example` thành `.env`.
5. Điền `DATABASE_URL`, `SESSION_SECRET`, `OPENAI_API_KEY`, `OPENAI_MODEL`.
6. `npm start`
7. Mở `http://localhost:3000`.

## Đưa lên mạng
Có thể dùng Render hoặc một host Node.js tương tự:
- Tạo PostgreSQL database.
- Tạo Web Service từ thư mục GitHub này.
- Build: `npm install`
- Start: `npm start`
- Thêm các biến môi trường trong `.env.example`.
- Sau khi deploy, host sẽ cấp một URL HTTPS. Gửi URL đó cho người khác; họ chỉ cần mở bằng điện thoại.

## Quan trọng về model
Không nên đoán tên model API. `OPENAI_MODEL` phải là model hiện thực đang được tài khoản OpenAI API của bạn cho phép dùng.

## Production tiếp theo
Nên bổ sung: email xác minh, quên mật khẩu, giới hạn tốc độ theo IP/tài khoản, CSRF protection, moderation, lưu ảnh vào object storage, admin CMS, ngân hàng đề/công thức thật, và thanh toán nếu cần.

V16 là mã nguồn triển khai; nó chưa tự tạo một URL công khai cho bạn nếu bạn chưa kết nối tài khoản hosting/database.
