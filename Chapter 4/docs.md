# 4.1. Khái quát về mã hóa thông tin và ứng dụng
## 4.1.1. Định nghĩa và quy trình cơ bản
Mã hóa (Cryptography) được định nghĩa là hành động hoặc nghệ thuật viết các ký tự bí mật, hoặc việc biến đổi dữ liệu sao cho chỉ những người được chỉ định mới có thể giải mã được.

Một hệ mã hóa cơ bản luôn bao gồm hai quá trình đối nghịch: 
- mã hóa (encryption)
- giải mã (decryption)

## 4.1.2. Các thuật nghữ then chốt
- **Bản rõ (Plaintext/Cleartext)**: Thông tin ở dạng có thể hiểu được
- **Bản mã (Ciphertext)**: thông tin sau khi đã bị xáo trộn
- **Giải thuật (Algorithm)**: quy trình toán học được sử dụng để mã hóa thông tin
- **Khóa (key)**: Một chuỗi ký tự kết hợp với giải thuật để thực hiện mã hóa và giải mã
- **Không gian khóa (Keyspace)**: Tập hợp tất cả các khóa có thể có của một hệ mã hóa; không gian khóa càng lớn thì hệ thống càng an toàn

## 4.1.3. Vai trò của mã hóa trong An toàn thông tin (ATTT)
Mã hóa không chỉ đơn thuần là giữu bí mật mà còn đảm bảo bốn thuộc tính quan trọng của thông tin:
- **Tính bí mật (Confidentiality)**: Đảm bảo chỉ người có thẩm quyền mới truy cập được thông tin
- **Tính toàn vẹn (Integrity)**: Đảm bảo dữ liệu không bị sửa đổi trái phép
- **Xác thực (Authentication)**: Xác minh danh tính của các bên tham gia truyền thông
- **Chống chối bỏ (Non-repudiation)**: Ngăn chặn việc một bên phủ nhận hành vi hoặc phát ngôn đã thực hiện

## 4.1.4. Phân loại các phương pháp mã hóa
Dựa trên cách thức sử dụng khóa và xử lý dữ liệu, mã hóa được chia thành các loại chính:
- **Mã hóa khóa đối xứng (Symmetric key)**: Sử dụng một khóa duy nhất cho cả mã hóa và giải mã. Đặc điểm là tốc độ nhanh, kích thước khóa ngắn nhưng khó khăn trong việc quản lý và phân phối khóa khi số lượng người dùng lớn.  `VD`: DES vs AES
- **Mã hóa khóa bất đối xứng(Asymmetric key)**: Sử dụng một cặp khóa gồm khóa công khai (để mã hóa) và khóa bí mật (để giải mã). Phương pháp này thuận lợi trong việc trao đổi khóa nhưng tốc độ chậm hơn do kích thước khóa lớn. `VD`: RSA
- **Hàm băm (Hash function)**: Là ánh xạ chuyển dữ liẹu có kích thước bất kỳ thành một chuỗi có độ dài cố định. Nó chủ yếu được dùng để kiểm tra tính toàn vẹn và nhận dạng thông điệp
- **Mã hóa dòng và mã hóa khối**: Mã hóa dòng(Stream cipher) xử lý từng bit hoặc ký tự dữ liệu, trong khi mã hóa khối (Block cipher) chia dữ liệu thành các khối có kích thước cố định để xử lý

# 4.2. Phương pháp mã hóa 
## 4.2.1. Phương pháp thay thế (Substitution)
- Định nghĩa: Thay thế một giá trị(ký tự hoặc bit) này bằng một giá trị khác
- Phân loại:
  - Sử dụng một bỗ chữ mã: Dễ bị đoán do sự lặp lại
  - Sử dụng nhiều bộ chữ mã (n bộ): Khó đoán hơn vì tính phức tạp cao

## 4.2.2. Phương pháp đổi chỗ/hoán vị (Permutation)
- Định nghĩa: Sắp xếp lại thứ tự các giá trị trong một khối dữ liệu để tạo bản mã mà không thay đổi bản thân các giá trị đó
- Phạm vi: Có thể thực hiện trên từng bit hoặc từng byte(kí tự)
- Cơ chế: thường thực hiện đổi chỗ trong các khối có kích thước cố định (ví dụ khối 8 phần tử) theo một khóa quy định sẵn

## 4.2.3. Phương pháp XOR
- Cơ chế: Sử dụng phép XOR giữa từng bit của bản rõ vơi sbit tương ứng của khóa mã
- Đặc điểm: Đây là phép toán nền tảng trong nhiều thuật toán mã hóa hiện đại nhớ tính đơn giản và hiệu quả 

## 4.2.4. Phương pháp vernam
- Cơ chế: Sử dụng 1 tập ký tự (khóa) để nối vào các ký tự của bản rõ
- Đặc điểm then chốt: mỗi ký tự trong tập khóa chỉ được sử dụng duy nhất một lần trong một tiến tình mã hóa 
- Cách tính: thực hiện cộng giá trị ký tự bản rõ với giá trị khóa theo kiểu lấy modulo 

## 4.2.5. Phương pháp Sách hoặc khóa chạy
- Cơ chế: Sử dụng các từ nghữ trong 1 cuốn sách cụ thể làm khóa để mã hóa và giải mã

## 4.2.6. Phương pháp hàm băm (Hash function)
- Định nghĩa: là thuật toán ánh xạ thông điệp có chiều dài bất kỳ thành một bản tóm lược có độ dài nhất định

# 4.3. Giải thuật mã hóa đối xứng
## 4.3.1. Nguyên lý cơ bản 
- Định nghĩa: Là phương pháp mã hóa mà người gửi và người nhận sử dụng chung một khóa duy nhất cho cả 2 quá trình mã hóa và giải mã
- Kích thước khóa: Thường tưởng đối ngắn, phổ biến ở các mức 64, 128, 256 bits

## 4.3.2. Đặc điểm hệ thống
- Ưu điểm: 
  - Tốc độ xử lý nhanh và hiệu quả nâng cao
  - Độ an toàn cao nếu khóa được bảo vệ tốt
- Nhược điểm: 
  - Khó khăn trong quản lý khóa: Khi số lượng người dùng (N) tăng lên, số lượng khóa cần quản lý tăng rất nhanh theo công thức N * (N - 1) / 2
  - Trao đổi khóa: Gặp thách thức trong việc chia sẻ khóa an toàn giữa các bên trên môi trường mạng.
  - Không đáp ứng tốt các yêu cầu về xác thực và chống chối bỏ

## 4.3.3. Các giải thuật tiêu biểu
- DES (Data Encryption Standard):
  -  Ra đời từ những năm 1970, là mã hóa khối với kích thước khối 64 bít,.
  - Sử dụng khóa 64 bít nhưng thực tế chỉ có 56 bít có hiệu lực bảo mật.
  - Hiện nay không còn an toàn do không gian khóa nhỏ và tốc độ tính toán của máy tính hiện đại đã quá nhanh.
- Triple-DES (3-DES):
  - Là bản cải tiến bằng cách áp dụng giải thuật DES 3 lần trên mỗi khối dữ liệu để tăng cường độ bảo mật.
  - Có thể sử dụng bộ 2 khóa hoặc 3 khóa độc lập.
- AES (Advanced Encryption Standard):
  - Là chuẩn mã hóa hiện đại (từ năm 2001) thay thế cho DES,.
  - Xử lý khối dữ liệu 128 bít, vận hành trên ma trận 4x4,.
  - Hỗ trợ 3 mức khóa: 128 bít (10 vòng lặp), 192 bít (12 vòng lặp) và 256 bít (14 vòng lặp),.
- Các giải thuật khác: IDEA, Blowfish, Twofish, RC4, RC5.

## 4.3.4. Chế độ hoạt động của mã hóa khối
Để xử lý các luồng dữ liệu dài, các giải thuật mã hóa khối thường hoạt động theo các chế độ:
- ECB: Các khối được mã hóa hoàn toàn độc lập
- CBC: Khối mã hiện tại phụ thuộc vào khối rõ hiện tại và khối mã trước đó
- CFB vs OFB: Các chế độ phản hồi để xử lý dữ liệu

# 4.4. Giải thuật mã hóa bất đối xứng
## 4.4.1. Nguyên lý và thành phần
- Định nghĩa: Còn được gọi là mã hóa khóa công khai (Public key cryptography), sử dụng một cặp khóa khác nhau cho quá trình mã hóa và giải mã.
- Cặp khóa (Key pair):
  - Khóa công khai (Public key): Dùng để mã hóa, có thể công bố rộng rãi và trao đổi dễ dàng
  - Khóa riêng/bí mật (Private key): Đùng để giải mã, phải được giữ bí mật tuyệt đối

## 4.4.2. Đặc điểm hệ thống
- Kích thước khóa: Rất lớn, thường từ 1024 đến 3072 bit
- Tốc độ xử lý: chậm
- Ưu điểm:
  - Quản lý khóa thuận lợi: Không cần thiết lập khóa bí mật trước với từng người dùng, dễ dàng mở rộng cho số lượng người dùng lớn.
  - Hỗ trợ tốt các dịch vụ an toàn như chữ ký số và xác thực.
- Độ an toàn: Rất cao, dựa trên các bài toán toán học khó (như phân tích số nguyên lớn).


## 4.4.3. Các giải thuật tiêu biểu
- RSA (Rivest, Shamir, Adleman):
  - Ra đời năm 1977, là giải thuật phổ biến nhất 
  - Độ an toàn dựa trên tính khó của việc phân tích số nguyên rất lớn thành các thừa số nguyên tố.
  - Được ứng dụng cho cả mã hóa thông tin và tạo chữ ký số
- DSA (Digital Signature Algorithm):
  - Được NIST công nhận là chuẩn chữ ký số năm 1991
  - Phát triển dựa trên giải thuật chữ ký ElGamal
- Các giải thuật khác: ElGamal, Rabin, McEliece, Knapsack

## 4.4.4. Ứng dụng chính
- phối khóa bí mật: Sử dụng mã hóa bất đối xứng để chuyển khóa phiên (khóa đối xứng) một cách an toàn trên môi trường không tin cậy.
- Chữ ký số và Chứng chỉ số: Đảm bảo tính xác thực, tính toàn vẹn của dữ liệu và chống chối bỏ.
- Hạ tầng khóa công khai (PKI): Nền tảng quản lý chứng chỉ số cho các hệ thống an toàn như HTTPS (SSL/TLS)


# 4.5. Hàm băm (Hash Functions)
## 4.5.1. Định nghĩa và đặc điểm chính
Hàm băm là một thuật toán toán học thực hiện ánh xạ từ một thông điệp có chiều dài bất kỳ thành một chuỗi dữ liệu (bản tóm lược - digest) có chiều dài cố định,. Một hàm băm tiêu chuẩn cần có hai thuộc tính cơ bản:

- Tính nén (Compression): Chuyển đầu vào x bất kỳ sang đầu ra h(x) có độ dài n bit cố định
- Dễ tính toán (Ease of computation): Việc tính toán giá trị băm từ thông điệp đầu vào phải thực hiện 1 cách dễ dàng và nhanh chóng

## 4.5.2. Các tính chất an toàn quan trọng 
Để phục vụ mục đích bảo mật, hàm băm thường cần đáp ứng các tính chất:
- Tính một chiều (One-way): Việc tính toán giá trị băm là đơn giản, nhưng việc giải mã ngược từ giá trị băm để tìm lại thông điệp gốc là cực kỳ phức tạp hoặc không khả thi về mặt tính toán,.
- Tính chống đụng độ (Collision resistance): Rất khó để tìm thấy hai thông điệp khác nhau mà khi băm lại cho ra cùng một giá trị kết quả.

## 4.5.3. Phân loại hàm băm 
Dựa vào cách thức vận hành và tính năng, hàm băm được chia làm hai loại chính:
- Hàm băm không khóa (Unkeyed hash): Đầu vào chỉ bao gồm thông điệp, thường được gọi là Mã phát hiện sửa đổi (MDC) nhằm đảm bảo tính toàn vẹn của dữ liệu.
- Hàm băm có khóa (Keyed hash): Đầu vào bao gồm thông điệp và một khóa bí mật, thường được gọi là Mã xác thực thông điệp (MAC), dùng để đảm bảo cả tính toàn vẹn và tính xác thực mà không cần thêm biện pháp bổ sung