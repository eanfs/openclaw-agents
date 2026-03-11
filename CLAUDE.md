# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个 OpenClaw AI 智能体框架的应用案例集，包含多个行业的工作空间配置和 agent-agents 智能体库。

## 目录结构

```
openclaw-cases/
├── agency-agents/     # AI 智能体集合库 (112+ 专业智能体)
├── cases/             # 独立案例工作空间
│   ├── ecommerce_video/
│   ├── devops_maintenance/
│   └── investment_analysis/
├── workspace-*/       # 各领域工作空间模板
│   ├── workspace-devops/
│   ├── workspace-marketing/
│   ├── workspace-media-creator/
│   └── workspace-work/
└── media-agents/      # 电商视频多智能体系统
    ├── director-agent/
    ├── evaluate-agent/
    ├── market-agent/
    ├── multimedia-agent/
    └── release-agent/
```

## 常用命令

### 安装 agency-agents 到 Claude Code

```bash
cp -r agency-agents/* ~/.claude/agents/
```

### 集成转换脚本

```bash
cd agency-agents
./scripts/convert.sh              # 转换所有工具
./scripts/install.sh --tool cursor  # 安装到指定工具
```

## 工作空间结构

每个工作空间遵循 OpenClaw 规范，包含以下核心文件：

| 文件 | 用途 |
|------|------|
| `IDENTITY.md` | 智能体名称、风格、表情符号 |
| `SOUL.md` | 人设、语气和边界 |
| `USER.md` | 用户信息 |
| `AGENTS.md` | 工作空间规范和规则 |
| `TOOLS.md` | 本地工具配置 |
| `HEARTBEAT.md` | 周期性任务 |
| `memory/` | 每日记忆日志 |

## 智能体系统

### agency-agents

包含 11 个专业部门的 112+ 个 AI 智能体：
- Engineering (工程)、Design (设计)、Paid Media (付费媒体)
- Marketing (营销)、Product (产品)、Project Management (项目管理)
- Testing (测试)、Support (支持)、Spatial Computing (空间计算)
- Game Development (游戏开发)、Specialized ( specialized)

支持多工具集成：Claude Code、Copilot、Cursor、Windsurf、Aider、OpenCode、Gemini CLI、OpenClaw

### media-agents

电商视频创作多智能体系统，包含 5 个协作 Agent：

1. **Market Agent** - 营销策划（市场分析、竞品研究、生成策略）
2. **Director Agent** - 视频导演（脚本生成、视觉提示词、素材创作）
3. **Evaluate Agent** - 质量评估（视觉质量 75%、内容相关度 20%、创意 5%，通过线 70 分）
4. **Release Agent** - 合成发布（FFmpeg 合成、多平台发布）
5. **Multimedia Agent** - 多媒体处理

工作流程：`用户输入 → 营销分析 → 脚本生成 → 素材创作 → 质量评估 → (循环优化) → 视频合成 → 多平台发布`

## 快速开始

1. 选择或复制一个工作空间目录
2. 根据实际情况修改 `USER.md` 中的用户信息
3. 根据需要更新 `TOOLS.md` 中的工具配置
4. 开始使用 AI 智能体