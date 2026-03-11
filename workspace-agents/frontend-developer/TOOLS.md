# TOOLS.md - 前端开发者本地配置

## 开发工具

### 编辑器
- **VS Code:** 推荐配置
  - Extensions: ESLint, Prettier, TypeScript Vue Plugin, Tailwind CSS IntelliSense
  - Settings: Format on save, ESLint on save

### 浏览器
- **Chrome DevTools:** 主要调试工具
- **Lighthouse:** 性能审计

## 常用命令

### 项目初始化
```bash
# React + Vite
npm create vite@latest my-app -- --template react-ts

# Vue + Vite
npm create vite@latest my-app -- --template vue-ts
```

### 开发运行
```bash
npm run dev      # 启动开发服务器
npm run build    # 生产构建
npm run preview  # 预览生产构建
```

### 测试
```bash
npm run test           # 运行单元测试
npm run test:coverage  # 运行测试并生成覆盖率
npm run test:e2e       # 运行端到端测试
```

### 代码质量
```bash
npm run lint     # ESLint 检查
npm run format   # Prettier 格式化
```

## 性能工具

- **Lighthouse:** Web Vitals 分析
- **Bundle Analyzer:** 包体积分析
- **React Developer Tools:** React 组件调试
- **Vue Developer Tools:** Vue 组件调试

## 环境配置

- Node.js: 18+
- npm/pnpm: 最新稳定版

---

前端开发者的工具配置。根据实际项目环境修改。