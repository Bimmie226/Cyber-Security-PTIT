# 1.1. Khái quát về an toàn thông tin
- Chúng ta sống trong "thế giới kết nối" với mức độ ngày càng "sâu"
- Ngày càng có nhiều nguy cơ, đe dọa mất an toàn thông tin, 
hệ thống, mạng
- Ngày càng có nhiều nguy cơ, đe dọa mất an toàn thông tin, hệ thống, mạng: 
  - Bị tấn công từ tin tặc 
  -  Bị tấn công hoặc lạm dụng từ người dùng
  - Lây nhiễm các phần mềm độc hại (vi rút, sâu,...) 
  - Nguy cơ bị nghe trộm, đánh cắp và sửa đổi thông tin
  - Lỗi hoặc các khiếm khuyết phần cứng, phần mềm

## Hệ thống thông tin là gì?
- Hệ thống thông tin (IS - Information System) là một hệ thống tích hợp các thành phần nhằm phục vụ việc thu thập, lưu trữ, xử lý thông tin và chuyển giao thông tin, tri thức và các sản phẩm số.
- Sử dụng HTTT để quản lý các hoạt động:
  - Tương tác với: Khách hàng, nhà cung cấp, cơ quan chính quyền
  - Quảng bá thương hiệu và sản phẩm
  - Cạnh tranh với các đối thủ trên thị trường

## Các loại hệ thống thông tin(mô hình tháp)
- Gồm 4 loại theo đối tượng sử dụng

    ![alt text](../images/1_01.png)

  - Hệ thống thông tin **giao dịch(Transactional Processing Systems**) với người sử dụng là các **nhân viên(Workers)**.
  - Hệ thống thông tin **quản lý(Management Information Systems)** với người sử dụng là các **quản lý bộ phận(Middle Managers)**
  - Hệ thống **trợ giúp ra quyết định(Decision Support Systems)** với người sử dụng là các **quản lý cao cấp(Senior Managers)**
  - Hệ thống thông tin **điều hành(Executive Information Systems**) với người sử dụng là các **Giám đốc điều hành(Executives)**

## Một số hệ thống thông tin điển hình
- Các kho dữ liệu (data warehouses)
- Các hệ lập kế hoạch nguồn lực doanh nghiệp (enterprise resource planning)

## Hệ thống thông tin dựa trên máy tính(Computer-Based Information System)
- Là một hệ thống thông tin sử dụng công nghệ máy tính để thực thi các nhiêm vụ

## Các thành phần của hệ thống thông tin dựa trên máy tính
- `Hardware`: Phần cứng để thu thập, lưu trữ, xử lý và biểu diễn dữ liệu
- `Software`: Các phần mềm chạy trên phần cứng để xử lý dữ liệu
- `Databases`: Lưu trữ dự liệu
- `Networks`: Hệ thống truyền dẫn thông tin/dữ liệu
- `Procedures`: Tập hợp các lệnh kết hợp các bộ phận nêu trên để xử lý dữ liệu, đưa ra kết quả mong muốn

## An toàn thông tin(Information Security) là gì?
- An toàn thông tin là việc bảo vệ chống truy nhập, sử dụng, tiết lộ, 
sửa đổi, hoặc phá hủy thông tin một cách trái phép.

## Hai lĩnh vực chính của ATTT:
- An toàn công nghệ thông tin (IT security)
- Đảm bảo thông tin(Information Assurance):
  -  Đảm bảo thông tin không bị mất khi xảy ra các sự cố (thiên tai, hỏng hóc hệ thống, trộm cắp, phá hoại,…)
  -  Sử dụng backup


## An toàn hệ thống thông tin (ISS - Information Systems Security) 
Là việc đảm bảo các thuộc tính an ninh an toàn của hệ thống thông tin:
- `Bí mật` (Confidentiality)
- `Toàn vẹn` (Integrity)
- `Sẵn dùng` (Availability)

# 1.2. Các yêu cầu đảm bảo ATTT và an toàn HTTT
## Tính bí mật(Confidentiality)
- Chỉ người dùng có thẩm quyền mới được truy nhập thông tin 

## Các thông tin bí mật gồm
- Dữ liệu riêng của cá nhân
- Các thông tin thuộc quyền sở hữu trí tuệ của các doanh nghiệp hay các cơ quan/tổ chức.
- Các thông tin có liên quan đến an ninh quốc gia

## Tính bí mật được đảm bảo bằng kênh mã hòa VPN
## Tính toàn vẹn (Integrity)
- Thông tin chỉ có thể được sửa đổi bởi những người dùng có thẩm quyền

## Tính toàn vẹn liên quan đến tính hợp lệ (validity) và chĩnh xác (accuracy) của dữ liệu
- Trong nhiều tổ chức, thông tin có giá trị lớn, như bản quyền phần mềm, bản quyền âm nhạc, bản quyền phát minh, sáng chế
- Mọi thay đổi không có thẩm quyền có thể ảnh hưởng rất nhiều đến giá trị của thông tin 

## Dữ liệu là toàn vẹn nếu
- Dữ liệu không bị thay đổi
- Dữ liệu hợp lệ
- Dữ liệu chính xác

## Tính toàn vẹn của hệ thống thông tin 
- Thông tin chỉ được sửa đổi bởi người dùng có thẩm quyền

## Tính sẵn dùng (Availability) 
- Thông tin có thể truy nhập bởi người dùng hợp pháp bất cứ khi nào họ có yêu cầu

## Tính sẵn dùng có thể được đo bằng các yếu tố
- Thời gian cung cấp dịch vụ (Uptime)
- Thời gian ngừng cung cấp dịch vụ (Downtime)
- Tỷ lệ phục vụ: A = (Uptime) / (Uptime + Downtime)
- Thời gian trung bình giữa các sự cố
- Thời gian trung bình ngừng để sửa chữa
- Thời gian khôi phục sau sự cố

# 1.3. Các thành phần của an toàn thông tin 
## Các thành phần của ATTT
- An toàn máy tính và dữ liệu(Computer and data security)
- An ninh mạng(Network security)
- Quản lý ATTT(Management of information security)
- Chính sách ATTT(Policy)

# 1.4. Các mối đe dọa & nguy cơ trong các vùng hạ tầng CNTT

| STT | Area                                                  |
| --- | ----------------------------------------------------- |
| 1   | Vùng người dùng(`User domain`)                        |
| 2   | Vùng máy trạm(`Workstation domain`)                   |
| 3   | Vùng mạng LAN(`LAN domain`)                           |
| 4   | Vùng LAN-to-WAN(`LAN-to-WAN domain`)                  |
| 5   | Vùng WAN(`WAN domain`)                                |
| 6   | Vùng truy nhập từ xa(`Remote Access domain`)          |
| 7   | Vùng hệ thống/ứng dụng(`Systems/Applications domain`) |

## Các đe dọa (threats) với vùng người dùng
- Thiếu ý thức về vấn đề an ninh an toàn
- Coi nhẹ các chính sách an ninh an toàn
- Vi phạm chính sách an ninh an toàn
- Đưa CD/DVD/USB với các files cá nhân vào hệ thống
- Tải ảnh, âm nhạc, video
- Phá hoại dữ liệu, ứng dụng và hệ thống
- Tấn công phá hoại từ các nhân viên bất mãn
- Nhân viên có thể dống tiền hoặc chiếm đoạt thông tin quan trọng

## Các đe dọa (threats) với vùng máy trạm
- Truy nhập trái phép vào máy trạm 
- Truy nhập trái phép vào hệ thống, ứng dụng và dữ liệu 
- Các lỗ hổng an ninh trong hệ điều hành máy trạm
- Các lỗ hổng an ninh trong các phần mềm ứng dụng máy trạm
- Các hiểm họa từ virus, mã độc và các phần mềm độc hại
- Người dùng đưa CD/DVD/USB với các files cá nhân vào hệ thống
- Người dùng tải ảnh, âm nhạc, video

## Các đe dọa (threats) với vùng LAN
- Truy nhập trái phép vào mạng LAN vật lý
- Truy nhập trái phép vào hệ thống, ứng dụng và dữ liệu
- Các lỗ hổng an ninh trong hệ điều hành máy chủ 
- Các lỗ hổng an ninh trong các phần mềm ứng dụng máy chủ
- Nguy cơ từ người dùng giả mạo trong mạng WLAN
- Tính bí mật dữ liệu trong mạng WLAN có thể bị đe dọa
- Các hướng dẫn và chuẩn cấu hình cho máy chủ LAN chưa được tuân thủ

## Các đe dọa (threats) với vùng LAN-to-WAN
- Thăm dò và rà quét trái phép các cổng dịch vụ
- Truy nhập trái phép
- Lỗ hổng an ninh trong các bộ định tuyến, tưởng lửa và các thiết bị mạng khác
- Người dùng cục bộ(trong LAN) có thể tải các file không xác định nội dung từ các nguồn không xác định

## Các đe dọa (threats) với vùng WAN
- Rủi ro từ việc dữ liệu có thể được truy nhập trong môi trường công cộng và mở
- Hầu hết dữ liệu được truyền dưới dạng rõ(cleartext/plaintext)
- Dễ bị nghe trộm
- Dễ bị tấn công phá hoại
- Dễ bị tấn công từ chối dịch vụ(DoS) và từ chối dịch vụ phân tán(DDoS)
- Kẻ tấn công có thể tự do, dễ dàng gửi email có đính kèm virus, sâu và các phần mềm độc hại

## Các đe dọa (threats) với vùng truy nhập từ xa
- Tấn công kiểu vét cạn(brute force) vào tên người dùng và mật khẩu
- Tấn công vào hệ thống đăng nhập và điểu khiển truy cập
- Truy nhập trái phép vào hệ thống CNTT, ứng dụng và dữ liệu
- Thông tin bí mật có thể bị đánh cắp từ xa 
- Dò rỉ dữ liệu do vi phạm các tiêu chuẩn phân loại dữ liệu

## Các đe dọa (threats) với vùng hệ thống/ứng dụng
- Truy nhập trái phép đén trung tâm dữ liệu, phòng máy hoặc tủ cáp
- Khó khăn trong quản lý các máy chủ yêu cầu tính sẵn dùng cao
- Lỗ hổng trong quản lý các phần mềm ứng dụng của hệ điều hành máy chủ
- Các vấn đề an ninh trong các môi trường ảo của điện toán đám mây
- Vân đề hỏng hóc hoặc mất dữ liệu

# 1.5 Mô hình tổng quát đảm bảo ATTT và an toàn HTTT
## Nguyên tắc đảm bảo an toàn thông tin, hệ thống và mạng
- Phòng vệ nhiều lớp có chiều sâu(Defence in Depth)
- Một lớp, một công cụ phòng vệ thường KHÔNG ĐẢM BẢO AN TOÀN
- Không tồn tại HTTT an toàn tuyệt đối:
  - Nếu nó an toàn tuyệt đối -> hệ thống đóng kín hoặc ít có giá trị sử dụng
  - Cần câng bằng giữa an toàn, tính hữu dụng và chi phí đảm bảo an toàn

## Các lớp phòng vệ điển hỉnh
- Lớp an ninh cơ quan/tổ chức(Plant Security)
- Lớp an ninh mạng (Network Security) 
- Lớp an ninh hệ thống (System Security)