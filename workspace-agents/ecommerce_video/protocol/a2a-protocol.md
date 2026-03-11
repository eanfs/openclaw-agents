# A2A 通信协议

## 概述

本协议定义了电商营销视频生成系统中各Agent之间的通信规范。

## 通信架构

```
                    ┌─────────────────┐
                    │ multimedia-agent│ (主Agent)
                    └────────┬────────┘
           ┌────────────────┼────────────────┐
           │                │                │
           ▼                ▼                ▼
    ┌────────────┐   ┌────────────┐   ┌────────────┐
    │market-agent│   │director-   │   │release-    │
    │            │◄─►│agent       │◄─►│agent       │
    └─────┬──────┘   └─────┬──────┘   └─────┬──────┘
          │                │                │
          │         ┌──────┴──────┐         │
          │         │evaluate-    │         │
          └────────►│agent        │◄────────┘
                    └─────────────┘
```

## 消息格式

### 请求消息

```json
{
  "id": "req_001",
  "type": "request",
  "from": "multimedia-agent",
  "to": "market-agent",
  "task": "market_analysis",
  "timestamp": "2024-01-01T12:00:00Z",
  "payload": {
    "product_url": "https://...",
    "product_info": {...},
    "requirements": {...}
  },
  "context": {
    "task_id": "task_001",
    "user_id": "user_001",
    "priority": "high"
  }
}
```

### 响应消息

```json
{
  "id": "resp_001",
  "type": "response",
  "from": "market-agent",
  "to": "multimedia-agent",
  "ref_id": "req_001",
  "status": "success",
  "timestamp": "2024-01-01T12:01:00Z",
  "payload": {
    "marketing_strategy": {...},
    "video_concepts": [...]
  }
}
```

### 事件消息

```json
{
  "id": "evt_001",
  "type": "event",
  "from": "director-agent",
  "to": "multimedia-agent",
  "event": "progress_update",
  "timestamp": "2024-01-01T12:02:00Z",
  "data": {
    "progress": 50,
    "message": "素材生成中...",
    "details": {...}
  }
}
```

### 错误消息

```json
{
  "id": "err_001",
  "type": "error",
  "from": "evaluate-agent",
  "to": "multimedia-agent",
  "timestamp": "2024-01-01T12:03:00Z",
  "error": {
    "code": "EVALUATION_FAILED",
    "message": "素材质量不达标",
    "details": {...},
    "suggestion": "建议重新生成素材"
  }
}
```

## 任务类型

| 任务 | 发送方 | 接收方 | 描述 |
|-----|-------|-------|------|
| market_analysis | multimedia-agent | market-agent | 市场营销分析任务 |
| creative_generation | multimedia-agent | market-agent | 创意概念生成 |
| script_generation | multimedia-agent | director-agent | 脚本生成任务 |
| material_generation | director-agent | director-agent | 素材生成任务 |
| quality_evaluation | multimedia-agent | evaluate-agent | 质量评估任务 |
| synthesis | multimedia-agent | release-agent | 视频合成任务 |
| publish | multimedia-agent | release-agent | 发布任务 |

## 状态码

| 状态码 | 说明 |
|-------|------|
| success | 任务成功完成 |
| failed | 任务失败 |
| pending | 任务待处理 |
| running | 任务执行中 |
| paused | 任务暂停 |
| timeout | 任务超时 |

## 心跳机制

- 心跳间隔：30秒
- 超时阈值：120秒
- 心跳内容：当前状态、进度百分比

---