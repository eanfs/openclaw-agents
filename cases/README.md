# OpenClaw 应用案例集

本目录包含 openclaw AI 智能体框架的多个行业应用案例。

## 案例列表

| 案例 | 目录 | 描述 |
|------|------|------|
| 电商短视频创作 | `ecommerce_video/` | 为电商平台创作吸引人的短视频脚本和创意 |
| 运维维护系统 | `devops_maintenance/` | 系统监控、故障排查、日志分析、自动化运维 |
| 金融投资分析 | `investment_analysis/` | 市场分析、个股研究、投资建议（仅供参考） |

## 如何使用

每个案例都是一个独立的工作空间，包含以下核心文件：

```
cases/[案例名]/
├── IDENTITY.md    # AI 身份定义
├── SOUL.md        # 核心价值观和行为准则
├── USER.md        # 用户/客户信息
├── AGENTS.md      # 工作空间规范
├── TOOLS.md       # 本地工具配置
└── HEARTBEAT.md   # 周期性任务
```

### 快速开始

1. 选择一个案例目录
2. 根据实际情况修改 `USER.md` 中的用户信息
3. 根据需要更新 `TOOLS.md` 中的工具配置
4. 开始使用 AI 智能体

## 添加新案例

参考现有案例结构，复制并修改：
```bash
cp -r cases/ecommerce_video cases/your_new_case
```

然后修改各文件内容即可。