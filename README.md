# HTML Viewer Plus

Obsidian 插件 — 在 Vault 中直接预览和嵌入 HTML / MHTML 文件。

## 功能

- **嵌入预览** — 在 Markdown 中用 `![[file.html]]` 直接渲染 HTML
- **元素定位** — `![[file.html#elementId]]` 只显示指定元素
- **自定义尺寸** — `![[file.html|400]]` 设宽度，`![[file.html|400x300]]` 设宽高
- **全屏 / 外部打开** — 嵌入视图一键全屏或用系统浏览器打开
- **缩放** — Ctrl + 滚轮缩放，可调步长
- **页内搜索** — Ctrl+F 在 HTML 内查找文本，自动跳转标签页
- **暗色主题同步** — 跟随 Obsidian 暗色模式，支持自定义暗色 CSS
- **热刷新** — HTML 文件修改后自动重新加载
- **MHTML 支持** — 直接打开 .mht / .mhtml 网页存档
- **右键菜单** — 右键点击 HTML 内容，快速复制嵌入/链接语法
- **滚动保护** — 嵌入内容需先点击才可滚动，避免误触

## 安装

### 手动安装

1. 下载 [main.js](main.js)、[manifest.json](manifest.json)、[styles.css](styles.css)
2. 在你的 Vault 中创建目录 `.obsidian/plugins/html-viewer-plus/`
3. 将三个文件复制到该目录
4. 重启 Obsidian，进入 设置 → 社区插件，启用 **HTML Viewer Plus**

### BRAT（可选）

暂未发布到 Obsidian 社区市场，可通过 [BRAT](https://github.com/TfTHacker/obsidian42-brat) 安装：

1. 安装 BRAT 插件
2. BRAT 设置 → Add Beta Plugin → 输入仓库地址 `kuaile1407/html-viewer-plus`
3. 启用插件

## 使用

### 嵌入到笔记

```markdown
![[demo.html]]              默认宽度和宽高比
![[demo.html|600]]          宽度 600px
![[demo.html|600x400]]      宽 600px × 高 400px
![[demo.html#chart]]         只显示 id="chart" 的元素
```

### 直接打开

在文件管理器中点击 HTML 文件，以独立视图打开，工具栏提供缩放、搜索、刷新、外部打开。

### 工具栏

| 按钮 | 嵌入模式 | 直接打开 |
|------|---------|---------|
| ⛶ | 全屏 | — |
| ＋ / － | — | 缩放 |
| ↺ | — | 重置缩放 |
| 🔍 | — | 搜索 |
| ↻ | — | 刷新 |
| ↗ | 外部打开 | 外部打开 |
| → | 定位到文件 | — |

### 右键菜单

在 HTML 内容上右键，显示当前元素及其祖先的 ID 列表，点击可复制嵌入语法到剪贴板。

## 设置

| 选项 | 默认值 | 说明 |
|------|-------|------|
| 默认宽度 | 100% | 嵌入区域的默认宽度 |
| 宽高比 | 4/3 | 支持 `4/3`、`16:9`、`1.33` 等格式 |
| 显示工具栏 | 开 | 嵌入视图右下角操作按钮 |
| 启用缩放 | 开 | 直接打开时的缩放功能 |
| 缩放步长 | 0.1 | 每次滚动的缩放比例 |
| 启用搜索 | 开 | 直接打开时的搜索功能 |
| 同步暗色主题 | 开 | 自动注入暗色 CSS |
| 自定义暗色 CSS | — | 追加到默认暗色样式之后 |
| 自定义背景色 | 关 | 强制设置 HTML body 背景色 |
| 热刷新 | 关 | 文件修改时自动重载 |
| MHTML 支持 | 开 | 支持 .mht/.mhtml 文件 |

## 支持的格式

- HTML: `.html` `.htm` `.shtml` `.xht` `.xhtml`
- MHTML: `.mht` `.mhtml`

## 仓库结构

```
html-viewer-plus/
├── main.js              插件入口
├── manifest.json        插件清单
├── styles.css           样式
├── assets/              赞赏二维码
├── demos/               示例 HTML 文件
├── LICENSE
└── README.md
```

## 支持作者

如果这个插件对你有帮助，欢迎请我喝杯咖啡 ☕

<img src="assets/支付宝.jpg" width="200"> <img src="assets/微信.jpg" width="200">

## License

[GPL-3.0](LICENSE)
