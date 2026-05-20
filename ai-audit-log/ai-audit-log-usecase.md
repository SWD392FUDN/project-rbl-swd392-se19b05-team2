1. Use Case là gì? (Definition)
Khái niệm: Use Case (Ca sử dụng) là một chuỗi các hành động hoặc tương tác giữa một hoặc nhiều Actor (Tác nhân - người dùng hoặc hệ thống khác) với hệ thống phần mềm nhằm đạt được một mục tiêu cụ thể.

Mục đích: Giúp team phát triển và khách hàng có chung một góc nhìn về tính năng hệ thống mà không bị sa đà vào code.

Thành phần chính: Actor, Pre-condition (Điều kiện tiên quyết), Post-condition (Kết quả sau khi thực hiện), Main Flow (Luồng xử lý chính), và Alternative/Exception Flow (Luồng rẽ nhánh/Xử lý lỗi).

--------------------------------------------------------
2. Cách sử dụng Use Case trong thiết kế hệ thống
Bước 1: Xác định Actor & Boundary: Ai sẽ xài hệ thống? Giới hạn của hệ thống tới đâu?

Bước 2: Liệt kê các Use Case chính: (Ví dụ cho JobVN: Đăng tuyển dụng, Tìm kiếm việc làm, Nộp CV, Duyệt hồ sơ).

Bước 3: Vẽ Use Case Diagram: Thể hiện mối quan hệ giữa các Actor và Use Case (<<include>> cho tính năng bắt buộc phải chạy qua, <<extend>> cho tính năng mở rộng tùy chọn).

Bước 4: Viết Use Case Specification (Mô tả chi tiết): Viết rõ từng bước User bấm gì, Hệ thống phản hồi gì.

--------------------------------------------------
3. Một số lỗi phổ biến khi dùng Use Case & Thao tác Git
Khi làm việc nhóm môn SWD, các bạn rất dễ dính các lỗi logic thiết kế hoặc lỗi xung đột khi đẩy code/tài liệu lên Git:

Lỗi Thiết kế (Use Case Errors):

Sai mức độ chi tiết (Granularity): Gom quá nhiều tính năng vào một Use Case (Ví dụ: "Quản lý hệ thống" là quá rộng, cần tách nhỏ ra thành Quản lý User, Quản lý Bài đăng).

Nhầm lẫn giữa <<include>> và <<extend>>: Ép buộc hệ thống phải chạy một tính năng tùy chọn (Sai include) hoặc ngược lại.

Viết Use Case theo góc nhìn giao diện (UI-driven): Mô tả chi tiết kiểu "User bấm nút màu xanh", "User cuộn chuột". Use Case phải tập trung vào mục tiêu và business logic, không phải UI.

Lỗi khi Git lên Repository (Git/Workflow Errors):

Conflict nặng do sửa chung một file Use Case/Markdown: Nhiều thành viên cùng edit file tài liệu mà không kéo git pull mới nhất về.

Commit cả file rác hoặc thư mục cấu hình cá nhân: Quên cấu hình .gitignore dẫn đến đẩy cả code thừa (node_modules, .env) lên cùng file tài liệu.

Commit Message không rõ ràng: Ghi chung chung kiểu "fix bug", "update" khiến giảng viên hoặc Leader chấm Audit Log không biết bạn đã làm tính năng hay Use Case nào.