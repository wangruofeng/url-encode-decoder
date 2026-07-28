# URL / HTML 实体 / Unicode 转义 / Base64 编解码工具

一个纯前端的单文件编解码工具，双击 `index.html` 即可使用，无需安装、无需后端、无任何外部依赖。

## 功能特性

- 🔗 **URL 编码 / 解码**：支持 `encodeURIComponent` 与 `encodeURI` 两种模式切换。
- 🧾 **HTML 实体**：字符与命名实体（`&amp;`）、十进制 / 十六进制数字实体（`&#x4E2D;`）双向转换。
- 🔤 **Unicode 转义**：中文 ↔ `中文`，兼容辅助平面字符（Emoji 等）。
- 🔢 **Base64**：文本与 Base64 双向转换，UTF-8 安全（使用 `TextEncoder` / `TextDecoder`）。
- 📋 **实时转换**：输入即转换，150ms 防抖；一键复制结果、交换输入输出、清空。
- 🔍 **URL 拆解卡**：当输入像 URL 时自动显示协议、host、端口、path、query 参数表格，每个参数 key/value 均可单独复制。
- 🎨 深浅色主题切换、自适应移动端。

## 使用方式

直接用浏览器打开 `index.html` 即可：

```bash
open index.html        # macOS
# 或拖入浏览器
```

点击「示例」可快速体验当前转换类型的效果。

## 技术说明

- 单一 HTML 文件，原生 HTML / CSS / JavaScript，零依赖、零构建步骤。
- 所有编解码运算均在浏览器本地完成，不上传任何数据。

## 在线访问

已通过 GitHub Pages 部署，可直接访问：

🔗 **https://blog.wangruofeng007.com/url-encode-decoder/**

源码仓库：https://github.com/wangruofeng/url-encode-decoder
