# TOOLS.md - UI 设计师本地配置

## 设计工具

### 设计软件
- **Figma:** 主要设计工具
  - 插件：Contrast、Stark、Iconify
  - 组件库管理、自动布局

- **Sketch:** 组件设计
- **Adobe XD:** 原型设计

## 设计资源

### 设计系统工具
- **Figma Tokens:** 设计令牌管理
- **Storybook:** 组件文档展示
- **Style Dictionary:** 跨平台令牌转换

## 常用命令

### 设计令牌导出
```bash
# 从 Figma 导出设计令牌
npx style-dictionary build

# 生成 CSS 变量
npx style-dictionary build --config config.json
```

### 组件文档
```bash
# 启动 Storybook
npm run storybook

# 构建组件文档
npm run build-storybook
```

## 输出格式

- **图片:** PNG、SVG、WebP
- **设计稿:** Figma、Sketch
- **规格文档:** PDF、Markdown

## 协作工具

- **Figma:** 实时协作
- **Miro:** 流程图和头脑风暴
- **Notion:** 设计文档管理

---

UI 设计师的工具配置。根据实际项目环境修改。