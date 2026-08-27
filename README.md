# Hello World VS Code Extension

Extension đơn giản hiển thị thông báo "Hello World" dạng toast message trong VS Code. Dự án này được tạo để học cách xây dựng, chạy thử và publish một VS Code extension từ đầu đến cuối.

## Tổng quan

Extension đăng ký một command duy nhất (`Hello World`). Khi gọi command này qua Command Palette, một thông báo sẽ hiện ra ở góc dưới bên phải màn hình VS Code.

## Yêu cầu

- [Node.js](https://nodejs.org/) (khuyến nghị bản LTS)
- [Visual Studio Code](https://code.visualstudio.com/)
- Git (để clone repo)

## Cài đặt môi trường phát triển

Cài các công cụ cần thiết để tạo và publish extension:

```bash
npm install -g yo generator-code @vscode/vsce
```

- **yo** + **generator-code**: sinh (scaffold) project extension theo template chuẩn của VS Code
- **@vscode/vsce**: đóng gói (`.vsix`) và publish extension lên Marketplace

## Khởi tạo project (nếu tạo mới từ đầu)

```bash
yo code
```

Chọn:

- **New Extension (TypeScript)**
- Đặt tên extension, identifier, publisher theo ý bạn
- Các câu hỏi khác có thể để mặc định (Enter)

## Chạy dự án ở local

1. Clone repo về máy và cài dependencies:

```bash
git clone https://github.com/huynhducthanhtuan/helloworld-vscode-extension.git
cd helloworld-vscode-extension
npm install
```

2. Mở project bằng VS Code:

```bash
code .
```

3. Nhấn **`F5`** (hoặc menu **Run → Start Debugging**)

→ VS Code sẽ compile code và mở ra một cửa sổ mới gọi là **Extension Development Host** — đây là môi trường test, extension đã được load sẵn.

4. Trong cửa sổ **Extension Development Host** vừa mở:
   - Nhấn `Ctrl+Shift+P` (Windows/Linux) hoặc `Cmd+Shift+P` (macOS) để mở **Command Palette**
   - Gõ **"Hello World"** → chọn command
   - Toast message thông báo sẽ hiện ra

5. Nếu sửa code, quay lại cửa sổ gốc và nhấn `Ctrl+Shift+F5` để restart debug, hoặc trong Extension Host nhấn `Ctrl+R` / `Cmd+R` để reload.

### Watch mode (tùy chọn)

Nếu muốn tự động compile mỗi khi sửa code:

```bash
npm run watch
```

Để lệnh này chạy nền, sau đó chỉ cần reload cửa sổ Extension Host (`Ctrl+R`) để thấy thay đổi.

## Đóng gói & cài thử như extension thật

```bash
vsce package
code --install-extension hello-popup-0.1.0.vsix
```

## Tính năng

- Hiển thị toast message "Hello World" thông qua command `Hello World` trong Command Palette

## Known Issues

Chưa ghi nhận issue nào.

## Release Notes

### 0.1.0

Phiên bản đầu tiên — hiển thị toast message Hello World.

---
