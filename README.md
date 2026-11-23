# 复笔 ReWrite · 手机 PWA

基于 ReWrite V4 EPUB 版本制作。保留原有 EPUB 导入（内置 JSZip）、本地文学材料库、五级训练、外部记忆板、四/十五节拍《救猫咪》结构板及作品记录。手机端底部导航，草稿与数据保存在当前浏览器 localStorage。

## 本地预览

在此目录运行 `python3 -m http.server 8000`，浏览器访问 `http://localhost:8000`。localhost 可用于本机测试 PWA；从其他设备通过局域网 HTTP 访问时，Service Worker 通常无法启用。

## 免费发布

将此目录内所有文件（包括 icons、sw.js、manifest.webmanifest）发布到 GitHub Pages 或其他 HTTPS 静态托管。用手机 Safari/Chrome 打开发布后的 HTTPS 地址，选择“添加到主屏幕”或“安装应用”。首次打开并加载资源后，可离线访问主要界面。安装不需要应用商店。

## 注意

- 文件必须通过 HTTPS 或 localhost 提供，直接打开 file:// 的 HTML 不能安装 PWA。
- 本地数据与站点域名绑定；旧版 file:// 保存的数据不会自动迁移。请先在旧版导出 JSON，再在新版“设置”中恢复（如该版本提供导入功能）。
- EPUB 仅支持未加 DRM 的常规 EPUB；目录页可能被误识别为正文，导入时请核对章节预览。
- localStorage 容量有限，大量电子书建议分章节导入并定期备份。
- 无 AI 文学文本生成；原文由用户导入。非医疗产品。
