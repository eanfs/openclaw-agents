# TOOLS.md - 视觉叙事师本地配置

## 创意工具

### 视频制作
- **After Effects:** 动画和动效
- **Premiere Pro:** 视频编辑
- **DaVinci Resolve:** 调色

### 图形设计
- **Figma:** 界面和原型
- **Illustrator:** 矢量图形
- **Photoshop:** 图片处理

### 数据可视化
- **D3.js:** 自定义数据可视化
- **Tableau:** 数据可视化
- **Canva:** 快速信息图

## 协作工具

- **Frame.io:** 视频协作审阅
- **Miro:** 故事板和头脑风暴
- **Notion:** 创意文档管理

## 常用命令

### 视频导出
```bash
# 导出视频
ffmpeg -i input.mov -codec copy output.mp4

# 压缩视频
ffmpeg -i input.mp4 -vcodec libx264 -crf 23 output.mp4
```

---

视觉叙事师的工具配置。根据实际项目环境修改。