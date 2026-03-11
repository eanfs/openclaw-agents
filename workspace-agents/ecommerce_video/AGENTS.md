# AGENTS.md - 工作空间规范

## 系统概述

本项目是一个电商营销视频生成的多Agent系统，通过4个子Agent的协作，完成从创意构思到视频发布的完整流程。

## Agent 架构

```
                    ┌─────────────────┐
                    │ multimedia-agent│ (主Agent)
                    │   协调调度       │
                    └────────┬────────┘
                             │
     ┌───────────────────────┼───────────────────────┐
     │                       │                       │
     ▼                       ▼                       ▼
┌────────────┐        ┌────────────┐         ┌────────────┐
│ market-    │        │ director-  │         │ release-   │
│ agent      │◄──────►│ agent      │◄───────►│ agent      │
│ 营销策划   │        │ 视频导演   │         │ 合成发布   │
└─────┬──────┘        └─────┬──────┘         └─────┬──────┘
      │                     │                       │
      │              ┌──────┴──────┐                │
      └─────────────►│ evaluate-   │◄───────────────┘
                     │ agent       │
                     │ 质量评估    │
                     └─────────────┘
```

## Agent 职责

### 1. multimedia-agent (主Agent)
- 协调其他4个Agent的工作
- 任务分发和进度跟踪
- 结果整合和问题升级

### 2. market-agent (营销策划)
- 解析商品信息
- 市场分析和竞品研究
- 制定营销策略
- 生成视频创意概念

### 3. director-agent (视频导演)
- 生成视频脚本和分镜
- 调用多模态能力生成素材
- 管理素材库

### 4. evaluate-agent (质量评估)
- 技术质量检测
- 内容质量分析
- 合规性检查
- 抽卡优化

### 5. release-agent (合成发布)
- 视频合成和后期处理
- 格式适配
- 多平台发布

## 目录结构

```
ecommerce_video/
├── agents/                    # Agent 目录
│   ├── multimedia-agent/     # 主Agent
│   ├── market-agent/         # 营销策划
│   ├── director-agent/       # 视频导演
│   ├── evaluate-agent/       # 质量评估
│   └── release-agent/        # 合成发布
├── workflow/                  # 工作流配置
├── protocol/                  # 通信协议
└── examples/                  # 示例数据
```

## 工作流程

1. **任务接收**：用户输入商品信息和要求
2. **营销策划**：market-agent 分析市场，生成创意
3. **视频生成**：director-agent 生成脚本和素材
4. **质量评估**：evaluate-agent 评估筛选素材
5. **合成发布**：release-agent 合成并发布视频

## A2A 通信

各Agent之间通过A2A协议进行通信，详见 `protocol/a2a-protocol.md`

## Memory

- **Daily notes:** `memory/YYYY-MM-DD.md` — raw logs
- **Long-term:** `MEMORY.md` — curated memories

## Safety

- 各Agent独立运行，互不访问内部数据
- 发布前必须通过质量评估
- 敏感内容零容忍

## Make It Yours

根据实际运行情况优化各Agent的配置和协作流程。