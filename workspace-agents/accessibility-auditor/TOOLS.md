# 本地工具配置

## 自动化测试工具

### axe-core
- **用途**: 自动可访问性扫描
- **安装**: `npm install @axe-core/cli`
- **用法**: `npx @axe-core/cli <URL> --tags wcag2a,wcag2aa,wcag22aa`

### Lighthouse
- **用途**: 可访问性审计
- **安装**: `npm install lighthouse`
- **用法**: `npx lighthouse <URL> --only-categories=accessibility --output=json`

### WAVE
- **用途**: Web可访问性评估
- **类型**: 浏览器扩展（Chrome/Firefox）
- **网站**: webaim.org/resources/wave

## 屏幕阅读器

### VoiceOver
- **平台**: macOS/iOS
- **用途**: macOS和iOS上的屏幕阅读器测试
- **快捷键**: Cmd + F5 启动/停止

### NVDA
- **平台**: Windows
- **用途**: Windows上的屏幕阅读器测试
- **下载**: nvaccess.org

### JAWS
- **平台**: Windows
- **用途**: 专业屏幕阅读器测试

## 键盘导航测试

### 测试清单
- [ ] 所有交互元素可通过Tab到达
- [ ] Tab顺序遵循视觉布局逻辑
- [ ] 跳过导航链接存在且可用
- [ ] 无键盘陷阱（始终可以Tab离开）
- [ ] 每个交互元素上焦点指示器可见
- [ ] Escape关闭模态、下拉菜单和覆盖层

## 浏览器开发工具

### Chrome开发者工具
- **Accessibility Tree**: 审查可访问性树
- **Tab键测试**: 模拟键盘导航

### Firefox开发者工具
- **检查器**: 审查可访问性属性
- **无障碍面板**: 查看可访问性信息

## 颜色对比度工具

### WebAIM对比度检查器
- **用途**: 验证颜色对比度是否满足WCAG
- **网址**: webaim.org/resources/contrastchecker

### Coolors
- **用途**: 创建可访问的颜色调色板

## ARIA工具

### A11y Checklist
- **用途**: ARIA最佳实践检查
- **参考**: w3.org/WAI/ARIA/apg/practices

### ARIA Authoring Practices
- **用途**: ARIA模式参考
- **网址**: w3.org/WAI/ARIA/apg

## 报告工具

### markdown-accessible-tables
- **用途**: 生成可访问的表格测试报告

### axe-sarif
- **用途**: 将axe结果导出为SARIF格式

## 测试环境

### 本地服务器
- **URL**: http://localhost:8000
- **要求**: 支持多种浏览器

### 浏览器列表
- Chrome (最新版本)
- Firefox (最新版本)
- Safari (最新版本)
- Edge (最新版本)

## 配置参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| TARGET_URL | 测试目标URL | http://localhost:8000 |
| WCAG_LEVEL | WCAG合规级别 | AA |
| WCAG_VERSION | WCAG版本 | 2.2 |
| SCREEN_READERS | 测试的屏幕阅读器 | VoiceOver, NVDA |
| ZOOM_LEVELS | 测试的缩放级别 | 100%, 200%, 400% |