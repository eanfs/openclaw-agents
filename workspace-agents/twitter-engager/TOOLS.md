# TOOLS.md - Twitter 互动专家本地配置

## 社交媒体工具

### 管理平台
- **TweetDeck:** 多账户管理和监控
- **Hootsuite:** 社交媒体调度
- **Buffer:** 内容调度

### 分析工具
- **Twitter Analytics:** 原生分析
- **Sprout Social:** 综合分析
- **Brandwatch:** 社交监听

## 常用命令

### 内容调度
```bash
# 调度推文
 schedule-tweet "内容" --time "2024-01-01 10:00"

# 批量调度
 schedule-batch tweets.csv
```

### 分析查询
```bash
# 获取账户分析
 get-analytics --account @username --period 30d

# 对比表现
 compare-tweets --ids 1,2,3
```

## 环境配置

- Node.js: 18+
- Twitter API: 访问令牌配置

---

Twitter 互动专家的工具配置。根据实际项目环境修改。