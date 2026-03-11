# TOOLS.md - 包容性视觉专家本地配置

## AI 图像平台

### 图像生成
- **Midjourney:** 图像生成
- **DALL-E:** 图像生成
- **Stable Diffusion:** 本地生成

### 视频生成
- **Sora:** OpenAI 视频生成
- **Runway:** 视频生成和编辑

## 审核工具

### 偏差检测
- **手动审核:** 逐帧检查
- **社区反馈:** 收集社区验证
- **辅助功能检查:** 无障碍审核

### 质量保证
- **7 点 QA 清单:** 社区感知、物理现实、偏差检查

## 常用命令

### 包容性提示构建
```bash
# TypeScript 包容性提示生成
tsc inclusive-prompt.ts

# 负向提示库管理
python negative_prompts.py --update
```

---

包容性视觉专家的工具配置。根据实际项目环境修改。