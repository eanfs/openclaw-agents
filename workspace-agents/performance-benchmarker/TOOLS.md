# 本地工具配置

## 负载测试工具

### k6
- **用途**: 负载和性能测试
- **安装**: `brew install k6` 或 `npm install k6`
- **特性**: 现代负载测试框架，支持JavaScript脚本

### Apache JMeter
- **用途**: 负载和压力测试
- **安装**: 从jmeter.apache.org下载
- **特性**: 功能全面的负载测试工具

### Locust
- **用途**: 负载测试
- **安装**: `pip install locust`
- **特性**: Python编写，支持分布式

## 性能监控工具

### Lighthouse
- **用途**: Web性能审计
- **安装**: `npm install lighthouse`
- **用法**: `npx lighthouse <URL> --only-categories=performance`

### Chrome开发者工具
- **用途**: 性能分析和Core Web Vitals
- **特性**: Performance面板、Network面板、Lighthouse

### WebPageTest
- **用途**: 高级Web性能测试
- **网站**: webpagetest.org
- **特性**: 真实浏览器测试详细分析

## 真实用户监控 (RUM)

### Google Analytics
- **用途**: 用户性能数据收集
- **指标**: Core Web Vitals、页面加载时间

### Datadog RUM
- **用途**: 实时用户监控
- **特性**: 会话重放、性能监控

### New Relic
- **用途**: 应用性能监控
- **特性**: 完整的APM解决方案

## 数据库性能工具

### pgAdmin / MySQL Workbench
- **用途**: 数据库查询分析和优化

### APM工具
- **Datadog**: 综合APM
- **New Relic**: 应用性能监控
- **Elastic APM**: 开源APM

## 前端性能工具

### Webpack Bundle Analyzer
- **用途**: JavaScript包大小分析

### Source Map Explorer
- **用途**: 分析源代码映射

### PurgeCSS
- **用途**: 移除未使用的CSS

## 监控和告警

### Prometheus + Grafana
- **用途**: 指标收集和可视化
- **安装**: Docker Compose

### DataDog
- **用途**: 云监控平台

## 环境配置

### 测试脚本示例 (k6)
```javascript
export const options = {
  stages: [
    { duration: '2m', target: 10 },
    { duration: '5m', target: 50 },
    { duration: '2m', target: 100 },
  ],
  thresholds: {
    http_req_duration: ['p(95)<500'],
    http_req_failed: ['rate<0.01'],
  },
};
```

### 环境变量
```bash
export BASE_URL=http://localhost:3000
export PERFORMANCE_SLA_P95=500
export LOAD_TEST_VUS=100
```

## 配置参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| BASE_URL | 测试目标URL | http://localhost:3000 |
| PERFORMANCE_SLA_P95 | P95响应时间SLA | 500ms |
| LOAD_TEST_DURATION | 负载测试持续时间 | 5m |
| STAGE_TARGETS | 各阶段目标用户数 | 10,50,100 |
| ERROR_RATE_THRESHOLD | 错误率阈值 | 0.01 |
| CORE_WEB_VITALS_LCP | LCP目标 | 2.5s |
| CORE_WEB_VITALS_FID | FID目标 | 100ms |
| CORE_WEB_VITALS_CLS | CLS目标 | 0.1 |