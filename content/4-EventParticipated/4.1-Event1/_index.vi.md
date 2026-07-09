---
title: "Event 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---
# Bài thu hoạch "FCAJ Community Day - 09/05/2026"

**Ngày diễn ra:** 09/05/2026

### Mục Đích Của Sự Kiện

- Chia sẻ những kinh nghiệm và phương pháp học tập thực tiễn nhằm giúp người học hình thành thói quen học lâu dài dựa trên cách não bộ tiếp nhận và duy trì động lực.
- Giới thiệu các kỹ thuật Prompt Engineering nâng cao, đồng thời làm rõ vai trò của việc tối ưu prompt trong việc cải thiện chất lượng phản hồi từ các mô hình ngôn ngữ lớn (LLM).
- Trao đổi về cơ hội, thách thức của lập trình viên trẻ trong kỷ nguyên AI và nhấn mạnh giá trị của nền tảng kiến thức vững chắc.
- Giới thiệu BMAD — một framework phát triển phần mềm có cấu trúc với sự hỗ trợ của AI, hướng đến quy trình bài bản thay vì cách làm "vibe coding" thiếu định hướng.

### Danh Sách Diễn Giả

- **Mr. Huỳnh Hoàng Long** - FCAJ Member
- **Mr. Nguyễn Tuấn Thịnh** - DevOps/Cloud Engineer (đại diện FCAJ)
- **Mr. Anh Khang** - Solutions Architect tại Cloud Kinetics
- **Ms. Thao Nguyen** - Chuyên gia về phương pháp BMAD

### Nội Dung Nổi Bật

#### Hack Não Để Học Như Nghiện Game (Huỳnh Hoàng Long)

Mở đầu phần chia sẻ, anh Huỳnh Hoàng Long đặt ra một câu hỏi rất gần gũi: vì sao chúng ta có thể dành hàng giờ để xem TikTok nhưng lại nhanh chóng mất tập trung khi học chỉ khoảng 10 phút?

- **Phân tích nguyên nhân tâm lý:** Não bộ có xu hướng ưu tiên những hoạt động ít tốn năng lượng nhưng mang lại phần thưởng nhanh và tạo cảm giác tò mò. Đây cũng chính là cơ chế được các nền tảng mạng xã hội và trò chơi trực tuyến khai thác rất hiệu quả.
- **Cơ chế dopamine:** Dopamine không xuất hiện khi phần thưởng đã nhận được mà được giải phóng ngay từ lúc não bộ **mong đợi** phần thưởng. Điều này giải thích vì sao TikTok hay các trò chơi dạng slot machine có thể giữ chân người dùng trong thời gian dài.
- **Kỹ thuật "hộp phần thưởng bí ẩn":** Chuẩn bị nhiều phần thưởng nhỏ, ghi vào từng mảnh giấy rồi bỏ chung vào một chiếc hộp. Sau mỗi 10 phút học, rút ngẫu nhiên một phần thưởng. Sự tò mò về kết quả tiếp theo sẽ giúp duy trì động lực học tập.
- **Khai thác nỗi sợ mất mát:** Xây dựng thói quen điểm danh học tập hằng ngày tương tự chuỗi streak của Duolingo hoặc hệ thống đăng nhập nhận thưởng trong game. Khi chuỗi ngày càng dài, bạn sẽ có xu hướng cố gắng duy trì để không bị mất.
- **Chia nhỏ nhiệm vụ:** Thay vì học quá nhiều nội dung trong một buổi, hãy chia thành từng mục nhỏ, chẳng hạn mỗi ngày chỉ tập trung vào một dịch vụ AWS. Cách làm này giống như người mới chạy bộ chia quãng đường 5 km thành nhiều chặng ngắn.
- **Quy tắc 2 phút:** Nếu một công việc có thể hoàn thành trong vòng 2 phút thì nên xử lý ngay, tránh trì hoãn.
- **Hệ thống XP:** Tự xây dựng cơ chế tích lũy điểm kinh nghiệm (XP) cho bản thân. Sau khi hoàn thành từng chủ đề sẽ được cộng điểm và tự thưởng khi đạt các cột mốc đã đặt ra.
- **Chia sẻ kiến thức thay vì lướt mạng xã hội:** Thay vì dành nhiều thời gian để lướt bảng tin, hãy biến việc học thành những bài chia sẻ kiến thức. Điều này vừa giúp ghi nhớ tốt hơn, vừa tạo nền tảng để trở thành diễn giả tại các sự kiện như FCAJ Community Day trong tương lai.

#### Automated Prompt Engineering & Proptimizer trên AWS (Nguyễn Tuấn Thịnh)

Anh Nguyễn Tuấn Thịnh thực hiện phần trình bày hoàn toàn bằng tiếng Anh, tập trung vào cách xây dựng prompt hiệu quả để giao tiếp với các mô hình AI hiện đại.

- **Hạn chế của prompt chung chung:** Khi prompt thiếu rõ ràng, AI thường tạo ra kết quả chưa chính xác, tiêu tốn nhiều token hơn, làm tăng chi phí API và dễ dẫn đến hiện tượng hallucination (AI tạo ra thông tin không đúng sự thật).
- **7 thành phần của một prompt hiệu quả:**
  - **Role (Vai trò):** Xác định vai trò mà AI cần đảm nhận (ví dụ: *"You are a senior career coach"*).
  - **Instruction (Chỉ dẫn):** Mô tả cụ thể nhiệm vụ AI cần thực hiện.
  - **Context (Ngữ cảnh):** Cung cấp thông tin nền để AI hiểu đúng vấn đề.
  - **Input (Dữ liệu đầu vào):** Nội dung hoặc dữ liệu cần AI xử lý.
  - **Output Format (Định dạng đầu ra):** Quy định kết quả mong muốn như JSON, Markdown hoặc danh sách bullet.
  - **Examples (Ví dụ):** Đưa ra mẫu tham khảo bằng kỹ thuật Few-shot Prompting để định hướng phản hồi.
  - **Constraints (Ràng buộc):** Xác định giới hạn về ngôn ngữ, độ dài hoặc các yêu cầu cụ thể khác.
- **Các kỹ thuật nâng cao:**
  - **Chain of Thought (CoT):** Hướng dẫn AI suy luận theo từng bước để giải quyết các vấn đề phức tạp.
  - **Self-Consistency:** Tạo nhiều hướng suy luận và lựa chọn kết quả có mức độ đồng thuận cao nhất.
  - **Tree of Thought (ToT):** Cho phép AI mở rộng nhiều nhánh lập luận bằng các chiến lược như BFS hoặc DFS nhằm tìm ra phương án tối ưu.
- **Token Economics:** Token là đơn vị tính toán của các mô hình LLM. Văn bản tiếng Việt thường sử dụng nhiều token hơn tiếng Anh, và tổng chi phí sẽ được tính dựa trên cả token đầu vào lẫn đầu ra.
- **Demo Proptimizer trên AWS:**
  - **Frontend:** Ứng dụng Next.js được triển khai trên Amazon S3 và phân phối nội dung thông qua Amazon CloudFront với OAC.
  - **Xác thực:** Amazon Cognito đảm nhiệm đăng ký, đăng nhập và cấp JWT Token mà không cần tự xây dựng hệ thống xác thực.
  - **API & Backend:** Amazon API Gateway tiếp nhận và định tuyến request đến AWS Lambda để xử lý logic theo mô hình serverless.
  - **AI Core:** Amazon Bedrock cung cấp khả năng truy cập an toàn đến các Foundation Model như Claude hoặc GPT mà không phải triển khai máy chủ riêng.
  - **Lưu trữ:** Amazon DynamoDB lưu trữ lịch sử prompt và dữ liệu người dùng, trong khi Amazon S3 lưu các tài nguyên tĩnh.
  - **Giám sát:** Amazon CloudWatch được sử dụng để theo dõi log của Lambda cũng như hiệu năng của API Gateway.
  - **Tính năng sản phẩm:** Proptimizer là một tiện ích mở rộng trên trình duyệt, cho phép người dùng chọn bất kỳ đoạn văn bản nào trên website, tự động tối ưu thành prompt chất lượng cao trước khi sử dụng với ChatGPT hoặc Gemini.

#### Nền Tảng Kiến Thức & Vai Trò Của AI Đối Với Fresher (Anh Khang)

Anh Khang, hiện là Solutions Architect tại Cloud Kinetics với khoảng 3 năm kinh nghiệm, đã chia sẻ góc nhìn thực tế về yêu cầu tuyển dụng trong bối cảnh AI ngày càng phát triển.

- **Ưu tiên kiến thức nền tảng:** Công nghệ có thể thay đổi rất nhanh, nhưng kiến thức nền luôn là yếu tố cốt lõi. Nhà tuyển dụng không mong đợi ứng viên biết toàn bộ hàng trăm dịch vụ AWS mà cần hiểu thật chắc những dịch vụ quan trọng cùng với quy trình tư duy (**thought process**) rõ ràng.
- **AI khuếch đại năng lực:** AI không thay thế lập trình viên mà giúp phát huy khả năng của họ. Người có nền tảng tốt sẽ tận dụng AI để làm việc hiệu quả hơn, còn người thiếu kiến thức sẽ bộc lộ điểm yếu nhanh hơn.
- **Có thể nhờ AI hỗ trợ nhưng không thể thay thế sự hiểu biết:** Khi đề bài thay đổi hoặc phát sinh yêu cầu mới, những người chỉ sao chép kết quả từ AI sẽ gặp khó khăn, trong khi người hiểu bản chất có thể thích nghi dễ dàng.
- **Không tồn tại một kiến trúc đúng tuyệt đối:** Điều quan trọng nhất là khả năng giải thích vì sao lựa chọn một giải pháp cụ thể. Một lập luận hợp lý và có phân tích sẽ được đánh giá cao hơn việc chỉ ghi nhớ đáp án.
#### BMAD Method — Phát Triển Phần Mềm Có Cấu Trúc Với AI

BMAD (Breakthrough Method for Agile AI-Driven Development) là một framework mã nguồn mở giúp chuẩn hóa quy trình phát triển phần mềm với AI, thay thế cách làm thiếu tổ chức của "vibe coding".

- **Agentic Roles (Vai trò AI chuyên biệt):** Hệ thống phân chia AI thành nhiều vai trò như Product Manager, Architect, Developer, QA và Scrum Master, mỗi agent đảm nhận một giai đoạn cụ thể trong SDLC.
- **Hai giai đoạn chính:**
  - **Phase 1 - Agentic Planning:** Hoàn thiện các tài liệu như PRD, thiết kế kiến trúc và User Stories trước khi bắt đầu lập trình.
  - **Phase 2 - Context-Engineered Development:** Sử dụng toàn bộ tài liệu ở Phase 1 làm ngữ cảnh để AI tạo mã nguồn chính xác, đồng nhất và thuận tiện cho việc bảo trì.
- **Lợi ích thực tiễn:**
  - Hạn chế tình trạng AI hallucination nhờ cơ chế kiểm tra chéo giữa các agent.
  - Tạo ra codebase đi kèm tài liệu đầy đủ, thuận tiện cho việc mở rộng và kiểm tra.
  - Có thể áp dụng từ các dự án cá nhân cho đến hệ thống quy mô doanh nghiệp.
  - Hỗ trợ cài đặt thông qua CLI (`npx bmad-method install`) và tích hợp với Cursor, Claude Code cùng nhiều công cụ AI khác.
### Những Gì Học Được

#### Phương Pháp Học Tập & Phát Triển Bản Thân
- Hiểu rằng cơ chế dopamine có thể được tận dụng để xây dựng một phương pháp học tập phù hợp với bản thân và duy trì động lực trong thời gian dài.
- Dự định áp dụng ngay mô hình "hộp phần thưởng bí ẩn" kết hợp với hệ thống streak hằng ngày vào kế hoạch tự học AWS.

#### Prompt Engineering & Chi Phí AI
- Nắm được cấu trúc gồm 7 thành phần của một prompt hiệu quả cùng các kỹ thuật như CoT và ToT để khai thác tốt hơn khả năng của các mô hình LLM.
- Biết cách ước tính và quản lý lượng token khi phát triển ứng dụng AI trên AWS Bedrock nhằm hạn chế các khoản chi phí phát sinh.

#### Tư Duy Kiến Trúc Cloud
- Có cái nhìn rõ ràng hơn về vai trò của từng dịch vụ trong kiến trúc Serverless trên AWS như S3, CloudFront, Cognito, API Gateway, Lambda, Bedrock, DynamoDB và CloudWatch, cũng như lý do lựa chọn chúng.

#### Làm Việc Với AI Một Cách Chuyên Nghiệp
- Nhận ra rằng AI chỉ đóng vai trò hỗ trợ và nâng cao năng lực, trong khi tư duy và kiến thức nền tảng vẫn là yếu tố quyết định.
- Bắt đầu tìm hiểu BMAD Method với mục tiêu áp dụng vào các dự án cá nhân theo quy trình bài bản và có tổ chức hơn.

### Ứng Dụng Vào Công Việc

- **Nâng cao hiệu quả sử dụng AI:** Vận dụng cấu trúc 7 thành phần của prompt cùng kỹ thuật Chain of Thought vào các công việc thường xuyên như viết tài liệu, đánh giá mã nguồn và tạo test case cho dự án AutoRx.
- **Duy trì việc học:** Xây dựng hệ thống streak kết hợp phần thưởng ngẫu nhiên nhằm tạo động lực và giữ nhịp độ học AWS mỗi ngày.
- **Thử nghiệm BMAD Method:** Áp dụng BMAD trong giai đoạn lập kế hoạch của dự án thực tập để chuẩn bị PRD và tài liệu kiến trúc trước khi bắt đầu phát triển.
- **Kiểm soát chi phí Cloud:** Theo dõi thường xuyên lượng token sử dụng và log của Amazon Bedrock để quản lý hiệu quả chi phí trên tài khoản AWS Lab.

### Trải Nghiệm Trong Event

Đây là lần đầu tôi tham gia FCAJ Community Day và buổi sự kiện đã mang lại nhiều ấn tượng tích cực.

#### Sự kết hợp độc đáo giữa kỹ năng mềm và kỹ thuật
- Thay vì bắt đầu bằng những nội dung thuần kỹ thuật, chương trình mở đầu với chủ đề về **tâm lý học trong học tập**. Bài chia sẻ của Anh Huỳnh Hoàng Long giúp tôi hiểu rõ hơn nguyên nhân khiến nhiều người khó duy trì động lực học tập.

#### Thực hành thực tế trên AWS
- Phần trình diễn **Proptimizer** của anh Nguyễn Tuấn Thịnh là nội dung khiến tôi ấn tượng nhất. Việc quan sát một browser extension vận hành trên kiến trúc Serverless hoàn chỉnh của AWS giúp tôi hình dung rõ hơn về định hướng và mục tiêu của chương trình thực tập.

#### Góc nhìn thực tế từ nhà tuyển dụng
- Những chia sẻ của Anh Khang về cách đánh giá ứng viên và bài tập tuyển dụng khiến tôi thay đổi cách nhìn về việc sử dụng AI, đồng thời nhận ra rằng hiểu bản chất vấn đề luôn quan trọng hơn việc chỉ sao chép kết quả do AI tạo ra.

#### Một số hình ảnh khi tham gia sự kiện
![Slide chia sẻ](/images/slide1.jpg)
> Tổng kết lại, FCAJ Community Day 09/05 là một buổi gặp mặt chất lượng cao, cung cấp cho tôi cả công cụ kỹ thuật (Prompt Engineering, BMAD, Serverless AWS) lẫn mindset (tư duy học tập, nền tảng kiến thức, AI amplify) để phát triển trong sự nghiệp IT một cách bền vững.
