# TOOLS.md - 工具配置

## Agent 通信

### A2A 协议配置

```yaml
protocol:
  name: "A2A"
  version: "1.0"
  transport: "json-rpc"

agents:
  market-agent:
    endpoint: "internal://market-agent"
    timeout: 300s
    retry: 3

  director-agent:
    endpoint: "internal://director-agent"
    timeout: 600s
    retry: 2

  evaluate-agent:
    endpoint: "internal://evaluate-agent"
    timeout: 300s
    retry: 2

  release-agent:
    endpoint: "internal://release-agent"
    timeout: 300s
    retry: 2
```

## 任务模板

### 营销策划任务
```json
{
  "task": "market_analysis",
  "input": {
    "product_url": "",
    "product_info": {}
  },
  "output": {
    "marketing_strategy": {},
    "video_concepts": []
  }
}
```

### 视频导演任务
```json
{
  "task": "generate_video",
  "input": {
    "marketing_strategy": {},
    "video_concept": {}
  },
  "output": {
    "scripts": [],
    "video_materials": []
  }
}
```

### 评估任务
```json
{
  "task": "evaluate_quality",
  "input": {
    "video_materials": []
  },
  "output": {
    "quality_scores": [],
    "selected_materials": []
  }
}
```

### 合成发布任务
```json
{
  "task": "synthesize_release",
  "input": {
    "selected_materials": [],
    "release_config": {}
  },
  "output": {
    "final_videos": [],
    "release_results": []
  }
}
```

---