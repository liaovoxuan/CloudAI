# CloudAI

CloudAI là một trợ lý AI đa nền tảng.

> **Trạng thái phiên bản 1.0.1:** Chế độ Agent hỗ trợ tác vụ nhiều bước và các gói ứng dụng mặc định sử dụng định dạng ZIP. Các gói 1.0.0 trước đây được lưu trong [kho phiên bản cũ](../Releases/Legacy/v1.0.0/). Xem [chế độ Agent](../docs/AGENT_MODE.md) và [các giới hạn của HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Phiên bản 1.0.1 sử dụng bản dựng Universal cho cả Intel và Apple Silicon, trong khi gói 1.0.0 đã lưu trữ chỉ hỗ trợ Apple Silicon (`arm64`).

## Tính năng

-   Trò chuyện với AI
-   Chế độ Agent cho tác vụ nhiều bước
-   Tích hợp API Cloud AI
-   Ứng dụng máy tính để bàn đa nền tảng
-   Bản dựng cho nhiều kiến trúc
-   Giao diện đồ họa
-   Hỗ trợ nhiều ngôn ngữ

## Chế độ Agent

Chế độ Agent có thể chia mục tiêu thành nhiều bước, sử dụng các công cụ do người dùng bật, thực hiện những thay đổi được cho phép và xác minh kết quả khi có thể. Chế độ này không tự cấp thêm quyền và phải yêu cầu xác nhận trước các hành động nhạy cảm hoặc có tính phá hủy. Xem [hướng dẫn chế độ Agent](../docs/AGENT_MODE.md).

## Nền tảng được hỗ trợ

### Máy tính để bàn

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Các nền tảng khác

-   HarmonyOS
-   OpenHarmony

## Chi tiết nền tảng

| Nền tảng | Kiến trúc và trạng thái gói | Cài đặt và giới hạn |
| --- | --- | --- |
| Windows | Phiên bản 1.0.1 nhắm đến x64 và ARM64, mặc định sử dụng ZIP. Kho lưu trữ giữ tệp ZIP 1.0.0 cũ cho x64. | Giải nén hoàn toàn ZIP trước khi chạy. |
| Linux | Phiên bản 1.0.1 nhắm đến x86_64 và ARM64, mặc định sử dụng ZIP. Các gói 1.0.0 cho cả hai kiến trúc đã được lưu trữ. | ZIP có thể chứa AppImage, DEB, RPM hoặc TAR.GZ. AppImage cần quyền thực thi; DEB và RPM được cài bằng trình quản lý gói. |
| macOS | Phiên bản 1.0.1 dùng bản dựng Universal cho Intel và Apple Silicon, mặc định phân phối dưới dạng ZIP; 1.0.0 chỉ hỗ trợ Apple Silicon (`arm64`). | Giải nén ZIP để lấy ứng dụng. Ứng dụng chưa được ký và có thể cần được cho phép thủ công trong macOS. |
| HarmonyOS | Bản phân phối 1.0.1 mặc định dùng ZIP; hãy cài HAP tương thích và đã ký ở bên trong. Các HAP 1.0.0 đã lưu trữ là bản dựng debug chỉ dành cho `2in1`. | HAP cũ nhắm đến API `60101024`. Cần hệ thống tương thích và chữ ký hợp lệ. Xem [ghi chú HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | Bản phân phối 1.0.1 mặc định dùng ZIP; việc cài đặt cần HAP tương thích OpenHarmony ở bên trong. | Cần chữ ký tương thích và thử nghiệm thiết bị. Không dùng HAP HarmonyOS 1.0.0 đã lưu trữ làm gói OpenHarmony. |

## Cài đặt

### Linux

AppImage:

1.  Tải xuống và giải nén gói ZIP mặc định cho Linux, sau đó chọn AppImage phù hợp với kiến trúc của bạn.
2.  Thêm quyền thực thi:

``` bash
chmod +x CloudAI.AppImage
```

3.  Chạy ứng dụng:

``` bash
./CloudAI.AppImage
```

Có thể cài đặt gói .deb bằng:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Phiên bản macOS hiện chưa được ký bằng chứng chỉ Apple Developer.

Khi mở lần đầu, người dùng có thể cần cho phép ứng dụng thủ công trong cài đặt bảo mật của macOS.

### HarmonyOS

Phiên bản HarmonyOS được xây dựng bằng bộ công cụ phát triển chính thức của HarmonyOS.

Quá trình phát triển và đóng gói sử dụng DevEco Studio. Ứng dụng HarmonyOS được đóng gói dưới dạng HAP/App và cần cấu hình chữ ký phù hợp trước khi phân phối.

## Giấy phép

[Giấy phép MIT](../LICENSE).

## Tệp dự án nguồn mở

Xem [thông tin dự án nguồn mở](../docs/OPEN_SOURCE.md) để biết giấy phép, trạng thái cung cấp mã nguồn, hướng dẫn đóng góp và các chính sách của dự án.

Bản sao cây mã nguồn CloudAI 1.0.1 hiện có tại [`Source/CloudAI`](../Source/CloudAI/) và bao gồm ứng dụng máy tính, hỗ trợ Agent và phần bổ trợ, tài nguyên đóng gói cùng dự án HarmonyOS. Dự án HAP riêng cho OpenHarmony, ánh xạ bản phát hành với mã nguồn, phiên bản phần phụ thuộc được khóa và quy trình đóng gói có thể tái tạo đã được xác minh vẫn chưa được cung cấp; xem [bản đánh giá trạng thái nguồn mở](../docs/OPEN_SOURCE_STATUS.md).

## Nhà phát triển

Liao Boxuan

## Ngày

2026-09-13
