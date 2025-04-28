# Hệ thống phân tán

## Hệ thống phân tán là gì?

Hệ thống phân tán (Distributed System) là một tập hợp các máy tính độc lập phối hợp với nhau để đạt được một mục tiêu chung. Các máy tính này xuất hiện với người dùng như một hệ thống thống nhất, mặc dù về mặt vật lý, chúng có thể được đặt tại nhiều vị trí khác nhau.

Mục tiêu chính của hệ thống phân tán là chia sẻ tài nguyên, tăng hiệu suất xử lý, nâng cao độ tin cậy và khả năng mở rộng so với hệ thống đơn lẻ.

---

## Các ứng dụng của hệ thống phân tán

Hệ thống phân tán có mặt ở khắp nơi trong cuộc sống hiện đại:

- Dịch vụ web như Google, Amazon, Facebook.
- Ứng dụng lưu trữ đám mây như Dropbox, Google Drive.
- Thương mại điện tử như Shopee, Lazada.
- Mạng xã hội như Instagram, TikTok.
- Ứng dụng thanh toán điện tử như MoMo, ZaloPay.
- Hệ thống ngân hàng, giao dịch chứng khoán yêu cầu tính sẵn sàng cao và khả năng chịu lỗi.

---

## Các khái niệm chính của hệ thống phân tán

Trong hệ thống phân tán, một số khái niệm quan trọng cần nắm vững bao gồm:

- **Scalability (Khả năng mở rộng)**: Hệ thống có thể mở rộng về số lượng người dùng, dữ liệu và khối lượng công việc mà không giảm hiệu suất.
- **Fault Tolerance (Khả năng chịu lỗi)**: Hệ thống vẫn tiếp tục hoạt động khi một phần nào đó gặp sự cố.
- **Availability (Tính sẵn sàng)**: Mức độ mà hệ thống luôn sẵn sàng để phục vụ người dùng.
- **Transparency (Tính trong suốt)**: Người dùng không cần quan tâm đến việc hệ thống phân tán; mọi thứ diễn ra như thể là một hệ thống đơn lẻ.
- **Concurrency (Tính đồng thời)**: Nhiều tiến trình có thể thực hiện song song mà không gây xung đột.
- **Parallelism (Song song hóa)**: Các tác vụ được chia nhỏ và xử lý đồng thời để tăng tốc độ xử lý.
- **Openness (Tính mở)**: Hệ thống hỗ trợ khả năng mở rộng, thay đổi hoặc tích hợp dễ dàng các thành phần mới.
- **Vertical Scaling (Mở rộng theo chiều dọc)**: Tăng năng lực của một node (máy chủ) bằng cách nâng cấp phần cứng (RAM, CPU, SSD).
- **Horizontal Scaling (Mở rộng theo chiều ngang)**: Thêm nhiều node mới vào hệ thống để chia tải.
- **Load Balancer (Bộ cân bằng tải)**: Phân phối yêu cầu người dùng tới nhiều server để tối ưu hiệu suất và độ tin cậy.
- **Replication (Sao chép dữ liệu)**: Tạo nhiều bản sao của dữ liệu ở các node khác nhau để tăng độ tin cậy và khả năng truy cập.

---

## Ví dụ: Hệ thống mua vé xem phim online

**Tình huống**: Một ứng dụng đặt vé xem phim như CGV online.

**Mối liên hệ với các thuật ngữ:**

- **Scalability**: Khi có nhiều người truy cập để đặt vé cho một suất chiếu hot, hệ thống cần mở rộng để chịu tải.
- **Fault Tolerance**: Nếu một server bị sự cố, người dùng vẫn có thể đặt vé thông qua các server khác.
- **Availability**: Hệ thống luôn cần sẵn sàng 24/7 vì người dùng có thể mua vé bất kỳ lúc nào.
- **Transparency**: Người dùng không cần biết server đang xử lý yêu cầu ở đâu.
- **Concurrency**: Hàng ngàn người cùng lúc đặt vé, thanh toán.
- **Parallelism**: Xử lý song song việc kiểm tra vé, thanh toán, gửi email xác nhận.
- **Openness**: Hệ thống cần dễ dàng thêm cổng thanh toán mới hoặc rạp chiếu phim mới.
- **Vertical Scaling**: Ban đầu nâng cấp server chính khi lượng đặt vé tăng.
- **Horizontal Scaling**: Sau đó thêm nhiều server phụ để chia tải.
- **Load Balancer**: Chia đều yêu cầu đặt vé đến các server.
- **Replication**: Dữ liệu vé được sao chép giữa các trung tâm dữ liệu để đảm bảo không bị mất.

---

## Kiến trúc của hệ thống phân tán

Hiện nay, có nhiều mô hình kiến trúc phân tán, mỗi mô hình phù hợp với yêu cầu khác nhau:

- **Client-Server**: Máy khách gửi yêu cầu, máy chủ xử lý và phản hồi.  
  _Ví dụ_: Các website thông thường.

- **Peer-to-Peer (P2P)**: Các node vừa là client vừa là server.  
  _Ví dụ_: Torrent.

- **Three-tier architecture**: Bao gồm tầng giao diện, tầng logic nghiệp vụ và tầng cơ sở dữ liệu.

- **Microservices**: Ứng dụng được chia thành nhiều dịch vụ nhỏ, độc lập.  
  _Ví dụ_: Netflix, Amazon.

- **Event-Driven Architecture**: Giao tiếp thông qua các sự kiện bất đồng bộ.  
  _Ví dụ_: Hệ thống thanh toán real-time.

- **Serverless Architecture**: Chạy ứng dụng mà không cần quản lý server, chỉ trả tiền cho tài nguyên sử dụng thực tế.  
  _Ví dụ_: AWS Lambda.

- **Edge Computing**: Xử lý dữ liệu gần người dùng hơn thay vì gửi hết về server trung tâm.  
  _Ví dụ_: IoT, xe tự lái.

---

## Ví dụ: Hệ thống thương mại điện tử

Giả sử bạn xây dựng một website bán hàng như Shopee:

- Tầng frontend giao tiếp với backend thông qua API (Client-Server).
- Các chức năng như quản lý giỏ hàng, thanh toán, giao hàng, mỗi chức năng là một microservice.
- Khi người dùng đặt đơn, sự kiện được kích hoạt và xử lý bất đồng bộ (Event-Driven).
- Dữ liệu giao dịch được lưu trữ ở nhiều nơi khác nhau để tăng tốc độ truy cập (Edge Computing).
- Một số tác vụ như gửi email xác nhận đơn hàng chạy trên nền serverless.

---
