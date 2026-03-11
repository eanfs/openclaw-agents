# TOOLS.md - 后端架构师本地配置

## 开发工具

### 编辑器
- **VS Code:** 推荐配置
  - Extensions: Go, Java, PostgreSQL, Docker, Terraform
  - Settings: Format on save, lint on save

### 数据库
- **PostgreSQL:** 主要关系型数据库
- **Redis:** 缓存和消息队列
- **pgAdmin / DBeaver:** 数据库管理工具

## 常用命令

### Docker
```bash
docker build -t app .
docker run -d -p 8080:8080 app
docker-compose up -d
```

### Kubernetes
```bash
kubectl get pods -n production
kubectl rollout status deployment/app
kubectl logs -f deployment/app
```

### 数据库
```bash
psql -U postgres -d mydb
redis-cli
```

## 云 CLI

- **AWS:** aws-cli, eksctl, terraform
- **GCP:** gcloud, kubectl
- **Azure:** az, terraform

## 监控工具

- **Prometheus:** 指标收集和查询
- **Grafana:** 可视化监控面板
- **Jaeger:** 分布式链路追踪

## 环境配置

- Go: 1.21+
- Java: 17+
- Node.js: 18+
- Python: 3.10+
- PostgreSQL: 15+
- Redis: 7+

---

后端架构师的工具配置。根据实际项目环境修改。