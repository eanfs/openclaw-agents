# 本地工具配置

## 测试工具

### Playwright 截图捕获
- **工具**: qa-playwright-capture.sh
- **用途**: 专业级视觉证据捕获
- **配置**: 支持多设备（桌面、平板、移动端）截图

### 命令行工具
- **ls**: 检查实际构建的文件结构
- **grep**: 搜索代码中的功能实现
- **cat**: 读取测试结果文件

## 自动化测试

### 测试结果分析
- **test-results.json**: 包含设备兼容性、暗色模式、交互、完整页面捕获的综合数据
- **截图文件**: responsive-*.png, dark-mode-*.png, *-before.png, *-after.png

## 环境要求

### 开发服务器
- **本地服务器**: http://localhost:8000（或其他配置的端口）
- **截图输出目录**: public/qa-screenshots/

## 报告生成

### 证据存储
- 截图目录: public/qa-screenshots/
- 测试结果: public/qa-screenshots/test-results.json
- 报告格式: Markdown

## 配置参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| BASE_URL | 测试目标URL | http://localhost:8000 |
| OUTPUT_DIR | 截图输出目录 | public/qa-screenshots |
| DEVICES | 测试设备列表 | desktop, tablet, mobile |