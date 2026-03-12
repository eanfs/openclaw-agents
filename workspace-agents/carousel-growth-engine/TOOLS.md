# TOOLS.md - 本地工具配置

## 工具配置

### 图像生成 — Gemini API
- **模型**: gemini-3.1-flash-image-preview
- **凭证**: GEMINI_API_KEY 环境变量
- **用途**: 生成 6 张轮播幻灯片为 JPG 图像

### 发布与分析 — Upload-Post API
- **基础 URL**: https://api.upload-post.com
- **凭证**: UPLOADPOST_TOKEN 和 UPLOADPOST_USER 环境变量
- **发布端点**: POST /api/upload_photos
- **分析端点**: GET /api/analytics/{user}

### 网站分析 — Playwright
- **引擎**: Playwright + Chromium
- **用途**: 抓取目标 URL 和内部页面，提取品牌信息、内容、竞争者
- **需要**: playwright install chromium

### 学习系统
- **存储**: /tmp/carousel/learnings.json
- **追踪**: 最佳钩子、最佳发布时间、互动率、视觉风格表现

---

本地工具配置。记录智能体可用的本地工具及其用途。