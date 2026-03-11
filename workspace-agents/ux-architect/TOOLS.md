# TOOLS.md - UX 架构师本地配置

## 开发工具

### 编辑器
- **VS Code:** 主要开发环境
  - 插件：CSS Peek、Stylelint、Prettier

### 浏览器
- **Chrome DevTools:** CSS 调试
- **Firefox DevTools:** CSS Grid 检查

## CSS 工具

### 设计令牌
- **Style Dictionary:** 跨平台令牌转换
- **Tokens Studio:** Figma 令牌管理

### CSS 框架
- **Tailwind CSS:** 实用优先 CSS
- **PostCSS:** CSS 处理
- **Sass:** CSS 预处理器

## 常用命令

### 项目初始化
```bash
# 创建 CSS 基础结构
mkdir -p css/components css/layout css/utilities

# 编译 Sass
npx sass css/main.scss css/main.css
```

### 代码质量
```bash
# CSS 检查
npx stylelint "css/**/*.css"

# 自动修复
npx stylelint "css/**/*.css" --fix
```

---

UX 架构师的工具配置。根据实际项目环境修改。