# OpenClaw 🦞 — Trợ lý AI trên thiết bị của bạn

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/openclaw/openclaw/main/docs/assets/openclaw-banner-light.png">
    <img src="https://raw.githubusercontent.com/openclaw/openclaw/main/docs/assets/openclaw-banner-dark.png" alt="OpenClaw - Trợ lý AI mã nguồn mở">
  </picture>
</p>

<p align="center">
  <a href="https://github.com/openclaw/openclaw/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/openclaw/openclaw/ci.yml?branch=main&style=flat-square&label=CI" alt="CI"></a>
  <a href="https://www.npmjs.com/package/openclaw"><img src="https://img.shields.io/npm/v/openclaw?style=flat-square&label=npm" alt="Phiên bản npm"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/Giấy%20phép-MIT-green?style=flat-square" alt="MIT"></a>
</p>

> **Lưu ý:** Đây là bản fork của [openclaw/openclaw](https://github.com/openclaw/openclaw), với README được biên soạn bằng tiếng Việt để dễ tiếp cận. Mã nguồn và tài liệu chính thức do cộng đồng OpenClaw phát triển. Đây không phải bản phát hành chính thức riêng.

**OpenClaw** là trợ lý AI mã nguồn mở, có thể chạy trên máy tính hoặc máy chủ của bạn. Bạn có thể trò chuyện với trợ lý qua giao diện web, dòng lệnh hoặc các nền tảng nhắn tin được hỗ trợ như Telegram, Discord, WhatsApp, Slack và nhiều kênh khác.

Trợ lý có thể sử dụng mô hình AI từ nhà cung cấp dịch vụ hoặc mô hình chạy cục bộ. Các **công cụ (tools)**, **kỹ năng (skills)** và **plugin** giúp mở rộng khả năng thực hiện tác vụ.

**Liên kết:** [Trang chủ](https://openclaw.ai) · [Tài liệu](https://docs.openclaw.ai) · [Bắt đầu](https://docs.openclaw.ai/start/getting-started) · [FAQ](https://docs.openclaw.ai/help/faq) · [Repository gốc](https://github.com/openclaw/openclaw)

## ✨ Tính năng nổi bật

- **Trò chuyện đa nền tảng:** kết nối nhiều dịch vụ nhắn tin qua một Gateway.
- **Tự động hóa:** thực hiện công việc qua các công cụ được cấp quyền.
- **Hỗ trợ lập trình:** tương tác với tệp, lệnh và quy trình phát triển phần mềm khi được cấu hình.
- **Linh hoạt về mô hình:** kết nối nhà cung cấp AI hoặc mô hình cục bộ phù hợp.
- **Tự quản lý dữ liệu:** cấu hình, trạng thái và bộ nhớ của trợ lý được quản lý trên thiết bị hoặc máy chủ bạn vận hành.
- **Mở rộng:** cài thêm skills, plugins và các tích hợp cộng đồng.

> Phần mềm mã nguồn mở, nhưng API của nhà cung cấp mô hình AI hoặc dịch vụ tích hợp có thể phát sinh chi phí.

## 📦 Cài đặt

Trình cài đặt chính thức hỗ trợ **Windows, macOS và Linux**; có thể chuẩn bị môi trường Node.js phù hợp khi cần.

### Windows (PowerShell)

Mở PowerShell và chạy:

```powershell
iwr -useb https://openclaw.ai/install.ps1 | iex
```

### macOS / Linux / WSL2

Mở Terminal:

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

> **Bảo mật:** Các lệnh trên tải và chạy tập lệnh từ Internet. Hãy xem xét nội dung script và chỉ sử dụng nguồn chính thức trước khi chạy.

### Cài bằng npm

Nếu đã có môi trường Node.js phù hợp (theo README gốc: **Node.js 24.22.1+ hoặc 26.12.1+**, khuyến nghị Node 26), có thể dùng:

```bash
npm install -g openclaw@latest --allow-scripts=openclaw
```

Tùy phiên bản npm, cờ `--allow-scripts=openclaw` có thể không được hỗ trợ. Đối với npm 11.15 trở xuống, bỏ cờ này. Xem thêm [hướng dẫn cài đặt](https://docs.openclaw.ai/install).

## 🚀 Thiết lập và chạy lần đầu

Trình cài đặt có thể tự khởi động phần cấu hình ban đầu. Nếu bạn cài trực tiếp bằng npm/pnpm/Bun, chạy:

```bash
openclaw onboard --install-daemon
```

Làm theo hướng dẫn để cấu hình mô hình AI, quyền truy cập và Gateway.

Kiểm tra trạng thái:

```bash
openclaw gateway status
```

Mở giao diện quản lý:

```bash
openclaw dashboard
```

Sau đó gửi thử một tin nhắn trong giao diện web để xác nhận trợ lý hoạt động.

## 🧩 OpenClaw hoạt động như thế nào?

| Thành phần | Chức năng |
| --- | --- |
| **Gateway** | Quản lý phiên làm việc, công cụ, sự kiện và kết nối các kênh |
| **Control UI** | Giao diện web để tương tác và quản lý |
| **CLI / TUI** | Sử dụng OpenClaw qua dòng lệnh |
| **Channels** | Kết nối các nền tảng nhắn tin |
| **Models** | Cung cấp khả năng AI qua nhà cung cấp hoặc mô hình cục bộ |
| **Tools / Skills / Plugins** | Mở rộng chức năng và khả năng tự động hóa |

## 💻 Chạy từ mã nguồn của bản fork này

Dành cho người muốn tìm hiểu hoặc chỉnh sửa mã nguồn, không bắt buộc nếu chỉ muốn dùng OpenClaw.

Cần có **Git**, môi trường Node.js phù hợp và **pnpm**.

```bash
git clone https://github.com/nguyentuankiet210666/openclaw.git
cd openclaw
pnpm install
pnpm build
pnpm ui:build
```

Repository sử dụng **pnpm workspace**, vì vậy **không dùng `npm install` ở thư mục gốc**. Xem [hướng dẫn phát triển](https://docs.openclaw.ai/start/setup) và [CONTRIBUTING.md](CONTRIBUTING.md) nếu muốn đóng góp.

## 🔐 Bảo mật và quyền riêng tư

OpenClaw có thể thực hiện các hành động thực tế nếu bạn cấp công cụ và quyền phù hợp. Vì vậy:

1. **Không chia sẻ API key, token hay mật khẩu** lên GitHub hoặc trong tin nhắn.
2. **Chỉ kết nối tài khoản và công cụ cần thiết**; áp dụng nguyên tắc cấp quyền tối thiểu.
3. **Không mở Gateway công khai ra Internet** nếu chưa cấu hình xác thực và bảo vệ thích hợp.
4. **Sử dụng sandbox** với công cụ hoặc phiên làm việc không đáng tin cậy.
5. **Cẩn trọng với tin nhắn đầu vào** từ người lạ; xác nhận các yêu cầu ghép nối thiết bị/kênh trước khi cho phép.

Lệnh phê duyệt ghép nối kênh (khi cần):

```bash
openclaw pairing approve <channel> <code>
```

Tìm hiểu thêm: [Bảo mật](https://docs.openclaw.ai/gateway/security) · [Sandbox](https://docs.openclaw.ai/gateway/sandboxing) · [Hướng dẫn xử lý rủi ro khi phơi lộ Gateway](https://docs.openclaw.ai/gateway/security/exposure-runbook).

## 📚 Tài liệu tham khảo

| Nội dung | Liên kết |
| --- | --- |
| Cấu hình và mô hình AI | [Models](https://docs.openclaw.ai/concepts/models) |
| Nhà cung cấp AI | [Model providers](https://docs.openclaw.ai/concepts/model-providers) |
| Telegram, Discord và các kênh khác | [Channels](https://docs.openclaw.ai/channels) |
| Công cụ, kỹ năng | [Tools](https://docs.openclaw.ai/tools) · [Skills](https://docs.openclaw.ai/tools/skills) |
| Plugin | [Plugins](https://docs.openclaw.ai/plugins) |
| Lệnh CLI | [CLI](https://docs.openclaw.ai/cli) |
| Cập nhật | [Updating](https://docs.openclaw.ai/install/updating) |
| Câu hỏi thường gặp | [FAQ](https://docs.openclaw.ai/help/faq) |

## 🤝 Đóng góp và cộng đồng

OpenClaw được cộng đồng phát triển công khai dưới sự quản lý của [OpenClaw Foundation](https://openclaw.org).

- [Repository chính thức](https://github.com/openclaw/openclaw)
- [Báo lỗi hoặc đề xuất tính năng](https://github.com/openclaw/openclaw/issues/new/choose)
- [Cộng đồng hỗ trợ](https://community.openclaw.ai/)
- [Hướng dẫn đóng góp](CONTRIBUTING.md)
- [Báo cáo lỗ hổng bảo mật](SECURITY.md)

## 📄 Giấy phép

Dự án được phát hành theo giấy phép **MIT**. Xem chi tiết tại [LICENSE](LICENSE).

---

**README tiếng Việt cho bản fork:** [nguyentuankiet210666/openclaw](https://github.com/nguyentuankiet210666/openclaw)  
**Nguồn chính thức:** [openclaw/openclaw](https://github.com/openclaw/openclaw)
