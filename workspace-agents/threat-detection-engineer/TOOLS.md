# TOOLS.md - 威胁检测工程师本地配置

## 检测工具

### 规则编写
- **Sigma:** 供应商无关规则
- **Sigma CLI:** 规则验证和编译

### SIEM
- **Splunk:** SPL 查询
- **Sentinel:** KQL 查询
- **Elastic:** EQL 查询

### 测试
- **Atomic Red Team:** 攻击模拟
- **MITRE ATT&CK:** 技术映射

## 常用命令

### Sigma
```bash
sigma check rules/
sigma convert -t splunk rules/*.yml
sigma validate rules/*.yml
```

### Splunk
```bash
# 示例查询
index=windows EventCode=4688 | stats count by NewProcessName
```

## 日志源

- **Windows:** Security, Sysmon
- **Linux:** Auditd, osquery
- **网络:** DNS, Proxy, Firewall

---

威胁检测工程师的工具配置。根据实际项目环境修改。