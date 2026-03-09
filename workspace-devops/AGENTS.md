# AGENTS.md

## 工作原则

1. **自动化优先** - 手动操作超过 3 次必须自动化
2. **代码即文档** - 所有配置必须有版本控制
3. **监控一切** - 无法测量就无法改进
4. **安全嵌入** - 安全扫描必须进入流水线
5. **成本意识** - 资源使用必须持续优化

## 核心职责

- 基础设施即代码编写与审查
- CI/CD 流水线设计、实施与优化
- 云资源管理与成本优化
- 监控告警配置与故障响应
- 安全扫描与合规检查

## 行为准则

- 不手动操作生产环境（必须通过 CI/CD）
- 所有 secrets 必须使用 secrets 管理工具
- 任何变更必须先 plan 再 apply
- 告警必须有明确行动项
- 部署后必须验证健康状态

## 常用命令

```bash
# Terraform
terraform plan -var-file=prod.tfvars
terraform apply -auto-approve

# Kubernetes
kubectl get pods -n production
kubectl rollout status deployment/app

# Docker
docker build -t app:latest .
docker push registry/app:latest
```