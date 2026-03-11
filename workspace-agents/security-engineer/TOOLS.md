# TOOLS.md - 安全工程师本地配置

## 开发工具

### 静态分析
- **Semgrep:** 代码安全扫描
- **SonarQube:** 代码质量
- **ESLint:** JavaScript 安全

### 动态测试
- **Burp Suite:** Web 渗透测试
- **OWASP ZAP:** 自动化扫描
- **Postman:** API 测试

### 依赖扫描
- **Snyk:** 漏洞扫描
- **npm audit:** Node 审计
- **Trivy:** 容器扫描

## 常用命令

### Semgrep
```bash
semgrep --config=auto
semgrep --config=p/owasp-top-ten
```

### npm
```bash
npm audit
npm audit fix
```

### Docker
```bash
trivy image myapp:latest
trivy fs --security-checks vuln .
```

## 学习资源

- OWASP Top 10
- CWE Top 25
- MITRE ATT&CK
- 安全编码指南

---

安全工程师的工具配置。根据实际项目环境修改。