# Sliver (Reforged Edition)

> ⚠️ **TUYÊN BỐ MIỄN TRỪ TRÁCH NHIỆM QUAN TRỌNG** ⚠️
>
> Đây là một phiên bản **fork đã được sửa đổi sâu** của framework Sliver C2 gốc của Bishop Fox. Mã nguồn trong kho chứa này đã được thay đổi đáng kể bằng các kịch bản tự động để lẩn tránh các phương pháp phát hiện dựa trên chữ ký.
>
> **KHÔNG** sử dụng kho chứa này nếu bạn đang tìm kiếm phiên bản Sliver chính thức. Để có phiên bản gốc, vui lòng truy cập: [https://github.com/BishopFox/sliver](https://github.com/BishopFox/sliver).
>
> Các thay đổi trong kho chứa này có thể gây ra lỗi không lường trước được. Hãy tự chịu rủi ro khi sử dụng.

## Giới thiệu

Sliver là một framework mã nguồn mở đa nền tảng được sử dụng để giả lập đối thủ và thử nghiệm thâm nhập. Phiên bản này dựa trên Sliver gốc nhưng đã được làm cứng để cải thiện khả năng lẩn tránh.

## Hướng dẫn Build cho phiên bản Fork này

Quy trình build cho phiên bản này khác với phiên bản gốc. Bạn phải chạy kịch bản "reforging" trước khi biên dịch.

1.  **Cài đặt các phụ thuộc:**
    ```bash
    # (Tương tự như hướng dẫn gốc: go, make, git, mingw-w64)
    ```

2.  **Clone kho chứa này:**
    ```bash
    git clone [URL của kho chứa fork của bạn]
    cd [tên thư mục]
    ```

3.  **Tái tạo mã Protobuf và dọn dẹp module:**
    ```bash
    make pb
    go mod tidy
    ```

4.  **Biên dịch Sliver:**
    ```bash
    make
    ```

## Tóm tắt các sửa đổi

Phiên bản này đã được tự động sửa đổi để:
*   Thay đổi đường dẫn module gốc từ `github.com/bishopfox/sliver` thành `github.com/papcaii/slisli`.
*   Đổi tên các message, trường, và tệp `.proto` nhạy cảm để vô hiệu hóa các quy tắc YARA.
*   Xóa các DLL export không cần thiết và đổi tên hàm vào chính.
*   Làm cứng logic mã nguồn để phá vỡ các mẫu phát hiện dựa trên mã lệnh.
*   Và nhiều thay đổi nhỏ khác...

---
*(Phần còn lại của README gốc)*
---

## Dự án Gốc

Kho chứa này là một phiên bản fork và đã được sửa đổi. Dự án Sliver gốc được duy trì bởi Bishop Fox tại:
*   **Kho chứa GitHub:** [https://github.com/BishopFox/sliver](https://github.com/BishopFox/sliver)
*   **Tài liệu chính thức:** [https://sliver.sh/](https://sliver.sh/)
