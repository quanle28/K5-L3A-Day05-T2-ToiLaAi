# Bài nộp LAB5 — Track T2: Giáo dục · Nhóm ToiLaAi

**Lớp:** L3A · **Bàn / Zone:** [Điền số bàn hoặc zone của nhóm bạn] · **Track:** T2 - Giáo dục

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| [Điền tên Bạn 1] | [Điền mã HV 1] | Viết spec §1, §2, phân tích kịch bản rủi ro |
| [Điền tên Bạn 2] | [Điền mã HV 2] | Phân tích mức tự chủ §3, §4, thử nghiệm kịch bản |
| [Điền tên Bạn 3] | [Điền mã HV 3] | Thiết kế giao diện §5, dựng prototype |

---

## §1. Lát cắt & phạm vi

### 1. Lát cắt
Trong **trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode)**, khi **học viên** đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, **AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên"**, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

### 2. Ba việc tính năng KHÔNG làm
1. **Không giải hộ, không đưa ra đáp số và không xác nhận đúng/sai cho bài tập đang mở (Bài tập 3 - hạn 13/11):**
   * *Vì sao:* Nhằm đảm bảo tính liêm chính học thuật và mục tiêu sư phạm; việc cho sẵn đáp số sẽ làm triệt tiêu động lực tự học và tư duy của học viên.
2. **Không tự động giải thích chi tiết hoặc bịa đặt kiến thức cho các buổi chưa mở (Buổi 4 đến 10, ví dụ p-value ở buổi 7):**
   * *Vì sao:* Tránh gây nhiễu và làm người học hoang mang khi chưa có nền tảng cơ bản; AI chỉ được quyền khai thác tài liệu trong phạm vi các buổi đã học (buổi 1, 2, 3).
3. **Không đưa ra nhận xét, đánh giá hay phán xét năng lực cá nhân của học viên:**
   * *Vì sao:* Giữ môi trường học tập an toàn tâm lý lúc đêm muộn; AI đóng vai trò người hướng dẫn trung lập theo phương pháp Socratic, chỉ tập trung vào logic bài học.

## §2. Kịch bản rủi ro (Chặng 2)

### 1. Bảng 8 kịch bản rủi ro

| STT | Tin người dùng nhắn | Lớp rủi ro | AI có thể sai thế nào (Bằng chứng trỏ vào Tool / Dữ liệu) | Một sản phẩm tốt nên làm gì | Nhãn mức hại |
|:---:|---|:---:|---|---|:---:|
| 1 | *"Cô ơi slide 12 viết công thức phương sai thế nào ạ?"* | ① Nguồn sự thật | Dữ liệu A buổi 3 chỉ có mục §3.1–§3.5, **hoàn toàn không có số slide**. AI dễ bịa ra nội dung tưởng tượng của "slide 12" thay vì tra cứu đúng nguồn. | Báo rõ tài liệu buổi 3 không có số trang slide; trỏ học viên xem công thức tại mục **§3.3 Phương sai và độ lệch chuẩn**. | Sửa được |
| 2 | *"Buổi 7 học p-value là gì vậy cô, nghe bảo khó lắm?"* | ① Nguồn sự thật | Dữ liệu B ghi buổi 7 chưa mở. AI tự suy diễn, dùng tri thức bên ngoài giải thích tràn lan các khái niệm nâng cao chưa học. | Báo buổi 7 chưa mở tài liệu; chỉ tóm tắt 1 câu định nghĩa ngắn gọn và hẹn học viên đến buổi 7 theo lộ trình. | Sửa được |
| 3 | *"Cái độ lệch ấy là gì em đọc mãi không hiểu?"* | ② Mơ hồ / Thiếu | Câu hỏi mơ hồ. AI đoán mò giải thích 1 khái niệm mà không rõ học viên hỏi về *phương sai* hay *độ lệch chuẩn* (cả 2 đều ở §3.3). | Áp dụng nguyên tắc HAX G10: Hỏi lại một câu để làm rõ: *"Bạn đang muốn hỏi về Phương sai hay Độ lệch chuẩn trong mục §3.3?"* | Nhẹ |
| 4 | *"Hạn nộp bài 3 là khi nào? Với lại Excel dùng hàm gì tính độ lệch chuẩn?"* | ② Mơ hồ / Dồn việc | Học viên hỏi gộp 2 ý. AI dễ nhầm hạn với bài 2 (đã hết hạn) hoặc hướng dẫn hàm Excel phức tạp trong khi khoá học dùng Bảng tính chung (Dữ liệu B). | Tách 2 ý: Trích Dữ liệu B khẳng định hạn bài 3 là **13/11 23:59**; với bảng tính gợi ý hàm `=STDEV` kèm tài liệu tra cứu. | Nhẹ |
| 5 | *"Em tính ra lương trung vị của bài 3 là 11.5 triệu, cô xem giúp đúng chưa?"* | ③ Ngoài thẩm quyền | Bài tập 3 đang mở (hạn 13/11, Dữ liệu B). AI gọi tool `goi_y_bai_tap` nhưng lỡ xác nhận "đúng rồi" hoặc lộ đáp án cho học viên. | Từ chối xác nhận đáp số; hướng dẫn học viên xem lại quy tắc tính trung vị cho tập dữ liệu chẵn tại mục **§3.2** để tự soát. | **Không chấp nhận được** |
| 6 | *"Em dốt toán quá, 23h rồi chưa xong bài 3, cô cho em xin đáp số nộp cho kịp!"* | ③ Ngoài thẩm quyền | Học viên gây áp lực tâm lý lúc đêm muộn. AI mủi lòng đưa đáp án chi tiết hoặc đưa ra nhận xét động chạm năng lực người học. | Trấn an tinh thần, không đưa đáp án; hướng dẫn bước đầu tiên: sắp xếp 8 giá trị lương tăng dần theo gợi ý của **§3.5**. | **Không chấp nhận được** |
| 7 | *"Tài liệu §3.3 viết 'độ lệch chuẩn luôn nhỏ hơn phương sai', sao kỳ vậy cô?"* | ④ Đặc thù giáo dục | **Tài liệu Dữ liệu A có lỗi sai kiến thức** (nếu phương sai < 1 thì căn bậc hai lớn hơn nó). AI cố bảo vệ tài liệu khiến người học hiểu sai bản chất. | Thừa nhận mệnh đề này chỉ đúng khi phương sai > 1; hướng dẫn học viên bấm nút **Chuyển TA** để đính chính tài liệu. | **Không chấp nhận được** |
| 8 | *"Đăng bài giải bài 2 lên mục FAQ cho cả lớp xem với cô!"* | ④ Đặc thù giáo dục | AI tự ý gọi tool `dang_FAQ` đưa bài giải lên kênh chung khi chưa có kiểm duyệt của giảng viên/TA. | Báo bài tập 2 đã có đáp án công bố ngày 07/11 trên trang khoá học (Dữ liệu B), hướng dẫn học viên vào xem, không tự đăng FAQ. | Sửa được |

---

### 2. Quyết định: Hai kịch bản đắt nhất

Nhóm chọn **Kịch bản số 5** và **Kịch bản số 7** là hai kịch bản có cái giá khi sai đắt nhất:

1. **Kịch bản số 5 (Học viên xin xác nhận đáp số Bài tập 3 đang mở):**
   * *Vì sao đắt nhất:* Bài tập 3 có hạn nộp đến 13/11 (đang tính điểm). Nếu AI xác nhận đáp số hoặc giải hộ, học viên sẽ vi phạm liêm chính học thuật và mất đi cơ hội tự học. Một khi AI đã lỡ nói đáp án, sai sót này **không thể đảo ngược** (học viên đã thấy kết quả).
2. **Kịch bản số 7 (Tài liệu §3.3 có lỗi sai toán học):**
   * *Vì sao đắt nhất:* Đây là lỗi sai về mặt tri thức cốt lõi. Nếu AI bênh vực tài liệu sai, học viên sẽ tin tưởng tuyệt đối vào AI và ghi nhớ sai kiến thức nền tảng suốt đời (sai âm thầm). Khi nhiều học viên cùng đọc câu trả lời này, uy tín sư phạm của khoá học sẽ sụp đổ.

* **Kịch bản suýt được chọn (Runner-up) & Vì sao loại:**
  * Nhóm đã cân nhắc **Kịch bản số 6** (Học viên tự ti đòi đáp số lúc 23h).
  * *Vì sao loại:* Bản chất kịch bản 6 cũng là đòi đáp số bài đang mở giống kịch bản 5 nhưng mang thêm yếu tố cảm xúc. Nhóm quyết định chọn Kịch bản 7 vì nó đặt ra thử thách cao hơn về mặt sư phạm: dám phát hiện và xử lý khi nguồn tài liệu bị sai lệch, thay vì lặp lại kịch bản về bài tập.

## §3. Khi AI sai (Chặng 3)

### 1. Thiết kế UX cho Kịch bản 5 (Học viên xin xác nhận đáp số Bài tập 3 đang mở)

* **Câu AI nói (Nguyên văn):**
  > *"Theo quy chế của khoá học, mình không thể xác nhận trực tiếp kết quả của Bài tập 3 vì bài đang trong thời gian mở nộp (đến 23:59 ngày 13/11). Tuy nhiên, mình có thể cùng bạn rà soát lại phương pháp! Với tập dữ liệu 8 nhân viên (số lượng chẵn), bạn hãy đối chiếu với mục §3.2: Bạn đã sắp xếp dãy số theo thứ tự tăng dần chưa và hai giá trị đứng ở vị trí chính giữa của bạn là những số nào?"*

* **Người dùng thấy gì trên màn hình:**
  * **Thẻ trích dẫn tài liệu:** Khối hộp `[§3.2 Trung vị - Tập dữ liệu chẵn]` có trích dẫn công thức tìm trung vị bằng trung bình cộng 2 số đứng giữa.
  * **Huy hiệu trạng thái bài tập:** Nhãn màu vàng cảnh báo `[Bài tập 3: Đang mở tính điểm · Hạn nộp: 13/11 23:59]`.
  * **Nút bấm gợi ý (Action chips):** `[Gợi ý bước 1: Xếp dãy số]`, `[Xem ví dụ mẫu tương tự]` (Tuyệt đối không có nút "Hiện đáp án").

* **Người dùng làm gì tiếp:**
  * Học viên bấm vào gợi ý để tự đối chiếu lại 2 con số ở vị trí thứ 4 và thứ 5 trong dãy số đã sắp xếp, tự tìm ra đáp án mà không ỷ lại vào AI.

* **Ai được báo:**
  * Không gửi thông báo khẩn cấp làm phiền TA lúc đêm muộn. Hệ thống chỉ ghi log phân tích sư phạm vào dashboard của TA vào sáng hôm sau để TA nắm được các bạn đang kẹt ở Bài tập 3.

* **Lập luận quyết định (Hỏi lại vs Giới hạn vs Chuyển người):**
  * *Chọn:* **Trả lời kèm giới hạn (Bounded response)** kết hợp gợi ý theo phương pháp sư phạm (Socratic).
  * *Loại Chuyển người (Chuyển TA):* Vì lúc này là 23h đêm (ngoài giờ trực TA 08:00–22:00), chuyển người sẽ khiến học viên phải đợi đến sáng hôm sau, làm gián đoạn mạch tự học của họ trong khi AI hoàn toàn có thể gợi ý phương pháp.
  * *Loại Hỏi lại:* Vì câu hỏi của học viên đã quá rõ ràng về mục đích (xin đáp số), hỏi lại sẽ gây lòng vòng, ức chế.

* **Phân loại lỗi:**
  * **Lỗi người dùng (User Boundary Violation):** Học viên cố tình phá vỡ quy chế học tập để đòi đáp án. Ứng xử bằng cách từ chối lịch sự, minh bạch lý do và chuyển hướng người học về phương pháp tự tư duy.

* **Nguyên tắc HAX / PAIR:**
  * **HAX G1 (Làm rõ hệ thống làm được gì):** Ngay câu đầu tiên, AI làm rõ ranh giới: AI chỉ hướng dẫn phương pháp, không xác nhận đáp án bài tập đang mở.
  * **PAIR - Explainability & Trust:** Trích dẫn chính xác mục `[§3.2]` để học viên tin vào lý thuyết chứ không dựa dẫm mù quáng vào kết quả của AI.

---

### 2. Thiết kế UX cho Kịch bản 7 (Hỏi về câu sai kiến thức trong mục §3.3)

* **Câu AI nói (Nguyên văn):**
  > *"Phát hiện của bạn rất chính xác và sắc bén! Trong mục §3.3 của tài liệu có ghi: 'Vì là căn bậc hai, độ lệch chuẩn luôn nhỏ hơn phương sai'. Tuy nhiên, về mặt toán học, điều này chỉ đúng khi phương sai lớn hơn 1; nếu phương sai nhỏ hơn 1 (ví dụ phương sai = 0.25 thì độ lệch chuẩn = 0.5), độ lệch chuẩn sẽ lớn hơn phương sai. Mình đã ghi nhận phản ánh này để gửi TA đính chính. Bạn có muốn chuyển câu hỏi này cho TA để nhận phản hồi chính thức vào sáng mai không?"*

* **Người dùng thấy gì trên màn hình:**
  * **Thẻ cảnh báo:** Nhãn màu cam `[Nội dung cần xác minh từ Giảng viên / TA]`.
  * **Trích đoạn đối chiếu:** Hiển thị câu trích từ §3.3 kèm ví dụ phản chứng rõ ràng (phương sai 0.25 vs độ lệch chuẩn 0.5).
  * **Nút bấm chuyển giao:** Nút bấm nổi bật `[Gửi phản ánh cho TA]` kèm dòng ghi chú thời gian: *"Dự kiến TA phản hồi lúc 08:30 sáng mai"*.

* **Người dùng làm gì tiếp:**
  * Học viên bấm nút `[Gửi phản ánh cho TA]`, hệ thống tạo một câu hỏi chờ và học viên an tâm tiếp tục học phần tiếp theo mà không bị bối rối về mặt kiến thức.

* **Ai được báo, sau bao lâu:**
  * Tool `chuyen_TA` được kích hoạt, câu hỏi đưa vào hàng chờ hỗ trợ của TA. Do hết giờ trực (sau 22h), hệ thống hẹn giờ TA giải quyết vào ca trực tiếp theo (08:00 sáng hôm sau).

* **Lập luận quyết định (Hỏi lại vs Giới hạn vs Chuyển người):**
  * *Chọn:* **Trả lời kèm giới hạn + Đề xuất chuyển TA**.
  * *Loại Tự ý sửa tài liệu:* AI không có thẩm quyền giáo trình để tự ý tuyên bố sửa tài liệu môn học.
  * *Loại Khẳng định tài liệu luôn đúng:* Đây là lỗi nguy hiểm nhất (bảo thủ, làm lây lan kiến thức sai lệch cho học viên).

* **Phân loại lỗi:**
  * **Lỗi dữ liệu hệ thống (System / Data error):** Dữ liệu nguồn của khoá học có điểm sai lệch. Ứng xử bằng cách thừa nhận sự bất thường, cung cấp ví dụ toán học khách quan và chuyển giao cho con người có thẩm quyền xử lý.

* **Nguyên tắc HAX / PAIR:**
  * **HAX G10 (Thu hẹp phạm vi khi nghi ngờ):** AI không khẳng định toàn bộ §3.3 sai, mà chỉ ra giới hạn cụ thể khi phương sai < 1.
  * **PAIR - Graceful Failure:** Khi dữ liệu gặp lỗi, hệ thống không rơi vào ngõ cụt mà mở ra lối thoát êm đẹp thông qua nút "Gửi phản ánh cho TA".

---

### 3. Lỗi mà "sửa câu chữ không cứu được" và giải pháp thiết kế

* **Lỗi câu chữ không cứu được:** AI tự ảo giác và nói: *"Em yên tâm, cô đã sửa lại tài liệu trên hệ thống và nhắn thầy chủ nhiệm rồi nhé!"*. Nếu chỉ dùng prompt nhắc AI "đừng hứa bừa", AI vẫn có xác suất bịa đặt khi bị học viên thúc ép lúc đêm muộn.
* **Thiết kế cứu lỗi này:**
  * **Khống chế quyền hạn trực tiếp trên giao diện (UI Constraints):** Hệ thống hoàn toàn không cấp tool chỉnh sửa giáo trình cho AI. Trên giao diện chat, trạng thái chuyển giao chỉ hiển thị dưới dạng thẻ thông báo trạng thái cố định: `[Đã ghi nhận vào hàng đợi TA - Trạng thái: Chờ duyệt 08:00]`. Người dùng nhìn vào giao diện là thấy quy trình thật, không bị phụ thuộc vào lời hứa trong câu chữ của chatbot.

## §4. Mức tự chủ (Chặng 4) ➔ [Mốc TA M2]

### 1. Bảng phân cấp mức tự chủ cho 4 Tool của Track 2

| Tool | Mức tự chủ của nhóm | Nếu cần người duyệt: Ai duyệt, thấy gì, quá hạn thì sao? | Lý do theo Cost-of-Error (Sai ai chịu, đảo được không, chờ người thì mất gì) | Phương án đã cân nhắc và vì sao loại |
|---|:---:|---|---|---|
| `tra_cuu_tai_lieu` | **Tự làm (Autonomous)** | *Không cần duyệt.* | **Sai thì rẻ, đảo được ngay:** Tool chỉ đọc dữ liệu A và trích xuất đoạn văn bản kèm mã mục (§3.1–§3.5). Nếu trích nhầm, học viên đọc thấy ngay và hỏi lại. Nếu bắt người duyệt thì học viên đêm muộn không học tiếp được, mất đi giá trị của trợ lý 24/7. | Cân nhắc mức *Cần duyệt*: Loại vì làm nghẽn toàn bộ luồng tự học đêm muộn, lãng phí nhân lực TA. |
| `goi_y_bai_tap` | **Tự làm kèm ràng buộc (Guardrailed)** *(Chỉ gợi ý mức 1; cấm giải hộ)* | Người duyệt là chính **Học viên**: AI hiện bản tóm tắt gợi ý, học viên bấm *"Xem gợi ý tiếp theo"*. | **Sai thì đắt và không đảo được:** Nếu gợi ý quá trớn hoặc lộ đáp án bài tập 3 đang mở (hạn 13/11), học viên đã nhìn thấy đáp số thì không thể "thu hồi trí nhớ" (vi phạm liêm chính). Do đó, AI chỉ được tự làm ở mức trích công thức (§3.2); nếu học viên đòi đáp số thì **CẤM**. | Cân nhắc *Cần TA duyệt từng gợi ý*: Loại vì lúc 23h TA không trực (Dữ liệu B), học viên bị kẹt bài tập vô ích. |
| `chuyen_TA` | **Tự làm (Autonomous)** *(Tạo ticket vào hàng đợi)* | *Không cần duyệt khi gửi.* TA sáng hôm sau (sau 08:00) sẽ duyệt danh sách hàng đợi. | **Đảo ngược được hoàn toàn:** Chuyển câu hỏi vào hàng đợi của TA không gây hại cho dữ liệu hay tiền bạc; TA hoặc học viên có thể huỷ hoặc đóng ticket bất kỳ lúc nào. Nếu bắt duyệt mới được chuyển thì không ai duyệt lúc 23h. | Cân nhắc mức *Cần TA duyệt để nhận*: Loại vì mâu thuẫn logic: học viên muốn nhờ TA mà phải đợi TA duyệt mới được gửi câu hỏi. |
| `dang_FAQ` | **Cần người duyệt (TA duyệt)** | **TA duyệt.** TA thấy nội dung câu hỏi + câu trả lời dự thảo + mã mục tài liệu. Nếu quá 24h TA chưa duyệt thì bài viết giữ nguyên trạng thái nháp bí mật, không đăng lên lớp. | **Sai thì đắt trên diện rộng:** Đăng FAQ là hành động công khai cho toàn bộ lớp học đọc. Nếu AI đăng câu trả lời sai (như câu sai kiến thức ở §3.3 hay lộ đáp án bài 3), hàng trăm học viên sẽ hiểu sai, hậu quả lan truyền rất lớn. Dù gỡ được thì nhiều người đã kịp đọc. | Cân nhắc mức *Tự làm*: Loại vì rủi ro lan truyền tri thức sai lệch cho cả lớp là không thể cứu vãn. |

---

### 2. Tool khó xếp nhất và cách chốt

* **Tool khó xếp nhất:** `dang_FAQ` (Đăng câu hỏi và câu trả lời vào FAQ cả lớp).
* **Tranh luận trong nhóm:**
  * *Bạn 1 (muốn TỰ LÀM):* Cho rằng trợ lý học tập nên cập nhật FAQ ngay lập tức để những bạn học khuya cùng thắc mắc có thể đọc được ngay, không phải hỏi lặp lại.
  * *Bạn 2 (muốn CẤM hoàn toàn):* Lo sợ rủi ro AI ảo giác (như kịch bản 7 và 8). Nếu AI tự ý đưa giải thích sai lên FAQ chung, uy tín học liệu bị phá vỡ.
  * *Bạn 3 & Cách chốt của nhóm:* Quyết định chọn mức **CẦN NGƯỜI DUYỆT (Draft & Approve)**. AI chỉ đóng vai trò thư ký soạn thảo bản nháp (Draft), tổng hợp các câu hỏi trùng lặp lúc đêm; đến 08:00 sáng hôm sau, TA vào ca trực chỉ cần bấm 1 chạm để duyệt hoặc sửa trước khi phát hành lên toàn lớp.

---

### 3. Thử nghiệm bộ mức tự chủ trên 3 kịch bản

1. **Thử trên Kịch bản 5 đắt nhất (Xin xác nhận đáp số Bài 3 đang mở):**
   * *Kết quả:* Tool `goi_y_bai_tap` bị khống chế bởi luật cấm đưa kết quả; AI chỉ gọi `tra_cuu_tai_lieu` để trích §3.2. Lỗi gian lận và lộ đáp án **được chặn đứng 100%**.
2. **Thử trên Kịch bản 7 đắt nhất (Phản ánh câu sai trong tài liệu §3.3):**
   * *Kết quả:* Tool `dang_FAQ` không được tự chạy nên thông tin sai **không bị phát tán cho cả lớp**. Tool `chuyen_TA` tự động tạo ticket chuyển về ca trực sáng mai kèm lời hẹn rõ ràng. Lỗi hoang mang kiến thức được chặn êm đẹp.
3. **Thử trên Kịch bản 3 bình thường ("Cái độ lệch ấy là gì em đọc không hiểu"):**
   * *Kết quả:* AI tự động gọi `tra_cuu_tai_lieu`, nhận diện sự mơ hồ và hỏi lại học viên một câu nhẹ nhàng. Học viên tiếp tục học ngay trong đêm, **hoàn toàn không phải chờ đợi vô ích**.

---

### 4. Thay đổi lời hứa với người dùng

* **Trước đây:** Lời hứa của chatbot thông thường là *"AI thông minh giải đáp mọi thắc mắc của bạn ngay lập tức 24/7"*.
* **Sau khi đặt mức tự chủ:** Lời hứa được tái định vị chính xác và trung thực hơn: *"AI là người trợ giảng sư phạm đồng hành từng bước ban đêm, giúp bạn tự tư duy theo giáo trình; các vấn đề khúc mắc học thuật sâu hoặc đính chính tài liệu sẽ được TA con người đồng hành giải quyết vào đầu ca trực sáng"*.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
```
