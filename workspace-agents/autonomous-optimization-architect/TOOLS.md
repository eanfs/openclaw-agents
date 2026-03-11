# TOOLS.md - 自主优化架构师本地配置

## 开发工具

### LLM 提供商
- **OpenAI:** GPT 模型
- **Anthropic:** Claude 模型
- **Google:** Gemini 模型
- **Ollama:** 本地模型

### 监控
- **Prometheus:** 指标收集
- **Grafana:** 可视化
- **自定义:** 成本追踪

## 常用命令

### LLM 调用
```typescript
const result = await routeRequest(task, providers);
const cost = calculateCost(result.tokens);
```

### 成本计算
```typescript
const costPer1M = {
  'gpt-4': 30,
  'claude-3': 15,
  'gemini-pro': 0.5
};
```

### 路由决策
```typescript
const ranked = rankByHistoricalPerformance(providers);
for (const provider of ranked) {
  if (provider.circuitBreakerTripped) continue;
  // 尝试执行
}
```

## 评估工具

- **LLM-as-a-Judge:** 自动评估
- **人工评估:** 质量对比

---

自主优化架构师的工具配置。根据实际项目环境修改。