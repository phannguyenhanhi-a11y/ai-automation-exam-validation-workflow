# AI Automation – Quy trình tạo đề thi và thẩm định chéo bằng AI

Repository này chứa mã nguồn (workflow n8n) của một hệ thống tự động hóa
việc tạo đề thi và thẩm định chéo đề thi bằng trí tuệ nhân tạo.
Hệ thống cho phép AI đóng vai trò như một hội đồng chuyên môn,
đánh giá độ phù hợp, độ khó và mức độ bám sát mục tiêu bài dạy của đề thi.

---

## 1. Mục tiêu của sản phẩm

Sản phẩm được xây dựng nhằm:
- Tự động hóa quy trình tạo đề thi từ dữ liệu đầu vào
- Đảm bảo đề thi bám sát mục tiêu bài dạy và ma trận đánh giá
- Thực hiện thẩm định chéo đề thi bằng AI theo vai trò hội đồng chuyên môn
- Hỗ trợ giáo viên phát hiện và chỉnh sửa lỗi về nội dung, độ khó, hình thức trình bày
- Nâng cao chất lượng đề kiểm tra trong dạy học Toán phổ thông

---

## 2. Ý nghĩa sư phạm

Trong quy trình này, AI không thay thế giáo viên
mà đóng vai trò là công cụ hỗ trợ chuyên môn.
Việc thẩm định chéo bằng AI giúp:
- Giảm sai sót trong quá trình ra đề
- Chuẩn hóa đề thi theo mục tiêu và chuẩn kiến thức – kỹ năng
- Hỗ trợ giáo viên ra đề nhanh hơn nhưng vẫn đảm bảo chất lượng

---

## 3. Công nghệ sử dụng

- n8n: Nền tảng tự động hóa workflow
- OpenAI (GPT-4o-mini): 
  - Tạo dàn ý đề thi
  - Biên soạn đề thi
  - Thẩm định chéo và chỉnh sửa đề thi
- Google Sheets: Nhận dữ liệu đầu vào từ biểu mẫu
- Google Docs: Đọc nội dung tài liệu bài học
- Google Drive: Lưu trữ đề thi hoàn chỉnh

---

## 4. Mô tả quy trình workflow

Workflow bao gồm các bước chính:

1. Nhận dữ liệu đầu vào từ Google Sheets (lớp, môn, chủ đề, link tài liệu)
2. Đọc nội dung tài liệu bài học từ Google Docs
3. AI lập dàn ý đề thi theo ma trận đánh giá
4. Bóc tách và xử lý nội dung đề thi
5. Tạo đề thi hoàn chỉnh theo định dạng chuẩn
6. Gom dữ liệu từ nhiều nhánh xử lý
7. Tổng hợp nội dung đề thi
8. Thẩm định chéo đề thi bằng AI:
   - Đánh giá độ chính xác kiến thức
   - Đánh giá độ khó so với mục tiêu bài dạy
   - Kiểm tra lỗi chính tả, định dạng
9. Hoàn chỉnh đề thi sau thẩm định
10. Lưu trữ đề thi hoàn chỉnh lên Google Drive

---

## 5. Thẩm định chéo bằng AI

Trong bước thẩm định chéo, AI được thiết lập đóng vai:
- Hội đồng thẩm định đề thi độc lập

AI thực hiện:
- Rà soát nội dung kiến thức Toán học
- Đối chiếu độ khó với ma trận đề
- Phát hiện điểm chưa hợp lý
- Đề xuất và thực hiện chỉnh sửa trực tiếp

Kết quả đầu ra là một đề thi hoàn chỉnh,
chỉ bao gồm nội dung đề thi,
không kèm nhận xét hay phân tích trung gian.

---

## 6. Mã nguồn

Mã nguồn workflow được lưu dưới dạng file JSON của n8n:

- Quy trình tạo đề thi tự động thẩm định chéo.json

File này có thể được import trực tiếp vào n8n
để tái sử dụng hoặc mở rộng cho các môn học khác.

---

## 7. Ngữ cảnh học phần

Sản phẩm được xây dựng trong khuôn khổ học phần:
Trí tuệ nhân tạo trong Giáo dục

Sinh viên ngành Sư phạm Toán  
Trường Đại học Sư phạm Thành phố Hồ Chí Minh.

---

## 8. Ghi chú

Sản phẩm mang tính học thuật và thực nghiệm,
phục vụ cho mục đích học tập, nghiên cứu
và ứng dụng AI trong giáo dục phổ thông.
