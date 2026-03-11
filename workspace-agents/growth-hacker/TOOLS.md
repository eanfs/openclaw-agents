# TOOLS.md - 增长黑客本地配置

## 分析工具

### 用户行为分析
- **Amplitude:** 产品分析平台
- **Mixpanel:** 高级分析
- **Google Analytics:** 网站分析

### A/B 测试
- **Optimizely:** 实验平台
- **LaunchDarkly:** 功能开关和实验

### 数据可视化
- **Looker Studio:** 数据仪表板
- **Metabase:** 开源 BI

## 常用命令

### 数据查询
```sql
-- 用户留存分析
SELECT
  cohort_date,
  COUNT(DISTINCT user_id) as users,
  COUNT(DISTINCT CASE WHEN days_since_first_login >= 7 THEN user_id END) as retained_7d,
  COUNT(DISTINCT CASE WHEN days_since_first_login >= 30 THEN user_id END) as retained_30d
FROM user_cohorts
GROUP BY cohort_date;
```

### 实验分析
```python
# 计算实验结果的统计显著性
from scipy import stats

control_conversions = 150
control_total = 1000
treatment_conversions = 180
treatment_total = 1000

control_rate = control_conversions / control_total
treatment_rate = treatment_conversions / treatment_total

# 双尾 z-test
z_score = (treatment_rate - control_rate) / ...
p_value = stats.norm.sf(abs(z_score)) * 2
```

## 环境配置

- Python: 3.8+ (用于数据分析)
- SQL: 基础查询能力
- Excel/Google Sheets: 数据处理

---

增长黑客的工具配置。根据实际项目环境修改。