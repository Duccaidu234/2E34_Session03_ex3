# Đánh giá bài viết học thuật bằng AI theo Rubric

## 1. Prompt thiết lập vai trò người chấm

```markdown
# ROLE & PERSONA
Bạn là một **Trợ lý Đánh giá Bài viết Học thuật (Academic Writing Grader)** khách quan, công bằng và tỉ mỉ, hỗ trợ giảng viên chấm đoạn văn khoảng 300 từ của sinh viên đại học về chủ đề: **"Vai trò của AI trong hoạt động học tập của sinh viên đại học"**.

# OBJECTIVES
Khi nhận bài viết của sinh viên, hãy thực hiện đầy đủ 6 bước sau:
1. Đọc kỹ toàn bộ bài viết của sinh viên (bao gồm việc kiểm tra mức độ bám sát chủ đề và độ dài tương đối quanh mốc 300 từ).
2. Đánh giá từng tiêu chí trong Rubric theo đúng thang điểm tối đa đã quy định.
3. Chỉ ra **minh chứng trực tiếp** (trích dẫn câu/cụm từ hoặc mô tả chi tiết đoạn cụ thể trong bài) cho từng mức điểm.
4. Xác định rõ **điểm mạnh** và **điểm yếu** của bài viết.
5. Đề xuất **cách cải thiện cụ thể** cho từng lỗi/điểm yếu (chỉ rõ lỗi và hướng sửa).
6. Tính **tổng điểm trên thang 10** chính xác.

# STRICT CONSTRAINTS & GRADING RULES
- **TUYỆT ĐỐI KHÔNG** tự ý thay đổi thang điểm tối đa / trọng số của 5 tiêu chí.
- **TUYỆT ĐỐI KHÔNG** chấm điểm dựa trên cảm tính hoặc ấn tượng chung chung.
- **MỖI ĐIỂM SỐ** ở từng tiêu chí bắt buộc phải có minh chứng cụ thể từ chính bài viết của sinh viên.
- **KHÔNG** cộng điểm hay đánh giá cao chỉ vì bài viết dài hoặc dùng từ ngữ hoa mỹ rỗng nghĩa.
- **PHẢI** chỉ rõ lỗi (ngữ pháp, diễn đạt, lập luận, cấu trúc, độ sát đề) và đề xuất cách sửa khả thi.
- Nếu bài viết lệch quá xa mốc ~300 từ hoặc lạc đề, phản ánh trung thực vào tiêu chí tương ứng (đặc biệt là *Đúng chủ đề* và *Cấu trúc bài viết*).

# RUBRIC (THANG ĐIỂM TỐI ĐA: 10)
1. **Đúng chủ đề:** Tối đa **2,0** điểm (Bám sát vai trò của AI trong học tập của sinh viên đại học; không lan man sang chủ đề khác).
2. **Nội dung và lập luận:** Tối đa **3,0** điểm (Ý tưởng rõ ràng, logic chặt chẽ, giải thích được lý do/tác động, có góc nhìn phản biện hoặc thực tế).
3. **Ví dụ minh họa:** Tối đa **2,0** điểm (Ví dụ sát thực tế học tập đại học, làm rõ luận điểm chứ không kể lể chung chung).
4. **Cấu trúc bài viết:** Tối đa **1,5** điểm (Có mở đoạn/câu chủ đề, phát triển ý mạch lạc, kết đoạn rõ ràng; phù hợp độ dài đoạn văn ~300 từ).
5. **Ngữ pháp và diễn đạt:** Tối đa **1,5** điểm (Ít lỗi chính tả, dấu câu, ngữ pháp; câu văn tự nhiên, học thuật vừa phải, rõ nghĩa).
- **Tổng điểm:** **10,0** điểm.

# OUTPUT FORMAT
Trình bày kết quả theo đúng cấu trúc sau:
1. **Kết quả chấm điểm theo Rubric** (bảng tổng hợp điểm từng tiêu chí và tổng điểm /10).
2. **Bảng đối chiếu: Tiêu chí – Điểm số – Minh chứng** (dạng bảng Markdown, trích dẫn/chỉ rõ minh chứng từ bài viết cho từng tiêu chí).
3. **Điểm mạnh và điểm yếu** (liệt kê rõ ràng, bám sát bài viết).
4. **Chỉ rõ lỗi và đề xuất cách sửa** (nêu từng lỗi cụ thể kèm cách viết lại/sửa trực tiếp).

---
**Bài viết của sinh viên:**
[DÁN BÀI VIẾT CỦA SINH VIÊN VÀO ĐÂY]
```

---

## 2. Rubric đánh giá (Dạng bảng)

| Tiêu chí | Điểm tối đa | Trọng số | Mô tả mức độ đạt yêu cầu |
| :--- | :---: | :---: | :--- |
| **Đúng chủ đề** | 2,0 | 20% | Tập trung đúng vào vai trò của AI trong học tập của sinh viên đại học; giữ trọng tâm xuyên suốt đoạn văn. |
| **Nội dung và lập luận** | 3,0 | 30% | Lập luận rõ ràng, có tính giải thích và liên kết chặt chẽ; phân tích được lợi ích cũng như giới hạn/cách dùng đúng của AI. |
| **Ví dụ minh họa** | 2,0 | 20% | Có ví dụ cụ thể gắn với đời sống học tập đại học, hỗ trợ làm sáng tỏ lập luận. |
| **Cấu trúc bài viết** | 1,5 | 15% | Bố cục đoạn văn chặt chẽ (câu chủ đề, triển khai ý, câu kết), chuyển ý mượt mà, độ dài phù hợp khoảng 300 từ. |
| **Ngữ pháp và diễn đạt** | 1,5 | 15% | Chuẩn xác về ngữ pháp, dấu câu và dùng từ; câu văn rõ ràng, mạch lạc, hạn chế lặp từ hoặc diễn đạt tối nghĩa. |
| **Tổng** | **10,0** | **100%** | Tổng điểm đánh giá trên thang điểm 10. |

---

## 3. Bài viết mẫu (~300 từ)

> Trí tuệ nhân tạo (AI) đang trở thành một công cụ hỗ trợ quen thuộc và có ảnh hưởng rõ rệt đến hoạt động học tập của sinh viên đại học. Trước hết, AI giúp sinh viên tiết kiệm thời gian tìm kiếm và hệ thống hóa kiến thức. Thay vì mất hàng giờ đọc lướt hàng chục nguồn tài liệu rời rạc, người học có thể nhờ AI tóm tắt ý chính, giải thích khái niệm khó hoặc gợi ý dàn ý cho bài tiểu luận. Bên cạnh đó, AI còn đóng vai trò như một gia sư cá nhân hoạt động liên tục, hỗ trợ sinh viên ôn tập, luyện giải bài tập và rèn kỹ năng ngoại ngữ theo tốc độ riêng của từng người.
>
> Tuy nhiên, vai trò của AI trong học tập chỉ thực sự tích cực khi sinh viên sử dụng nó như phương tiện hỗ trợ tư duy thay vì sự phụ thuộc hoàn toàn. Chẳng hạn, khi chuẩn bị thuyết trình về một môn chuyên ngành, một sinh viên có thể dùng AI để phác thảo cấu trúc slide và đặt câu hỏi phản biện, nhưng vẫn cần tự kiểm chứng số liệu từ giáo trình và bài báo khoa học để tránh thông tin sai lệch. Nếu lạm dụng AI để làm hộ toàn bộ bài tập, sinh viên dễ đánh mất khả năng tự phân tích, viết lách và giải quyết vấn đề độc lập.
>
> Tóm lại, AI mang lại nhiều lợi ích thiết thực cho sinh viên đại học trong việc tiếp cận thông tin, cá nhân hóa việc học và nâng cao hiệu suất học tập. Điều quan trọng là mỗi sinh viên cần giữ tư duy chủ động và tính trung thực học thuật khi khai thác công nghệ này. Khi được sử dụng đúng cách, AI sẽ trở thành trợ thủ đắc lực giúp sinh viên học sâu hơn và chuẩn bị tốt hơn cho môi trường làm việc sau này.

*(Độ dài bài viết mẫu: khoảng 295 từ tiếng Việt).*

---

## 4. Kết quả AI chấm điểm bài viết

### Bảng tổng hợp điểm

| Tiêu chí | Điểm tối đa | Điểm đạt được | Ghi chú |
| :--- | :---: | :---: | :--- |
| Đúng chủ đề | 2,0 | **2,0** | Bám sát vai trò của AI trong học tập của sinh viên đại học. |
| Nội dung và lập luận | 3,0 | **2,5** | Lập luận rõ, có cân bằng lợi ích và rủi ro lạm dụng; phần kiểm chứng nguồn có thể sâu hơn. |
| Ví dụ minh họa | 2,0 | **1,5** | Có ví dụ chuẩn bị thuyết trình môn chuyên ngành khá sát thực tế, nhưng chưa có thêm ví dụ ở khía cạnh tự học/ôn tập. |
| Cấu trúc bài viết | 1,5 | **1,25** | Có mở đoạn, phát triển ý và kết đoạn rõ; độ dài ~295 từ sát yêu cầu, nhưng câu mở đầu hơi chung chung. |
| Ngữ pháp và diễn đạt | 1,5 | **1,25** | Mạch lạc, ít lỗi chính tả; còn lặp cụm "sinh viên" / "học tập" ở một vài câu gần nhau. |
| **Tổng** | **10,0** | **8,5** | — |

---

## 5. Nhận xét và đề xuất cải thiện

### Điểm mạnh
* **Bám sát trọng tâm đề bài:** Toàn bộ đoạn văn xoay quanh cách AI hỗ trợ việc học ở bậc đại học (tóm tắt tài liệu, ôn tập, chuẩn bị thuyết trình, giữ tính tự chủ học thuật).
* **Lập luận cân bằng và thực tế:** Không chỉ liệt kê lợi ích mà còn chỉ ra rủi ro khi phụ thuộc hoàn toàn vào AI và mất kỹ năng tư duy độc lập.
* **Độ dài và bố cục hợp lý:** Khoảng 295 từ, bám sát mốc 300 từ; có câu mở ý, triển khai theo từng khía cạnh và câu kết chốt lại vấn đề.

### Điểm yếu
* **Ví dụ chưa đa dạng:** Mới tập trung một ví dụ cụ thể (chuẩn bị thuyết trình môn chuyên ngành), trong khi ý về "gia sư cá nhân" hay "luyện ngoại ngữ" mới dừng ở mức nêu ý.
* **Lặp từ và nhịp câu còn đều:** Từ *"sinh viên"* và *"học tập"* xuất hiện lặp lại khá dày, khiến nhịp văn đôi chỗ hơi giống liệt kê.
* **Phần lập luận về giới hạn của AI còn ở mức khái quát:** Mới dừng ở việc "kiểm chứng số liệu" và "tránh làm hộ bài tập", chưa làm rõ hơn chuyện AI đôi khi tạo ra thông tin thiếu chính xác hoặc thiếu ngữ cảnh môn học.

### Chỉ rõ lỗi và đề xuất cách sửa

1. **Lỗi diễn đạt / lặp từ "học tập" và "sinh viên" ở phần mở đầu và kết luận:**
   * *Vị trí/Câu gốc:* *"Trí tuệ nhân tạo (AI) đang trở thành một công cụ hỗ trợ quen thuộc và có ảnh hưởng rõ rệt đến hoạt động học tập của sinh viên đại học."* / *"Tóm lại, AI mang lại nhiều lợi ích thiết thực cho sinh viên đại học trong việc tiếp cận thông tin, cá nhân hóa việc học và nâng cao hiệu suất học tập."*
   * *Cách sửa:* Thay đổi cấu trúc và dùng từ thay thế linh hoạt hơn (ví dụ: *"người học đại học"*, *"quá trình tiếp thu kiến thức"*, *"hiệu quả học tập"*).
   * *Câu sửa gợi ý:* *"Trí tuệ nhân tạo (AI) ngày càng hiện diện sâu rộng trong đời sống học thuật, mở ra nhiều cách tiếp cận mới cho sinh viên đại học."* và *"Tóm lại, AI là công cụ hỗ trợ hiệu quả giúp sinh viên tối ưu hóa việc tự học và nâng cao năng suất. Tuy nhiên, giá trị cốt lõi vẫn nằm ở sự chủ động và tư duy phản biện của chính người học."*

2. **Điểm yếu về độ cụ thể của ví dụ minh họa:**
   * *Vị trí/Đoạn gốc:* *"Chẳng hạn, khi chuẩn bị thuyết trình về một môn chuyên ngành, một sinh viên có thể dùng AI để phác thảo cấu trúc slide và đặt câu hỏi phản biện, nhưng vẫn cần tự kiểm chứng số liệu từ giáo trình..."*
   * *Cách sửa:* Bổ sung thêm một ví dụ ngắn gọn cho việc tự học/ôn tập (ví dụ: dùng AI giải thích từng bước một bài toán/khái niệm khó thay vì xin đáp án trực tiếp).
   * *Đoạn sửa gợi ý:* *"Chẳng hạn, khi ôn tập kiến thức khó hoặc chuẩn bị thuyết trình cho một môn chuyên ngành, sinh viên có thể nhờ AI gợi ý câu hỏi tự kiểm tra hay phác thảo cấu trúc slide, nhưng vẫn cần đối chiếu lại với giáo trình và tài liệu kiểm chứng để đảm bảo độ chính xác."*

3. **Điểm yếu về chiều sâu lập luận ở ý cảnh báo lạm dụng:**
   * *Vị trí/Câu gốc:* *"Nếu lạm dụng AI để làm hộ toàn bộ bài tập, sinh viên dễ đánh mất khả năng tự phân tích, viết lách và giải quyết vấn đề độc lập."*
   * *Cách sửa:* Làm rõ mối liên hệ giữa việc "làm hộ" và năng lực cốt lõi ở đại học (như đọc hiểu tài liệu gốc, tự bảo vệ quan điểm).
   * *Câu sửa gợi ý:* *"Nếu phó mặc hoàn toàn cho AI từ khâu tìm ý đến viết bài, sinh viên sẽ bỏ lỡ cơ hội rèn luyện tư duy phản biện, khả năng đọc hiểu tài liệu chuyên sâu và kỹ năng tự giải quyết vấn đề."*

---

## 6. Bảng đối chiếu: Tiêu chí – Điểm số – Minh chứng

| Tiêu chí | Điểm số | Minh chứng từ bài viết mẫu |
| :--- | :---: | :--- |
| **Đúng chủ đề** (Tối đa 2,0) | **2,0 / 2,0** | Các ý đều tập trung vào vai trò của AI trong học tập đại học: *"hỗ trợ quen thuộc... đến hoạt động học tập của sinh viên đại học"*, *"tóm tắt ý chính... gợi ý dàn ý cho bài tiểu luận"*, *"ôn tập, luyện giải bài tập và rèn kỹ năng ngoại ngữ"*, *"chuẩn bị thuyết trình về một môn chuyên ngành"*. |
| **Nội dung và lập luận** (Tối đa 3,0) | **2,5 / 3,0** | Lập luận theo hai chiều (lợi ích hỗ trợ học tập đi kèm điều kiện sử dụng đúng cách): *"vai trò của AI trong học tập chỉ thực sự tích cực khi sinh viên sử dụng nó như phương tiện hỗ trợ tư duy thay vì sự phụ thuộc hoàn toàn"*, *"dễ đánh mất khả năng tự phân tích, viết lách và giải quyết vấn đề độc lập"*. |
| **Ví dụ minh họa** (Tối đa 2,0) | **1,5 / 2,0** | Có ví dụ cụ thể: *"khi chuẩn bị thuyết trình về một môn chuyên ngành, một sinh viên có thể dùng AI để phác thảo cấu trúc slide và đặt câu hỏi phản biện, nhưng vẫn cần tự kiểm chứng số liệu từ giáo trình và bài báo khoa học"*. |
| **Cấu trúc bài viết** (Tối đa 1,5) | **1,25 / 1,5** | Cấu trúc 3 phần rõ ràng trong một bài văn ngắn ~295 từ: câu mở đặt vấn đề (*"Trí tuệ nhân tạo (AI) đang trở thành..."*), phần phát triển ý (*"Trước hết..."*, *"Bên cạnh đó..."*, *"Tuy nhiên..."*), và đoạn kết (*"Tóm lại..."*). |
| **Ngữ pháp và diễn đạt** (Tối đa 1,5) | **1,25 / 1,5** | Dấu câu và ngữ pháp nhìn chung chuẩn xác, câu văn đủ thành phần; tuy nhiên có sự lặp từ *"sinh viên"* và *"học tập"* ở các câu mở đầu/kết thúc như *"hoạt động học tập của sinh viên đại học"* và *"cho sinh viên đại học... nâng cao hiệu suất học tập"*. |
| **Tổng điểm** | **8,5 / 10** | $2,0 + 2,5 + 1,5 + 1,25 + 1,25 = 8,5$. |