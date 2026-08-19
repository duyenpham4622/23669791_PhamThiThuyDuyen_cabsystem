
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
8. business rule và Exception
# 1. Business Context – Ngữ cảnh nghiệp vụ
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
   
                         
   # 1.2. Business Problem – Vấn đề kinh doanh
      Hệ thống đặt xe hiện tại phụ thuộc nhiều vào thao tác thủ công và chưa có khả năng quản lý tập trung toàn bộ vòng đời chuyến xe, dẫn đến hiệu quả điều phối thấp, trải nghiệm khách hàng hạn chế, khó kiểm soát thanh toán và dữ liệu vận hành, đồng thời làm giảm khả năng mở rộng dịch vụ của ABC.
      Hệ thống cũ có 6 vấn đề đang hiện hành:
        Phân công tài xế thủ công: Chậm xử lý booking, tăng chi phí vận hành
        Khó theo dõi trạng thái chuyến: Khách hàng thiếu thông tin, tăng cuộc gọi đến tổng đài
        Quản lý thanh toán chưa tập trung: Khó kiểm soát doanh thu và giao dịch
        Dữ liệu khách hàng/tài xế/chuyến đi phân tán: Khó quản lý và báo cáo
        Hệ thống khó mở rộng: Khó đáp ứng khi số lượng booking tăng
        Phụ thuộc vào một hệ thống/luồng xử lý: Một lỗi có thể ảnh hưởng toàn bộ dịch vụ

   # 1.3. Mục đích – Business Purpose
      Xây dựng một nền tảng CAB tập trung nhằm tự động hóa quy trình đặt và điều phối xe, nâng cao trải nghiệm khách hàng, tăng hiệu quả vận hành và tạo nền tảng công nghệ có khả năng mở rộng cho các dịch vụ vận tải trong tương lai.
   # 1.4. Giá trị của CAB System so với hệ thống cũ

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
  
# 2. Stakeholders

| **C1: Stakeholder** | **C2: Vai trò** |
|---|---|
| **Ban giám đốc / Business Owner** | Định hướng kinh doanh, phê duyệt ngân sách, xác định mục tiêu và đánh giá hiệu quả dự án |
| **Khách hàng (Customer)** | Đăng ký, đặt xe, theo dõi chuyến, thanh toán, xem lịch sử và đánh giá tài xế |
| **Tài xế (Driver)** | Nhận/từ chối chuyến, cập nhật trạng thái chuyến, cập nhật vị trí và thông tin phương tiện |
| **Nhân viên vận hành (Operation Staff)** | Quản lý khách hàng, tài xế, phương tiện, theo dõi chuyến và xử lý các trường hợp bất thường |
| **Quản trị hệ thống (System Admin)** | Quản lý tài khoản, phân quyền, cấu hình và bảo mật hệ thống |
| **Bộ phận chăm sóc khách hàng (CS)** | Tiếp nhận và xử lý yêu cầu, khiếu nại, hỗ trợ khách hàng trong quá trình sử dụng dịch vụ |
| **Bộ phận tài chính / kế toán** | Theo dõi thanh toán, đối soát giao dịch, doanh thu và báo cáo tài chính |
| **Business Analyst (BA)** | Thu thập, phân tích, làm rõ và quản lý yêu cầu nghiệp vụ |
| **Project Manager (PM)** | Quản lý phạm vi, tiến độ, nguồn lực, rủi ro và phối hợp các bên |
| **Development Team** | Phân tích kỹ thuật, thiết kế và phát triển hệ thống CAB |
| **QA / Tester** | Kiểm thử chức năng, nghiệp vụ, hiệu năng và đảm bảo chất lượng hệ thống |
| **DevOps / Infrastructure** | Triển khai, vận hành, giám sát và đảm bảo khả năng mở rộng hệ thống |
| **Payment Provider** | Cung cấp dịch vụ thanh toán điện tử và xử lý giao dịch thanh toán |
| **Notification Provider** | Cung cấp dịch vụ gửi Push Notification, SMS, Email hoặc các kênh thông báo khác |
| **Map/GPS Provider** | Cung cấp dữ liệu bản đồ, vị trí, khoảng cách và hỗ trợ tính ETA |
| **Cơ quan quản lý / Pháp lý** | Đảm bảo hệ thống tuân thủ các quy định về vận tải, thanh toán và bảo vệ dữ liệu |

# 2.1. Ma trận Stakeholder – Mức độ ảnh hưởng

| **Stakeholder** | **Mức độ ảnh hưởng** | **Mức độ quan tâm** | **Chiến lược quản lý** |
|---|---|---|---|
| **Ban giám đốc / Business Owner** | 🔴 Cao | 🔴 Cao | **Manage Closely** – Tham gia quyết định, cập nhật thường xuyên |
| **Nhân viên vận hành (Operation)** | 🔴 Cao | 🔴 Cao | **Manage Closely** – Tham gia sâu vào phân tích nghiệp vụ |
| **Khách hàng (Customer)** | 🟠 Trung bình | 🔴 Cao | **Keep Informed** – Thu thập feedback và kiểm tra trải nghiệm |
| **Tài xế (Driver)** | 🟠 Trung bình | 🔴 Cao | **Keep Informed** – Thu thập nhu cầu và phản hồi |
| **System Admin** | 🔴 Cao | 🟠 Trung bình | **Keep Satisfied** – Đảm bảo quyền quản trị và bảo mật |
| **Bộ phận Tài chính / Kế toán** | 🟠 Trung bình | 🟠 Trung bình | **Keep Satisfied** – Đảm bảo yêu cầu thanh toán, đối soát |
| **Bộ phận CS** | 🟠 Trung bình | 🔴 Cao | **Keep Informed** – Đảm bảo chức năng hỗ trợ khách hàng |
| **Business Analyst (BA)** | 🔴 Cao | 🔴 Cao | **Manage Closely** – Phân tích và quản lý yêu cầu |
| **Project Manager (PM)** | 🔴 Cao | 🔴 Cao | **Manage Closely** – Quản lý tiến độ, phạm vi và rủi ro |
| **Development Team** | 🟠 Trung bình | 🔴 Cao | **Keep Informed / Collaborate** |
| **QA / Tester** | 🟢 Thấp – Trung bình | 🔴 Cao | **Keep Informed** – Đảm bảo chất lượng và nghiệp vụ |
| **DevOps / Infrastructure** | 🔴 Cao | 🟠 Trung bình – Cao | **Keep Satisfied / Collaborate** |
| **Payment Provider** | 🟠 Trung bình | 🟠 Trung bình | **Keep Satisfied** – Quản lý tích hợp và giao dịch |
| **Notification Provider** | 🟢 Thấp – Trung bình | 🟠 Trung bình | **Monitor / Keep Satisfied** |
| **Map/GPS Provider** | 🟠 Trung bình | 🟠 Trung bình | **Keep Satisfied** – Đảm bảo dữ liệu vị trí và ETA |
| **Cơ quan quản lý / Pháp lý** | 🔴 Cao | 🟠 Trung bình | **Keep Satisfied** – Đảm bảo tuân thủ pháp luật |

## Ma trận Power – Interest
  # 3. Ma trận Stakeholder – Power / Interest

| **Mức độ ảnh hưởng / Mức độ quan tâm** | **Thấp** | **Cao** |
|---|---|---|
| **Cao** | **KEEP SATISFIED** 🟠<br><br>• System Admin<br>• Tài chính / Kế toán<br>• DevOps / Infrastructure<br>• Payment Provider<br>• Map/GPS Provider<br>• Cơ quan quản lý / Pháp lý | **MANAGE CLOSELY** 🔴<br><br>• Ban giám đốc / Business Owner<br>• Nhân viên vận hành<br>• Business Analyst (BA)<br>• Project Manager (PM)<br>• Khách hàng<br>• Tài xế<br>• Development Team |
| **Thấp** | **MONITOR** 🟢<br><br>• Notification Provider | **KEEP INFORMED** 🟡<br><br>• Bộ phận CS<br>• QA / Tester |

## Sơ đồ ma trận

```text
                    MỨC ĐỘ QUAN TÂM
                  THẤP              CAO
                    │                 │
        ┌───────────┼─────────────────┐
        │           │                 │
        │  KEEP     │   MANAGE        │
 CAO    │ SATISFIED │   CLOSELY       │
        │           │                 │
        │  System   │   Ban giám đốc  │
        │  Admin    │   Operation     │
        │  Finance  │   BA            │
        │  DevOps   │   PM            │
        │  Payment  │   Customer      │
        │  Map/GPS  │   Driver        │
        │  Pháp lý  │   Development   │
        │           │                 │
        ├───────────┼─────────────────┤
        │           │                 │
        │  MONITOR  │   KEEP          │
THẤP   │           │   INFORMED      │
        │           │                 │
        │  Notify   │   CS            │
        │  Provider │   QA / Tester   │
        │           │                 │
        └───────────┴─────────────────┘
                    │                 │
                  THẤP              CAO
                    MỨC ĐỘ QUAN TÂM

