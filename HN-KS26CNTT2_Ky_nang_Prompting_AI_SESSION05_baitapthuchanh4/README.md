# 4.Yêu cầu đầu ra
- Bạn là giảng viên lập trình cấp cao cần sử dụng AI để phân tích dữ liệu, từ đó đưa ra biện pháp hỗ trợ học tập
- Yêu cầu: Tính mức tăng, giảm điểm của từng sinh viên, xác định sinh viên có dấu hiệu sa sút, so sánh kết quả học tập giữa các sinh viên, đưa ra những vấn đề cần giảng viên xác minh thêm, đề xuất giải pháp cải thiện kết quả học tập.
- Bắt buộc sử dụng Chain-of-Thought, yêu cầu AI phân tích theo từng bước: tính toán → so sánh → nhận định → đề xuất, chỉ sử dụng dữ liệu được cung cấp, không tự suy diễn nguyên nhân khiến sinh viên giảm điểm, mọi nhận định phải có dữ liệu chứng minh.
- Ràng buộc: Bảng phân tích kết quả của 5 sinh viên, xác định nhóm sinh viên có dấu hiệu sa sút, ba nhận định quan trọng từ dữ liệu, ba giải pháp hỗ trợ học tập cụ thể.
- Dữ liệu đầu vào:

Sinh viên|Tuần 1|Tuần 2|Tuần 3
|-|-|-|-|
An|8|7|5
Bình|7|6|4
Chi|9|8|8
Dũng|6|5|3
Hà|8|8|7

> Kết quả AI trả về:

PHẦN 1: QUÁ TRÌNH PHÂN TÍCH THEO CHUỖI TƯ DUY (CHAIN-OF-THOUGHT)

Bước 1: Tính toán (Tính mức tăng, giảm điểm của từng sinh viên qua các tuần)

Công thức xác định thay đổi:

Thay đổi Tuần 2 so với Tuần 1 = Điểm Tuần 2 - Điểm Tuần 1

Thay đổi Tuần 3 so với Tuần 2 = Điểm Tuần 3 - Điểm Tuần 2

Tổng thay đổi toàn bộ quá trình (Tuần 3 so với Tuần 1) = Điểm Tuần 3 - Điểm Tuần 1

Kết quả tính toán chi tiết cho từng sinh viên:

An: Tuần 1 (8) -> Tuần 2 (7, giảm 1 điểm) -> Tuần 3 (5, giảm 2 điểm so với Tuần 2). Tổng thay đổi từ Tuần 1 đến Tuần 3 là giảm 3 điểm.

Bình: Tuần 1 (7) -> Tuần 2 (6, giảm 1 điểm) -> Tuần 3 (4, giảm 2 điểm so với Tuần 2). Tổng thay đổi từ Tuần 1 đến Tuần 3 là giảm 3 điểm.

Chi: Tuần 1 (9) -> Tuần 2 (8, giảm 1 điểm) -> Tuần 3 (8, giữ nguyên so với Tuần 2). Tổng thay đổi từ Tuần 1 đến Tuần 3 là giảm 1 điểm.

Dũng: Tuần 1 (6) -> Tuần 2 (5, giảm 1 điểm) -> Tuần 3 (3, giảm 2 điểm so với Tuần 2). Tổng thay đổi từ Tuần 1 đến Tuần 3 là giảm 3 điểm.

Hà: Tuần 1 (8) -> Tuần 2 (8, giữ nguyên) -> Tuần 3 (7, giảm 1 điểm so với Tuần 2). Tổng thay đổi từ Tuần 1 đến Tuần 3 là giảm 1 điểm.

Bước 2: So sánh (Đối chiếu kết quả học tập giữa các sinh viên)

Về mặt điểm số tuyệt đối:

Chi luôn dẫn đầu lớp qua cả 3 tuần với điểm số cao nhất (Tuần 1: 9, Tuần 2: 8, Tuần 3: 8).

Dũng luôn có mức điểm thấp nhất lớp qua các tuần (Tuần 1: 6, Tuần 2: 5, Tuần 3: 3).

An và Hà có điểm số khởi đầu ở Tuần 1 bằng nhau (8 điểm), nhưng xu hướng diễn biến điểm số các tuần tiếp theo khác nhau (An liên tục giảm, Hà duy trì ổn định hơn ở Tuần 2 rồi mới giảm nhẹ ở Tuần 3).

Về mặt xu hướng biến động điểm số:

Toàn bộ 5 sinh viên (An, Bình, Chi, Dũng, Hà) đều không có tuần nào tăng điểm. Điểm số của tất cả các em hoặc giữ nguyên hoặc giảm đi qua từng tuần.

Tốc độ giảm điểm ở giai đoạn từ Tuần 2 sang Tuần 3 nhanh hơn hoặc bằng giai đoạn từ Tuần 1 sang Tuần 2 đối với nhóm có điểm số suy giảm mạnh (An, Bình, Dũng đều giảm 2 điểm từ Tuần 2 sang Tuần 3, trong khi giai đoạn trước chỉ giảm 1 điểm).

Bước 3: Nhận định (Xác định nhóm sa sút và các nhận định dựa trên dữ liệu)

Xác định nhóm sinh viên có dấu hiệu sa sút rõ rệt: Nhóm sa sút nghiêm trọng (giảm từ 2 điểm trở lên ở chặng cuối và tổng giảm 3 điểm) gồm An, Bình, và Dũng. Cả ba sinh viên này đều có điểm số tụt sâu liên tục qua các tuần (An từ 8 xuống 5; Bình từ 7 xuống 4; Dũng từ 6 xuống 3).

Ba nhận định quan trọng từ dữ liệu:

Toàn bộ 5 sinh viên trong dữ liệu đều ghi nhận sự sụt giảm hoặc trì trệ về điểm số từ Tuần 1 đến Tuần 3, không có trường hợp nào cải thiện điểm số lên mức cao hơn mốc ban đầu của mình.

Sinh viên Dũng xuất phát ở mức thấp nhất lớp (6 điểm ở Tuần 1) và tiếp tục giảm mạnh nhất về mặt tuyệt đối xuống mức thấp báo động là 3 điểm ở Tuần 3.

Sinh viên Chi là người duy nhất duy trì được điểm số ổn định nhất ở giai đoạn cuối (giữ nguyên 8 điểm từ Tuần 2 sang Tuần 3) và có tổng mức giảm qua 3 tuần thấp nhất nhóm (chỉ giảm 1 điểm).

PHÂN TÍCH KẾT QUẢ HỌC TẬP CỦA 5 SINH VIÊN

Sinh viên | Tuần 1 | Tuần 2 | Tuần 3 | Biến động T1 -> T2 | Biến động T2 -> T3 | Tổng thay đổi (T1 -> T3)
|-|-|-|-|-|-|-|
An | 8 | 7 | 5 | -1 | -2 | -3
Bình | 7 | 6 | 4 | -1 | -2 | -3
Chi | 9 | 8 | 8 | -1 | 0 | -1
Dũng | 6 | 5 | 3 | -1 | -2 | -3
Hà | 8 | 8 | 7 | 0 | -1 | -1

NHỮNG VẤN ĐỀ CẦN GIẢNG VIÊN XÁC MINH THÊM

Xác minh mức độ tiếp thu nội dung bài giảng lập trình qua các tuần của nhóm sinh viên có điểm giảm liên tục (An, Bình, Dũng) để biết các em gặp khó khăn cụ thể ở phần kiến thức nào.

Xác minh khối lượng thời gian tự học và mức độ hoàn thành bài tập thực hành lập trình hàng tuần của từng sinh viên trong bảng dữ liệu.

Xác minh lý do điểm số của toàn bộ lớp đều có xu hướng giảm hoặc chững lại từ Tuần 1 sang Tuần 3 (liệu độ khó của nội dung học phần có tăng lên hay có yếu tố khách quan nào tác động chung).

ĐỀ XUẤT 3 GIẢI PHÁP CẢI THIỆN KẾT QUẢ HỌC TẬP

Tổ chức buổi trao đổi hoặc khảo sát 1-1: Giảng viên trực tiếp làm việc với nhóm sinh viên có dấu hiệu sa sút rõ rệt (An, Bình, Dũng) để nắm bắt khó khăn cụ thể của các em đối với các bài tập lập trình từ Tuần 1 đến Tuần 3.

Cung cấp thêm tài liệu hướng dẫn từng bước (Step-by-step guidance): Bổ sung các bài tập mẫu kèm lời giải chi tiết cho các nội dung lập trình đã học qua 3 tuần vừa qua nhằm giúp sinh viên củng cố lại kiến thức nền tảng đang bị hụt.

Thiết lập cơ chế hỗ trợ định kỳ hàng tuần: Theo dõi sát sao điểm số và mức độ nộp bài của sinh viên qua các tuần tiếp theo để đánh giá hiệu quả của các biện pháp hỗ trợ kịp thời.