# 2.1. Tổng quan về lỗ hổng bảo mật và điểm yếu hệ thống
## Các thành phần của hệ thống máy tính
- Hệ thống phần cứng
  - CPU, ROM, RAM, Bus, ...
  - Các giao diện ghép nối và các thiết bị ngoại vi
- Hệ thống phền mềm
  - Hệ điều hành
    - Nhân hệ điều hành, các trình điều khiển thiết bị
    - Các trình cung cấp dịch vụ, tiện ích, ...
  - Các phần mềm ứng dụng 
    - Các dịch vụ(máy chủ web, CSDL, DNS, ...)
    - Trình duyệt web, các ứng dụng giao tiếp, ...
    - Các bộ ứng dụng văn phòng, lập trình

## Các điểm yếu hệ thống (system weaknesses) 
Là các lỗi hay các khiếm khuyết (thiết kế, cài đặt, phần cứng hoặc phần mềm) tồn tại trong hệ thống
  - Có điểm yếu đã biết và được khắc phục
  - Có điểm yếu đã biết và chưa được khắc phục
  - Có điểm yếu chưa biết/chưa được phát hiện

## Lỗ hổng bảo mật(Security vulnerability) 
Là một điểm yếu trong một hệ thống cho phép kẻ tấn cống khai thác gây tổn hại đến các thuộc tính an ninh, an toàn của hệ thống đó

- Toàn vẹn (integrity)
- Bí mật (confidentiality) 
- Sẵn dùng (availability)

### Toàn vẹn (integrity)
- Mọi sửa đổi đến thông tin/hệ thống chỉ được thực hiện bởi các bên có đủ thẩm quyền
- Kẻ tấn công có thể lợi dụng điểm yếu an ninh để lặng lẽ sửa đổi thông tin/hệ thống -> phá vỡ tính toàn vẹn

### Bí mật (confidentiality)
- Chỉ những người có thẩm được phép truy nhập đến thông tin/hệ thống
- kẻ tấn công có thể lợi dụng điểm yếu an ninh để truy nhập trái phép -> phá vỡ tính bí mật

### Sẵn dùng (available)
- Đảm bảo khả năng truy nhập đến thông tin/hệ thống cho người dùng hợp pháp
- Kẻ tấn công có thể lợi dụng điểm yếu an ninh để ngăn chặn hoặc gây khó khăn cho người dùng hợp pháp truy nhập vào thông tin/hệ thống

# 2.2. Các dạng lỗ hổng trong HDH và phần mềm ứng dụng
## Các dạng lỗ hổng bảo mật thường gặp trong hệ điều hành và các phần mềm ứng dụng
- Lỗi tràn bộ đệm (buffer overflows) 
- Không kiểm tra đầu vào (unvalidated input)
- Các vấn đề với điều khiển truy cập (access-control problems)
- Các điểm yếu trong xác thực, trao quyền hoặc các hệ mật mã (weaknesses in authentication, authorization, or cryptographic practices)
- Các lỗ hổng bảo mật khác

## 2.2.1. Các dạng lỗ hổng - lỗi tràn bộ đệm
- Lỗi tràn bộ đệm xảy ra khi một ứng dụng cố gắng ghi dữ liệu vượt khỏi phạm vi bộ đệm (giới hạn cuối hoặc cả giới hạn đầu của bộ đệm)
- Lỗi tràn bộ đệm có thể khiến ứng dụng ngừng hoạt động, gây mất dữ liệu hoặc thậm chí giúp kẻ tấn công kiểm soát hệ thống
- Lỗi tràn bộ đệm chiếm một tỷ lệ lớn cho số các lỗi gây lỗ hổng bảo mật
- Không phải tất cả các lỗi tràn bộ đệm có thể bị khai thác bởi kẻ tấn công
- Các vùng nhớ chứa bộ đệm của ứng dụng:
  - Ngăn xếp (Stack): vùng nhớ lưu các tham số gọi hàm, phương thức và dữ liệu cục bộ của chúng
    - Các biến cục bộ được cấp phát tĩnh
  - Vùng nhớ heap: là vùng nhớ chung lưu dữ liệu cho ứng dụng
    - Bộ nhớ heap thường được cấp phát động theo yêu cầu

- Các vùng nhớ chứa bộ đệm của ứng dụng:
  - Ngăn xếp (stack): 
  - Vùng nhớ heap

# 2.3. Các dạng tấn công - Tấn công bằng mã độc: Tấn công lợi dụng lỗi tràn bộ đệm
