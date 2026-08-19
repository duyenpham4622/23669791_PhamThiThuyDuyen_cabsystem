
b1: xacs ddinh bussiness contact nguwx canh nghiepj vuj

business problem

mucj ddichs laf gif

gias trij cuaj ht nayf taoj ra so voiws ht cux

Xác định các stalkhoder?
Lập bảng 
c1: những stalkhoder 
c2 vai trò 
vẽ ma trận stakhoder () mức đọ ảnh  hưởng cảu các vai trò trong hệ thống
3.
bs goals :bg01: hỗ trợ thanh toán (= tiền mặt ....)
bg02: giảm time tìm tài xế(tìm tài tự động, gần nhất
4.
scope_Phạm vi
(ql đc khách hang, quản lý tài xế,...) 
không thuộc trong scope(Dung ai tìm dương ngắn nhất, xử lý nhu cầu kh,...) phải deal vs kh
5. Xác nhận lại với kh chuyển đổi thành business requirements
6. business process -quy trình nghiệp vụ dùng công cụ mermaid trong markdown
7. Functional Requirement 
- 
1. Business Context – Ngữ cảnh nghiệp vụ
   ABC là doanh nghiệp cung cấp dịch vụ đặt xe trực tuyến, trong đó có 3 nhóm người dùng chính:

      Customer – người có nhu cầu đặt xe.
      Driver – tài xế cung cấp dịch vụ vận chuyển.
      Operation Staff – nhân viên vận hành/quản trị hệ thống.
      
   Ngoài ra, hệ thống còn tương tác với các hệ thống bên ngoài:
      
      Payment Provider – nhà cung cấp thanh toán điện tử.
      Notification Provider – SMS/Email/Push Notification.
      Có thể có Map/Location Service để hỗ trợ vị trí, khoảng cách, ETA.
      Các hệ thống báo cáo/BI trong tương lai.

   Ngữ cảnh hiện tại: hệ thống cũ còn phụ thuộc nhiều vào tổng đài và thao tác thủ công, đặc biệt trong việc phân công tài xế, theo dõi chuyến và quản lý thanh toán.
   
                         
   2. Business Problem – Vấn đề kinh doanh
      Hệ thống đặt xe hiện tại phụ thuộc nhiều vào thao tác thủ công và chưa có khả năng quản lý tập trung toàn bộ vòng đời chuyến xe, dẫn đến hiệu quả điều phối thấp, trải nghiệm khách hàng hạn chế, khó kiểm soát thanh toán và dữ liệu vận hành, đồng thời làm giảm khả năng mở rộng dịch vụ của ABC.
      Hệ thống cũ có 6 vấn đề đang hiện hành:
        Phân công tài xế thủ công: Chậm xử lý booking, tăng chi phí vận hành
        Khó theo dõi trạng thái chuyến: Khách hàng thiếu thông tin, tăng cuộc gọi đến tổng đài
        Quản lý thanh toán chưa tập trung: Khó kiểm soát doanh thu và giao dịch
        Dữ liệu khách hàng/tài xế/chuyến đi phân tán: Khó quản lý và báo cáo
        Hệ thống khó mở rộng: Khó đáp ứng khi số lượng booking tăng
        Phụ thuộc vào một hệ thống/luồng xử lý: Một lỗi có thể ảnh hưởng toàn bộ dịch vụ

   3. Mục đích – Business Purpose
      Xây dựng một nền tảng CAB tập trung nhằm tự động hóa quy trình đặt và điều phối xe, nâng cao trải nghiệm khách hàng, tăng hiệu quả vận hành và tạo nền tảng công nghệ có khả năng mở rộng cho các dịch vụ vận tải trong tương lai.
   # 4. Giá trị của CAB System so với hệ thống cũ

| **Khía cạnh** | **Hệ thống cũ** | **CAB System mới** | **Giá trị tạo ra** |
|---|---|---|---|
| **Đặt xe** | Đặt qua tổng đài hoặc ứng dụng đơn giản | Đặt xe trực tiếp trên nền tảng | Số hóa và đơn giản hóa quy trình đặt xe |
| **Phân công tài xế** | Chủ yếu thực hiện thủ công | Tự động tìm và phân công tài xế phù hợp | Giảm thời gian và chi phí vận hành |
| **Tìm tài xế** | Khó xác định tài xế phù hợp/gần khách | Dựa trên vị trí, trạng thái và tiêu chí vận hành | Tăng hiệu quả điều phối |
| **Tài xế từ chối/không phản hồi** | Có thể phải xử lý thủ công lại | Tự động chuyển sang tài xế tiếp theo | Giảm thời gian chờ, hạn chế mất booking |
| **Theo dõi chuyến đi** | Khách hàng ít thông tin về trạng thái | Theo dõi trạng thái và ETA của chuyến | Tăng tính minh bạch và trải nghiệm khách hàng |
| **Vị trí tài xế** | Chưa được khai thác hiệu quả | Cập nhật và lưu thông tin vị trí | Hỗ trợ tìm tài xế và dự kiến thời gian đến |
| **Quản lý chuyến đi** | Thông tin phân tán, khó tra cứu | Quản lý tập trung toàn bộ vòng đời chuyến | Dễ kiểm soát và xử lý sự cố |
| **Tính cước** | Chưa được quản lý tập trung | Tự động tính cước theo loại dịch vụ và thông tin chuyến | Giảm sai sót, tăng tính nhất quán |
| **Thanh toán** | Chưa tập trung | Hỗ trợ tiền mặt và thanh toán điện tử | Quản lý giao dịch và doanh thu tốt hơn |
| **Xử lý thanh toán lỗi** | Khó kiểm soát và đối soát | Có trạng thái giao dịch và cơ chế xử lý lại | Giảm rủi ro thất thoát doanh thu |
| **Thông báo** | Hạn chế | Thông báo theo từng sự kiện của chuyến | Cải thiện trải nghiệm khách hàng và tài xế |
| **Dữ liệu** | Phân tán | Tập trung dữ liệu khách hàng, tài xế, xe, chuyến, thanh toán | Dễ tra cứu, đối soát và phân tích |
| **Quản lý vận hành** | Phụ thuộc nhiều vào thao tác thủ công | Có hệ thống quản trị riêng | Tăng năng suất nhân viên vận hành |
| **Báo cáo** | Khó tổng hợp | Dashboard và báo cáo về chuyến, doanh thu, hủy, hiệu quả tài xế | Hỗ trợ ra quyết định dựa trên dữ liệu |
| **Bảo mật** | Khả năng kiểm soát hạn chế | Authentication, Authorization và Audit Log | Tăng mức độ an toàn và khả năng kiểm tra |
| **Khả năng mở rộng** | Khó đáp ứng khi số lượng khách/tài xế tăng | Có khả năng scale các thành phần độc lập | Hỗ trợ tăng trưởng kinh doanh |
| **Khả năng tích hợp** | Khó tích hợp thêm dịch vụ | Có thể tích hợp Payment, Map, Notification Provider | Dễ mở rộng hệ sinh thái |
| **Khả năng thay đổi** | Thay đổi một chức năng có thể ảnh hưởng hệ thống | Kiến trúc modular, giảm coupling | Giảm chi phí và rủi ro phát triển tương lai |
| **Xử lý sự cố** | Một lỗi có thể ảnh hưởng nhiều chức năng | Có khả năng cô lập các thành phần như Payment/Notification | Tăng tính ổn định và khả năng phục hồi |
| **Phát triển sản phẩm mới** | Khó bổ sung dịch vụ mới | Có nền tảng để thêm loại xe/dịch vụ/phương thức thanh toán | Tạo nền tảng cho phát triển dài hạn |

## Tóm tắt giá trị

### Hệ thống cũ

> Đặt xe → Xử lý thủ công → Khó theo dõi → Dữ liệu phân tán → Khó mở rộng

### CAB System mới

> Đặt xe → Tự động tìm tài xế → Theo dõi chuyến → Tính cước → Thanh toán → Đánh giá → Báo cáo

### Giá trị kinh doanh kỳ vọng

- Giảm chi phí vận hành.
- Tăng năng lực phục vụ khách hàng.
- Nâng cao trải nghiệm khách hàng.
- Tăng hiệu quả điều phối tài xế.
- Tăng khả năng kiểm soát và phân tích dữ liệu.
- Tăng tính ổn định và khả năng mở rộng.
- Tạo nền tảng để phát triển thêm dịch vụ trong tương lai.
      
