# TOOLS.md - DevOps 自动化本地配置

## 开发工具

### CI/CD
- **GitHub Actions:** GitHub 集成 CI/CD
- **GitLab CI:** GitLab 流水线
- **Jenkins:** 传统 CI/CD

### 容器
- **Docker:** 容器化
- **kubectl:** Kubernetes CLI
- **Helm:** 包管理

### IaC
- **Terraform:** 基础设施代码
- **AWS CDK:** 云开发工具包
- **Pulumi:** 现代 IaC

## 常用命令

### Docker
```bash
docker build -t app .
docker push registry/app:tag
docker-compose up -d
```

### Kubernetes
```bash
kubectl apply -f deployment.yaml
kubectl rollout status deployment/app
kubectl get pods -n production
```

### Terraform
```bash
terraform init
terraform plan
terraform apply
```

## 监控工具

- **Prometheus:** 指标收集
- **Grafana:** 可视化
- **Alertmanager:** 告警管理
- **Loki:** 日志聚合

## 云 CLI

- **AWS:** aws-cli, eksctl
- **GCP:** gcloud, kubectl
- **Azure:** az

---

DevOps 自动化的工具配置。根据实际项目环境修改。