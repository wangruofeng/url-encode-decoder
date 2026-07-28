# url-encode-decoder — 项目约定（给 AI 协作时参考）

纯前端、单文件的 URL / HTML 实体 / Unicode 转义 / Base64 编解码工具。面向人类的说明见 `README.md`；本文件记录**改代码时必须知道的红线与约定**。项目与同级目录 `../json-viewer` 保持同一套设计与代码风格。

## 红线（不要破坏）

- **单文件、零构建、零依赖**：全部 HTML / CSS / JS 都在 `index.html` 一个文件里。**禁止**引入打包器（Vite/Webpack 等）、框架（React/Vue 等）、npm 依赖或构建步骤。新增能力用原生 JS 实现。
- **纯前端、无后端**：所有编解码运算在浏览器本地完成，不上传任何数据。
- 主题用根元素 `html.dark` 类切换，配色全部走 `:root` / `html.dark` 里的 CSS 变量。新增颜色请复用已有变量，不要硬编码。localStorage key 为 `ued-theme`。

## 文件结构

- `index.html` — 全部代码（结构 + 样式 + 脚本）。
- `favicon.svg` — 站点图标。
- `.github/workflows/deploy.yml` — GitHub Pages 部署：仓库根即站点根，push 到 `main` 自动部署。
- `README.md` — 面向用户的功能说明与在线访问地址。

## UI 约定

- **按钮文案保持极简**：每个按钮都带 SVG 图标，图标已承担表意，文字尽量短（如「示例」「复制结果」「交换」「清空」）。改按钮时沿用这个风格，不要写长句子。
- 页头右侧两个图标按钮：GitHub 源码链接（仓库 `https://github.com/wangruofeng/url-encode-decoder`，新标签页打开）、深浅色主题切换。

## 在线地址

已部署到 GitHub Pages：https://blog.wangruofeng007.com/url-encode-decoder/
