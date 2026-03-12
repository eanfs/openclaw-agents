# 本地工具配置

## 截图捕获工具

### Playwright截图捕获
- **工具**: qa-playwright-capture.sh
- **用途**: 专业级可视化证据捕获
- **用法**: `./qa-playwright-capture.sh <URL> <output-dir>`
- **支持**: 多设备（桌面、平板、移动端）、暗色模式、交互测试

### Playwright手动截图
- **工具**: Playwright截图API
- **配置**: 自定义视口和设备

## 文件检查工具

### 命令行工具
- **ls**: 检查实际构建的文件结构
- **grep**: 搜索代码中的功能实现
- **cat**: 读取测试结果文件

## 测试结果文件

### 标准输出
- **test-results.json**: 包含设备兼容性、暗色模式、交互、完整页面捕获的综合数据
- **截图文件**:
  - responsive-desktop.png (1920x1080)
  - responsive-tablet.png (768x1024)
  - responsive-mobile.png (375x667)
  - dark-mode-*.png
  - *-before.png, *-after.png

## 报告生成工具

### Markdown报告
- **工具**: 标准Markdown
- **模板**: 内置报告模板

### 截图注释工具
- **工具**: 图像编辑工具（如Photoshop、GIMP）
- **用途**: 在截图中标注问题

## 环境要求

### 开发服务器
- **本地服务器**: http://localhost:8000（或其他配置的端口）
- **截图输出目录**: public/qa-screenshots/

### 浏览器支持
- Chrome
- Firefox
- Safari
- Edge

## 配置参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| BASE_URL | 测试目标URL | http://localhost:8000 |
| OUTPUT_DIR | 截图输出目录 | public/qa-screenshots |
| DEVICES | 测试设备列表 | desktop, tablet, mobile |
| THEME_MODES | 测试主题模式 | light, dark |
| VIEWPORTS | 自定义视口 | - |
| WAIT_FOR_TIMEOUT | 元素等待超时 | 30000ms |
| FULL_PAGE | 完整页面截图 | true |