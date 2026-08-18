# BÁO CÁO BÀI TẬP NHÓM: AI PRODUCT MANAGEMENT
## CASE STUDY: AI SUPPORT RADAR (REVERSE DISCOVERY & PROBLEM INTERVIEW)

---

## 1. THÔNG TIN CÁ NHÂN VÀ NHÓM
- **Mã học viên (MHV):** 2A2020601533
- **Họ và tên:** Hồ Phạm Đức Linh
- **Tên nhóm:** JCungdc - 1
- **Case study đã chọn:** **AI Support Radar** (Hệ thống phân tích tín hiệu học tập sau mỗi phiên để tạo Support Queue cho giảng viên điều phối hỗ trợ).

---

## 2. PROBLEM HYPOTHESIS BRIEF (KẾT QUẢ CHẶNG 1)

### 2.1. Giải mã ngược từ Solution (Reverse Engineering)
- **Solution Directive:** Tính năng AI Support Radar tự động ghi nhận và phân tích các hành vi học tập (di chuyển slide, ghi chú, đánh dấu "Chưa hiểu", thay đổi đáp án, tương tác AI Chat) sau mỗi phiên học để tạo ra một Support Queue (kèm tín hiệu & đề xuất hành động) giúp Giảng viên xem xét và quyết định can thiệp.
- **Capability trung tính:** Khả năng phát hiện sớm và chính xác các học viên đang gặp khó khăn trong việc hiểu bài giảng, cùng nội dung cụ thể cần hỗ trợ, để phục vụ việc điều phối can thiệp kịp thời.
- **Change (Sự thay đổi):**
  - *Trước đây (Before):* Giảng viên ở thế bị động, phải hỏi trực tiếp trên giảng đường: *"Các bạn có ai chưa hiểu bài không?"*. Tỉ lệ phản hồi rất thấp do tâm lý e ngại của học viên $\rightarrow$ Giảng viên bị động và mù thông tin về mức độ hiểu bài thực tế.
  - *Bây giờ (After):* Với năng lực phát hiện sớm, Giảng viên chủ động nắm bắt danh sách và vấn đề cụ thể của từng học viên, từ đó trực tiếp hoặc điều phối Lab Coach xuống hỗ trợ trúng đích mà không cần chờ học viên tự lên tiếng.

### 2.2. Đối tượng & Bối cảnh (Actor, Situation & Job)
- **Actor:**
  - *Học viên:* Người trực tiếp thực hiện hành vi học tập (bị ảnh hưởng / đối tượng nhận hỗ trợ).
  - *Giảng viên:* Người có quyền truy cập Support Queue, nắm bức tranh tổng thể và điều phối nguồn lực hỗ trợ.
  - *Lab Coach (Trợ giảng):* Người tiếp nhận danh sách hỗ trợ từ Giảng viên, trực tiếp can thiệp 1-1 với học viên và cập nhật trạng thái xử lý.
- **Situation (Bối cảnh):** Vào khoảng thời gian 10–15 phút cuối buổi học phức tạp, lớp học có quy mô vừa đến đông, thời lượng can thiệp có hạn và học viên có rào cản tâm lý e ngại đặt câu hỏi trước đám đông.
- **Job-to-be-done (JTBD):** Khi kết thúc một phiên học có nhiều nội dung khó, Giảng viên muốn chủ động xác định chính xác những học viên nào đang gặp lỗ hổng kiến thức và ở nội dung nào (mà không phụ thuộc vào việc học viên có tự giơ tay hay không), để có thể phân bổ và điều phối đội ngũ Lab Coach hỗ trợ kịp thời, đảm bảo chất lượng học tập đồng đều cho cả lớp.

### 2.3. Nỗi đau & Bằng chứng (Pain & Evidence)
- **Pain (Nỗi đau):**
  - *Phía Giảng viên & Lab Coach:* Mất thời gian hỏi han vô ích cuối buổi; Giảng viên "mù" thông tin về mức độ tiếp thu thực tế của lớp; Lab Coach có mặt tại lớp nhưng lúng túng không biết bàn nào cần giúp, dẫn đến lãng phí nguồn lực trợ giảng.
  - *Phía Học viên:* Gặp rào cản tâm lý sợ bị đánh giá nên không dám hỏi; rời buổi học với sự bối rối, không thể hoàn thành bài tập về nhà, dẫn đến tích tụ lỗ hổng kiến thức và tăng nguy cơ tụt lại phía sau hoặc bỏ học.
- **Evidence (Bằng chứng quan sát được):**
  - *Bằng chứng 1 (Dữ liệu học tập):* Điểm số bài quiz kiểm tra nhanh đầu giờ hôm sau rất thấp ở các phần bài giảng khó; tỉ lệ nộp bài tập về nhà (lab/assignment) sụt giảm.
  - *Bằng chứng 2 (Dữ liệu vận hành & Phản hồi):* Kênh tin nhắn riêng của Giảng viên/Lab Coach bị quá tải câu hỏi vào sát deadline nộp bài; khảo sát CSAT/NPS cuối khóa xuất hiện phàn nàn: *"Giảng viên dạy nhanh, không theo kịp nhưng không biết hỏi ai"*.

### 2.4. Problem Hypothesis (Phát biểu giả thuyết vấn đề)
> "Chúng tôi tin rằng **Giảng viên và Lab Coach** đang gặp khó khăn trong việc **xác định và điều phối hỗ trợ kịp thời cho các học viên chưa hiểu bài** vào **thời điểm cuối mỗi buổi học** vì **học viên có tâm lý e ngại không dám chủ động giơ tay hỏi**, dẫn đến **lãng phí nguồn lực trợ giảng và tích tụ lỗ hổng kiến thức khiến kết quả học tập sụt giảm**."

### 2.5. Điều kiện kiểm chứng giả thuyết
- **Điều gì phải đúng để giả thuyết đứng vững (What must be true):**
  1. Giảng viên và Lab Coach thực sự quan tâm, có trách nhiệm và có quỹ thời gian/nguồn lực để can thiệp hỗ trợ cá nhân hóa.
  2. Học viên gặp khó khăn thực sự có nhu cầu được hỗ trợ nhưng rào cản tâm lý ngăn cản họ giơ tay công khai.
  3. Việc can thiệp và giải đáp kịp thời ngay sau buổi học có tác động trực tiếp và đáng kể đến việc cải thiện kết quả học tập và giảm tỉ lệ rớt môn.
- **Điều gì khiến nhóm sửa hoặc bác bỏ giả thuyết (Falsification criteria):**
  1. Giảng viên cho rằng việc học viên tự tìm hiểu là trách nhiệm cá nhân và chỉ đánh giá kết quả qua điểm thi cuối kỳ.
  2. Học viên thích tự thảo luận trong các nhóm bạn riêng hoặc tự tra cứu hơn là nhận hỗ trợ từ Giảng viên/Lab Coach.
  3. Quy mô lớp học hoặc nguồn lực Lab Coach quá mỏng, không thể xử lý việc can thiệp dù biết danh sách học viên gặp khó khăn.

### 2.6. Solution Parking Lot (Bãi đỗ ý tưởng giải pháp)
| STT | Loại giải pháp | Tên giải pháp | Mô tả ngắn |
|---|---|---|---|
| 1 | 📝 Non-AI | **Exit Ticket ẩn danh** | Học viên điền 1 điều chưa hiểu vào form/phiếu ẩn danh trước khi ra về để Lab Coach gom lại hỗ trợ. |
| 2 | 👥 Non-AI | **Peer-Learning Pods** | Phân nhóm nhỏ cố định có bạn học kèm bạn yếu trước khi cần sự trợ giúp từ Giảng viên. |
| 3 | 🤖 AI | **AI Support Radar** | Thu thập telemetry học tập để phân loại và xuất Support Queue cho Giảng viên điều phối Lab Coach. |
| 4 | 🤖 AI | **AI In-Session Copilot** | Chatbot AI tích hợp trực tiếp giải thích lại khái niệm khó riêng cho từng học viên theo thời gian thực. |
| 5 | 🤖 AI | **AI Topic Aggregator** | AI tổng hợp các câu hỏi/hành vi khó thành Top 3 chủ đề nóng để Giảng viên giảng lại chung cho cả lớp. |

---

## 3. CONVERSATION GUIDE PHIÊN BẢN CUỐI (KỊCH BẢN PHỎNG VẤN VẤN ĐỀ)

### 3.1. Mục tiêu & Nguyên tắc (The Mom Test Framework)
- **Mục tiêu:** Xác thực mức độ nghiêm trọng của nỗi đau "mù thông tin tiếp thu của học viên" và hành vi xử lý thực tế của Giảng viên & Học viên.
- **Nguyên tắc cốt lõi:**
  - Tuyệt đối không đề cập đến AI, tính năng phần mềm hay ý tưởng giải pháp.
  - Hỏi về các sự kiện, hành động cụ thể trong quá khứ thay vì hỏi ý kiến hay phỏng đoán tương lai.
  - Lắng nghe 80%, nói 20%; đào sâu vào nguyên nhân gốc rễ (5-Whys).

### 3.2. Kịch bản phỏng vấn Giảng viên / Lab Coach
- **Phần 1: Bối cảnh & Thói quen thực tế (Situation - Warm-up)**
  1. *"Thầy/Cô thường phân bổ khoảng thời gian 10–15 phút cuối mỗi buổi học như thế nào?"*
  2. *"Trong các buổi dạy kiến thức mới và phức tạp, Thầy/Cô thường làm gì để biết được học viên trong lớp đã thực sự hiểu bài hay chưa?"*
- **Phần 2: Đào sâu Nỗi đau & Bằng chứng (Pain & Evidence Deep-dive)**
  3. *"Thầy/Cô hãy nhớ lại lần gần nhất khi đặt câu hỏi 'Cả lớp có ai chưa hiểu không?' và nhận lại sự im lặng. Lúc đó Thầy/Cô đã xử lý tình huống như thế nào?"*
  4. *"Thường thì đến thời điểm nào Thầy/Cô mới nhận ra một học viên đang bị tụt lại phía sau hoặc hổng kiến thức nặng?"*
  5. *"Khi phát hiện ra học viên không hiểu bài qua điểm quiz/bài tập hôm sau, điều đó gây khó khăn hoặc ảnh hưởng thế nào đến tiến độ của lớp?"*
- **Phần 3: Cách giải quyết hiện tại & Rào cản (Current Alternatives & Workarounds)**
  6. *"Hiện tại Thầy/Cô và các bạn Lab Coach đang phối hợp với nhau như thế nào để phát hiện và hỗ trợ các bạn học yếu ngay trong buổi học?"*
  7. *"Thầy/Cô đã từng thử áp dụng công cụ hoặc phương pháp nào khác để học viên chịu nói ra chỗ chưa hiểu chưa? Kết quả lúc đó ra sao và vì sao Thầy/Cô không tiếp tục dùng?"*

### 3.3. Kịch bản phỏng vấn Học viên (Đối tượng tiếp nhận)
- **Phần 1: Bối cảnh học tập**
  1. *"Khi tham gia một buổi học có nhiều kiến thức mới và khó, bạn thường ghi chép và theo dõi bài giảng như thế nào?"*
- **Phần 2: Rào cản tâm lý & Nỗi đau**
  2. *"Hãy kể lại lần gần nhất bạn cảm thấy hoàn toàn không hiểu một phần kiến thức trong buổi học. Lúc đó bạn đã làm gì?"*
  3. *"Điều gì khiến bạn ngần ngại nhất khi có cơ hội giơ tay hoặc bật mic hỏi trực tiếp Giảng viên tại lớp?"*
- **Phần 3: Hành vi bù đắp hiện tại**
  4. *"Sau khi rời một buổi học mà chưa hiểu bài, bạn thường tự giải quyết phần kiến thức đó bằng cách nào? Bạn mất bao nhiêu thời gian cho việc đó?"*

---

## 4. PRACTICE REFLECTION (PHẢN TƯ SAU KHI LUYỆN TẬP)

### Câu 1: Đâu là điểm dễ mắc bẫy làm lộ Solution nhất trong quá trình phỏng vấn và nhóm đã khắc phục như thế nào?
- **Phản tư:** Cạm bẫy lớn nhất là khi người được phỏng vấn than phiền *"Học sinh lười hỏi quá"* hoặc *"Không biết ai đang yếu"*, người phỏng vấn rất dễ buột miệng hỏi gài: *"Nếu có một công cụ AI tự phát hiện và báo danh sách cho Thầy/Cô thì Thầy/Cô thấy sao?"*. Câu hỏi này dẫn dắt người dùng nói dối xã giao (social desirability bias).
- **Cách khắc phục:** Nhóm thiết lập nguyên tắc *"Đóng băng giải pháp"*, chuyển toàn bộ câu hỏi hướng về quá khứ và đào sâu hành vi: *"Lần gần nhất Thầy/Cô thử tìm cách nhận biết học sinh yếu là khi nào, Thầy/Cô đã làm gì và tốn bao nhiêu thời gian?"*.

### Câu 2: Thông tin hoặc insight bất ngờ nhất nhóm nhận được khi đóng vai / phỏng vấn thử là gì?
- **Phản tư:** Nhóm nhận ra rằng Lab Coach có mặt tại lớp thường rơi vào trạng thái "ngại tiếp cận chủ động" vì sợ làm phiền những bạn học viên đang tự tập trung suy nghĩ. Đồng thời, học viên không chỉ ngại Giảng viên mà còn ngại cả việc Lab Coach tiến lại bàn mình vì sợ các bạn xung quanh nghĩ mình học kém.
- **Ý nghĩa với sản phẩm:** Bất kỳ giải pháp hỗ trợ nào (dù là AI hay quy trình) cũng cần đảm bảo tính tinh tế, riêng tư và không gắn mác (labeling/stigmatization) lên học viên.

### Câu 3: Nhóm đã áp dụng kỹ năng đào sâu (Deep-dive probing / 5-Whys) như thế nào để chạm tới Nỗi đau cốt lõi?
- **Phản tư:** Khi giảng viên trả lời: *"Tôi thường cho làm quiz đầu giờ hôm sau để kiểm tra"*, nhóm không dừng lại ở đó mà đào sâu thêm:
  1. *Tại sao lại là đầu giờ hôm sau mà không phải ngay trong buổi học?* $\rightarrow$ *"Vì không đủ thời gian chấm điểm tại lớp."*
  2. *Khi biết điểm quiz thấp vào hôm sau thì điều gì xảy ra?* $\rightarrow$ *"Giảng viên phải chọn: hoặc dạy lại mất tiến độ bài mới, hoặc dạy tiếp thì học sinh rớt luôn."*
- **Kết quả:** Chạm tới nỗi đau thực sự: **Sự đánh đổi tiến độ giảng dạy và chi phí sửa sai kiến thức quá cao khi phát hiện muộn**.

---

## 5. AI SUPPORT LOG (NHẬT KÝ SỬ DỤNG AI TRONG DỰ ÁN)

### 5.1. AI đã hỗ trợ những gì?
- Giúp bóc tách rành mạch giữa **Solution Directive** (giải pháp kỹ thuật cụ thể) và **Capability trung tính** (năng lực chức năng cốt lõi).
- Đồng hành tư duy theo luồng ngược: $\text{Solution} \rightarrow \text{Change} \rightarrow \text{Actor} \rightarrow \text{Situation \& Job} \rightarrow \text{Pain} \rightarrow \text{Evidence}$.
- Gợi ý cấu trúc bộ câu hỏi phỏng vấn vấn đề chuẩn theo triết lý *The Mom Test*, loại bỏ hoàn toàn các câu hỏi mớm ý giải pháp.
- Hỗ trợ brainstorm đa dạng các hướng giải pháp trong Solution Parking Lot (bao gồm cả các phương án Non-AI).

### 5.2. Điểm còn hạn chế / hời hợt của AI trong quá trình làm việc
- **Bẫy giải pháp:** Ở các lượt đầu, một số câu hỏi hoặc mô tả ban đầu của AI còn mang tính lý thuyết chung chung, chưa sát với mô hình phối hợp thực tế tại giảng đường (nơi có cả Giảng viên và Lab Coach).
- **Thiếu sắc thái bối cảnh:** Ban đầu AI có xu hướng xem học viên là một khối đồng nhất, chưa làm nổi bật được sự khác biệt giữa học viên tự tin và học viên có tâm lý e ngại.

### 5.3. Nhóm đã tự điều chỉnh và hoàn thiện như thế nào?
- **Bổ sung vai trò Lab Coach:** Nhóm chủ động đưa thêm actor "Lab Coach" và quy trình phối hợp phân cấp (Giảng viên duyệt $\rightarrow$ Lab Coach thực thi) vào toàn bộ phân tích JTBD và kịch bản phỏng vấn.
- **Chuẩn hóa lại JTBD:** Nhóm tự điều chỉnh câu JTBD từ hành vi bề nổi (*"muốn học sinh tự raise"*) sang giá trị cốt lõi (*"chủ động nắm bắt thông tin để điều phối can thiệp trúng đích"*).
- **Cá nhân hóa câu hỏi phỏng vấn:** Tinh chỉnh các câu hỏi phỏng vấn cho cả Giảng viên và Học viên để đào sâu vào các rào cản tâm lý thực tế tại môi trường giáo dục Việt Nam.