# CCPTPM_FinalProject

Nhóm 03 : Dự án Ekomart - Website bán thực phẩm

## Thông tin thành viên nhóm 03:

- Lê Huỳnh Như Nguyệt - 22110385
- Phạm Ngọc Hòa - 22110330
- Trần Trọng Nghĩa - 22110380
- Huỳnh Quốc Thắng - 22110423
- Lê Văn Tú - 22110454

## Giới thiệu về Ekomart

### Mục đích

Website là môi trường trung gian kết nối người bán và người tiêu dùng

- Đối với người tiêu dùng:
  Mang lại một môi trường mua sắm dễ dàng, thân thiện và dễ tiếp cận với mọi người trong đời sống hiện đại.
  Tiết kiệm thời gian trong việc mua sắm
- Đối với nhà bán hàng, doanh nghiệp:
  Nhà bán hàng, nhãn hàng có thể dễ dàng đăng ký, quản lý sản phẩm và tiếp cận nhiều khách hàng hơn mà không cần đầu tư quá nhiều vào hạ tầng công nghệ.
  Giúp các nhãn hàng mở rộng thị trường, tạo ra một môi trường cạnh tranh lành mạnh, đảm bảo chất lượng sản phẩm và dịch vụ

## Hướng dẫn setup và build project

### 1. Cơ chế vận hành trong Ekomart

Ekomart gồm có 3 role: USER, VENDOR, ADMIN.

- USER: là khách hàng để mua hàng. USER có quyền đăng ký để mở shop, đăng ký thành công tài khoản của USER sẽ vừa là khách vừa là nhà bán hàng.

- VENDOR: là chủ cửa hàng/nhà bán hàng.

  - _Tạo/mở bán/ngừng bán_ sản phẩm
  - _Quản lý/cập nhật trạng thái_ đơn hàng do USER mua

- ADMIN: là quản trị hệ thống.
  - _Quản lý_ tài khoản người dùng
  - _Duyệt_ USER đăng ký mở SHOP
  - _Duyệt/quản lý_ tất cả sản phẩm do VENDOR thêm vào SHOP đó
  - _Tạo/quản lý_ phân loại(Category) của sản phẩm

### 2. Chuẩn bị công cụ

- IntelliJ IDEA : dùng để chạy mã nguồn Java, Spring Boot,...
- MySQL - MySQL Workbench : Hỗ trợ lưu trữ, quản lý cơ sở dữ liệu của dự án
- Github và TortoiseGit : nhằm kiểm soát mã nguồn chặt chẽ, đảm bảo tính toàn vẹn của dự án, hỗ trợ theo dõi lịch sử thay đổi rõ ràng, đồng thời tối ưu hóa quy trình làm việc nhóm
- Docker : Đóng gói ứng dụng backend/frontend, triển khai & chạy nhất quán giữa các máy
- Postman : dùng để kiểm thử API

### 3. Tiến hành setup

- **Bước 1:** Tạo 1 thư mục trên máy -> clone đường dẫn git của dự án vào thư mục vừa tạo

- **Bước 2:** Tại ổ D trên máy, tạo 1 thư mục có tên: **_upload_** (bước này dùng để load được ảnh)

- **Bước 3:** Vào MySQL Workbench:

  - 3.1: Tạo 1 DB tên: **_ekomart_**
  - 3.2: Vào tab Server -> Data Import -> Chọn "Import from Dump Project Folder" -> Chọn thư mục **_db-web_** trong thư mục ở bước 1 -> Bấm "Start Import"

- **Bước 4:** Vào IntelliJ IDEA:

  - 4.1: File -> Open -> mở thư mục **_demo_** trong thư mục "ekomart" của thư mục ở bước 1
  - 4.2: Vào file **_application.yaml_** chỉnh sửa phần **username** và **password** của phần cấu hình **datasource** tại dòng số 13 và 14 
    `username: máy của bạn `
    `password: máy của bạn`

  - 4.3: Tiến hành **RUN** project trên đường dẫn: [http://localhost:8888](http://localhost:8888/login)
  - 4.4: Sau khi chạy được project, tiến hành tạo **branch** của bạn theo cú pháp : _"dev\_" + tên của bạn_ sau đó merge code từ nhánh main về

  * **LƯU Ý:**
    - Các account trong project đều có password là: "123"
    - Một số chức năng trong project còn bị lỗi chưa fix. Ví dụ: cần phải chọn tích chọn sản phẩm trong giỏ hàng trước khi bấm "Pay" nếu không sẽ nhảy lỗi.

### 4. Thông tin liên hệ

Liên hệ cho Lê Huỳnh Như Nguyệt thông qua group Zalo nếu gặp bất cứ trục trặc nào trong quá trình chạy project
