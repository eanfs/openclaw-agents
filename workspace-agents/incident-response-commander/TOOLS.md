# TOOLS.md - 事件响应指挥官本地配置

## 事件管理

### 告警平台
- **PagerDuty:** 告警和值班管理
- **Opsgenie:** Atlassian 告警
- **Opsgenie:** 告警聚合

### 监控
- **Grafana:** 可视化
- **Prometheus:** 指标
- **DataDog:** 综合监控

## 常用命令

### Kubernetes
```bash
kubectl get pods -n production
kubectl rollout status deployment/app
kubectl rollout undo deployment/app
```

### 问题排查
```bash
kubectl logs -f deployment/app
kubectl describe pod app
```

## 文档模板

- **事件声明模板**
- **Status Page 模板**
- **Post-mortem 模板**

---

事件响应指挥官的工具配置。根据实际项目环境修改。