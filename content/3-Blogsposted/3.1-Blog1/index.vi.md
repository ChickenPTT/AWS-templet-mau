---
title: "Blog 1"
date: 2026-07-06
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# S3 INTELLIGENT-TIERING – KHI LƯU TRỮ DỮ LIỆU TỰ "BIẾT" NÊN NẰM Ở TẦNG NÀO

Trong quá trình xây dựng data lake trên S3, có một bài toán mà nhiều team hay gặp: dữ liệu ngày càng nhiều, nhưng mô hình truy cập của từng loại dữ liệu lại rất khó đoán trước. Có file được đọc liên tục, có file chỉ đọc vài lần rồi bỏ đó, cũng có file gần như không ai đụng tới sau khi upload. Nếu cứ để tất cả nằm ở S3 Standard thì chi phí sẽ đội lên khá nhiều, còn nếu ngồi rà soát thủ công để chuyển storage class thì lại tốn công vận hành. Đây chính là lúc **S3 Intelligent-Tiering** phát huy tác dụng.

Điểm nổi bật nhất ở storage class này là nó tự "quan sát" hành vi truy cập của từng object rồi tự động xếp vào đúng tầng chi phí phù hợp, mà không cần con người can thiệp.

Các điểm chính cần nắm:

* Có 3 tầng hoạt động hoàn toàn tự động: **Frequent Access** (tầng mặc định cho object mới, dành cho dữ liệu truy cập thường xuyên), **Infrequent Access** (tự động chuyển sau 30 ngày không truy cập, chi phí thấp hơn), **Archive Instant Access** (tự động chuyển sau 90 ngày không truy cập, chi phí rẻ hơn nữa nhưng vẫn truy xuất tức thời).
* Có thể bật thêm 2 tầng archive không đồng bộ để tiết kiệm sâu hơn: **Archive Access** (sau tối thiểu 90 ngày không truy cập, thời gian phục hồi khoảng 3–5 giờ) và **Deep Archive Access** (sau tối thiểu 180 ngày, thời gian phục hồi trong vòng 12 giờ). Mốc thời gian này có thể tùy chỉnh lên tới 730 ngày.
* Không tính phí truy xuất dữ liệu (data retrieval) ở bất kỳ tầng nào, kể cả khi object đang ở archive.
* Chi phí phát sinh chủ yếu là một khoản phí giám sát nhỏ theo từng object mỗi tháng; riêng object dưới 128 KB được miễn phí này, phù hợp với hệ thống có nhiều file nhỏ (log, metadata, thumbnail...).
* Phù hợp nhất với các data lake có nguồn dữ liệu đa dạng, nơi việc dự đoán trước pattern truy cập gần như bất khả thi.
* Nếu đã biết chắc 100% một tập dữ liệu chỉ đọc một lần rồi lưu trữ lâu dài (ví dụ backup định kỳ), chuyển thẳng sang Glacier hoặc Standard-IA thủ công có thể tối ưu hơn, vì tránh được khoản phí giám sát hàng tháng.

Tính năng này đặc biệt hữu ích khi khối lượng dữ liệu lớn, mô hình truy cập thay đổi liên tục theo thời gian và team không muốn tốn công sức vận hành để theo dõi, chuyển đổi storage class thủ công.

...Hình ảnh...
![Hình ảnh 1](./Images/hinh1.jpg)
...Link...
- [Manage Amazon S3 storage costs granularly and at scale using S3 Intelligent-Tiering](https://aws.amazon.com/vi/blogs/storage/manage-amazon-s3-storage-costs-granularly-and-at-scale-using-s3-intelligent-tiering/)


