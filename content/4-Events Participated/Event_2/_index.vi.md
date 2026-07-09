---
title: "AWS AI & Cloud Operations Workshop"
date: 2026-06-12
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch "AWS AI & Cloud Operations Workshop"

### Mục Đích Của Sự Kiện

- Cập nhật xu hướng ứng dụng AI Agent trong vận hành hạ tầng cloud, DevOps và xử lý sự cố hệ thống.
- Tìm hiểu các bài toán thực tế về AI Voice, xử lý tiếng Việt, độ trễ phản hồi và trải nghiệm hội thoại tự nhiên.
- Khám phá cách AI hỗ trợ doanh nghiệp trong tuyển dụng, onboarding, đánh giá ứng viên và tối ưu quy trình nhân sự.
- Liên hệ kiến thức sự kiện với proposal ước tính chi phí AWS cho hệ thống serverless xử lý hàng hóa hư hỏng.

### Danh Sách Diễn Giả

- **Truong Tran** – AI Solution Sales, Noventiq
- **Steve Tran** – CTO/Founder, CloudThinker
- **Trung Vu** – CEO, Revve AI
- **Anh Dang** – Solution Sales, Noventiq
- **Nghi Danh** – AI Engineer, Renova Cloud
- **Kiet Tran** – AI Engineer, AWS Student Builder Group
- **Bao Phan** – Cloud Engineer, Cloud Kinetics
- **Nguyen Nguyen** – Cloud Engineer, Cloud Kinetics
- **Toan Nguyen** – AWS Security Builder

---

### Nội Dung Nổi Bật

#### AgenticOps for Your Cloud

Diễn giả **Steve Tran** chia sẻ về thực trạng vận hành cloud trong các hệ thống microservices phức tạp. Khi log, tracing, metric và alert bị phân tán ở nhiều nơi, kỹ sư vận hành thường mất nhiều thời gian để điều tra nguyên nhân gốc rễ của sự cố.

- **Thực trạng vận hành cloud**: Các hệ thống hiện đại có nhiều thành phần độc lập, làm cho quá trình giám sát, truy vết lỗi và phản hồi sự cố trở nên khó khăn hơn.
- **Giải pháp AgenticOps**: AI Agent được dùng để tự động hóa các bước điều tra, tổng hợp dữ liệu và đề xuất hướng xử lý, giúp giảm thời gian phân tích từ hàng giờ xuống còn vài phút.
- **Quy trình hoạt động**:
  - **Classification**: Phân loại sự cố từ alert hoặc yêu cầu trực tiếp.
  - **Investigation**: Phân tích log, metric, topology và giả thuyết nguyên nhân.
  - **Mitigation**: Gợi ý phương án khắc phục an toàn để kỹ sư quyết định.
  - **Optimization**: Đề xuất cải tiến dài hạn nhằm hạn chế lỗi tái diễn.

#### Giọng Nói Của AI (AI Voice)

Phần chia sẻ của **Trung Vu**, **Nghi Danh** và **Kiet Tran** tập trung vào cách xây dựng trải nghiệm hội thoại bằng giọng nói có độ trễ thấp và phù hợp với người dùng Việt Nam.

- **Yêu cầu về độ trễ**: Để hội thoại tự nhiên, hệ thống cần xử lý theo cơ chế streaming từ Speech-to-Text, LLM đến Text-to-Speech, thay vì đợi người dùng nói xong toàn bộ câu lệnh.
- **Thách thức của tiếng Việt**: AI cần hiểu cách xưng hô, giới tính, ngữ cảnh giao tiếp và sắc thái ngôn ngữ để tránh phản hồi thiếu tự nhiên hoặc thiếu tôn trọng.
- **Xử lý giọng vùng miền**: Dữ liệu huấn luyện cần có tỷ lệ giọng vùng miền phù hợp để cải thiện khả năng nhận diện, nhưng vẫn cần kiểm soát để AI không tự động bắt chước giọng địa phương một cách thiếu chuyên nghiệp.

#### Khía Cạnh Kỹ Thuật Và Ứng Dụng Thực Tế Của DevOps Agent

Các diễn giả minh họa tình huống website bị chậm hoặc lỗi do lượng request tăng đột biến. Trong hệ thống truyền thống, kỹ sư phải tự truy cập nhiều dashboard khác nhau để gom log, tracing và metric. Với AI Agent, quá trình này có thể được tự động hóa theo hướng có kiểm soát.

- **Incident Investigation**: AI Agent tổng hợp dữ liệu quan sát được, tạo topology hệ thống và đưa ra giả thuyết về nguyên nhân gây lỗi.
- **Khả năng mở rộng**: Agent có thể tích hợp với MCP (Model Context Protocol), Slack, ServiceNow hoặc các công cụ vận hành khác.
- **Lưu ý bảo mật**: Agent chỉ nên truy cập dữ liệu được cấp quyền rõ ràng. Nếu log chưa được export ra CloudWatch hoặc hệ thống quan sát tập trung, Agent không nên tự ý SSH vào máy chủ để lấy dữ liệu.
- **Demo thực tế**: Tình huống giả lập DDoS với 1.000 request/giây vào ALB, AI Agent phát hiện 10 ECS Tasks bị spam và gợi ý lệnh dừng các task liên quan.

#### Case Study Thực Tế

- **Một trường đại học trực tuyến**: Giảm MTTR từ 2 tiếng xuống còn 28 phút, tương đương nhanh hơn khoảng 77%.
- **Nền tảng công nghệ nhà hàng Zenchef**: Phát hiện lỗi cấu hình trong khoảng 20 phút.

#### AI Và Nguồn Nhân Lực Trong Doanh Nghiệp

Phần trình bày của **Truong Tran** và **Anh Dang** đề cập đến cách AI hỗ trợ bộ phận HR trong tuyển dụng và vận hành nhân sự.

- **Giữ chân nhân tài**: Doanh nghiệp cần giảm rủi ro mất nhân sự sau quá trình đào tạo và onboarding.
- **Đánh giá ứng viên**: AI hỗ trợ đối chiếu CV với mô tả công việc, kiểm tra kỹ năng, kinh nghiệm và mức độ phù hợp.
- **Tự động hóa onboarding**: Rút ngắn thời gian nhân sự mới hòa nhập với quy trình, tài liệu và hệ thống nội bộ.
- **No-code/Low-code với Amazon Q**: HR có thể xây dựng ứng dụng quản lý tuyển dụng hoặc hỗ trợ phân tích hồ sơ mà không cần lập trình phức tạp.
- **Live demo**: Amazon Q được dùng để tạo JD cho vị trí Junior Cloud Engineer, so sánh năng lực ứng viên theo kỹ năng kỹ thuật, tư duy giải quyết vấn đề, giao tiếp và tham khảo mức lương phù hợp.

---

### Những Gì Học Được

#### Tư Duy Vận Hành Cloud Với AI Agent

- Hiểu rõ AI Agent không thay thế hoàn toàn kỹ sư vận hành, mà đóng vai trò trợ lý phân tích dữ liệu, gom ngữ cảnh và đề xuất phương án xử lý.
- Nhận ra tầm quan trọng của observability trong cloud: log, metric, tracing và alert phải được thiết kế tốt thì Agent mới có dữ liệu đáng tin cậy để phân tích.
- Nắm được quy trình vận hành sự cố theo các bước phân loại, điều tra, giảm thiểu tác động và tối ưu dài hạn.

#### Kỹ Thuật Xây Dựng Ứng Dụng AI Voice

- Học được rằng trải nghiệm AI Voice phụ thuộc rất lớn vào latency và khả năng streaming liên tục giữa các thành phần.
- Nhận thức rõ hơn về những khó khăn riêng của tiếng Việt như cách xưng hô, giọng vùng miền và ngữ cảnh giao tiếp.
- Hiểu rằng dữ liệu huấn luyện cần được lựa chọn cẩn thận để cân bằng giữa độ chính xác, tính tự nhiên và sự chuyên nghiệp.

#### Ứng Dụng AI Trong Doanh Nghiệp

- AI có thể giúp tự động hóa các công việc lặp lại trong tuyển dụng, phân tích CV, lên lịch phỏng vấn và hỗ trợ onboarding.
- Các công cụ như Amazon Q giúp người dùng nghiệp vụ tạo ứng dụng nội bộ nhanh hơn, đặc biệt trong các quy trình có nhiều dữ liệu và tiêu chí đánh giá.
- Khi áp dụng AI vào doanh nghiệp, cần chú ý đến quyền truy cập dữ liệu, tính minh bạch và khả năng kiểm soát quyết định cuối cùng bởi con người.

---

### Ứng Dụng Vào Proposal Và Dự Án AWS

- **Thiết kế vận hành cho hệ thống serverless**: Kiến thức về AgenticOps có thể áp dụng vào hệ thống phát hiện và xử lý hàng hóa hư hỏng trên AWS bằng cách chuẩn hóa log từ Lambda, API Gateway, SQS, S3, Rekognition, Textract và DynamoDB về CloudWatch.
- **Tối ưu chi phí theo hướng quan sát được**: Proposal chi phí AWS cho thấy hệ thống thử nghiệm vẫn nằm trong Free Tier. Tuy nhiên khi mở rộng, cần theo dõi metric sử dụng theo từng dịch vụ để kiểm soát chi phí và phát hiện bất thường sớm.
- **Tăng độ tin cậy của quy trình xử lý ảnh**: AI Agent có thể hỗ trợ kiểm tra lỗi trong pipeline S3 → SQS → Lambda → Rekognition/Textract → DynamoDB, đặc biệt khi ảnh xử lý thất bại hoặc độ tin cậy AI thấp.
- **Cải thiện trải nghiệm người dùng**: Kiến thức AI Voice có thể mở rộng cho chức năng nhập thông tin bằng giọng nói trong tương lai, giúp nhân viên kho báo cáo tình trạng hàng hóa nhanh hơn.

---

### Trải Nghiệm Trong Sự Kiện

Sự kiện mang lại góc nhìn thực tế về cách AI đang được đưa vào vận hành cloud, DevOps và quy trình doanh nghiệp. Điểm đáng chú ý là các phần trình bày không chỉ nói về ý tưởng AI tổng quát, mà đi sâu vào các tình huống có thể áp dụng ngay như điều tra sự cố, phân tích log, giảm MTTR, xử lý giọng nói tiếng Việt và tự động hóa tuyển dụng.

- **Không gian học hỏi thực tế**: Người tham gia được nghe các case study cụ thể từ cloud operations, AI Voice và HR automation.
- **Góc nhìn kỹ thuật rõ ràng**: Các diễn giả giải thích cách AI Agent phối hợp với telemetry, MCP, CloudWatch và các công cụ vận hành để hỗ trợ kỹ sư.
- **Liên hệ tốt với dự án cá nhân**: Nội dung sự kiện giúp củng cố cách thiết kế hệ thống AWS không chỉ chạy được, mà còn cần dễ quan sát, dễ kiểm soát chi phí và dễ xử lý sự cố.

#### Một số hình ảnh khi tham gia sự kiện

<div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
  <img src="/Content/4.%20Events%20Participated/Image_event/event2-1.png" alt="AWS AI and Cloud Operations Workshop 1" width="45%" />
  <img src="/Content/4.%20Events%20Participated/Image_event/event2-2.png" alt="AWS AI and Cloud Operations Workshop 2" width="45%" />
</div>
