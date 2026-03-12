# 本地工具配置

## 测试框架

### Playwright
- **用途**: 功能测试和端到端API测试
- **配置**: TypeScript/JavaScript
- **安装**: `npm install @playwright/test`

### REST Assured
- **用途**: Java API测试
- **配置**: Maven/Gradle依赖
- **特性**: 简洁的BDD语法

### k6
- **用途**: 负载和性能测试
- **配置**: JavaScript脚本
- **安装**: `brew install k6` 或 `npm install k6`

## 安全测试工具

### OWASP ZAP
- **用途**: 动态应用安全测试
- **配置**: API扫描模式
- **集成**: CI/CD管道集成

### SQLMap
- **用途**: SQL注入测试
- **配置**: 命令行工具

## 性能测试工具

### Lighthouse
- **用途**: Web性能审计
- **配置**: CLI或Playwright集成

### JMeter
- **用途**: 负载和压力测试
- **配置**: GUI或CLI模式

## 环境配置

### 测试环境变量
```bash
export API_BASE_URL=http://localhost:3000
export API_AUTH_TOKEN=your_token_here
export TEST_DATA_PATH=./test-data
```

### 配置文件
```json
{
  "baseUrl": "http://localhost:3000",
  "timeout": 30000,
  "retries": 3,
  "parallel": 10
}
```

## 报告工具

### Allure
- **用途**: 测试报告生成
- **集成**: TestNG, JUnit, Playwright

### k6 HTML导出
- **用途**: 性能测试结果可视化

## CI/CD集成

### 质量门槛配置
```yaml
quality_gates:
  functional_coverage: 95
  security_scan: pass
  performance_sla:
    p95_response_time: 200
    error_rate: 0.001
```

## 配置参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| API_BASE_URL | API基础URL | http://localhost:3000 |
| API_AUTH_TOKEN | 认证令牌 | - |
| TIMEOUT | 请求超时(ms) | 30000 |
| RETRY_COUNT | 重试次数 | 3 |
| PARALLEL_WORKERS | 并行工作数 | 10 |
| PERFORMANCE_SLA_P95 | P95响应时间SLA | 200ms |