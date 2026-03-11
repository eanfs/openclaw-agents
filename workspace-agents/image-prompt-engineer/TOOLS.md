# TOOLS.md - 图像提示工程师本地配置

## AI 图像平台

### 主流平台
- **Midjourney:** Discord 图像生成
- **DALL-E:** OpenAI 图像生成
- **Stable Diffusion:** 本地/云端图像生成
- **Flux:** 新兴图像生成模型

### 提示词工具
- **PromptHero:** 提示词库
- **PromptBase:** 提示词模板
- **Midjourney Prompt Generator:** 提示词生成

## 图像处理

### 图像编辑
- **Photoshop:** 图像精修
- **Lightroom:** 调色
- **Midjourney Vary (Region):** 局部重绘

### 图像管理
- **Eagle:** 设计资源管理
- **Bridge:** 素材管理

## 常用命令

### 图像生成
```bash
# Midjourney 参数
/imagine prompt: [描述] --ar 16:9 --v 6 --stylize 250

# Stable Diffusion
python generate.py --prompt "[描述]" --steps 30 --cfg 7.5
```

---

图像提示工程师的工具配置。根据实际项目环境修改。