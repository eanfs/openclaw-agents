# TOOLS.md - 微信小程序开发本地配置

## 开发工具

### 官方工具
- **微信开发者工具:** IDE 和调试
- **小程序基础库:** 版本兼容

### 框架
- **Taro:** 跨平台开发
- **uni-app:** Vue 开发
- **Remax:** 运行时开发

## 常用命令

### 微信 CLI
```bash
# 构建
npm run build:weapp

# 原生开发
wechat-devtools-cli start
```

### 代码示例
```javascript
// 登录
wx.login({
  success: res => {
    // 发送到服务端
  }
})

// 支付
wx.requestPayment({
  timeStamp: '',
  nonceStr: '',
  package: '',
  signType: 'MD5',
  paySign: '',
  success: () => {},
  fail: () => {}
})
```

## 审核要点

- 隐私合规
- 资质证明
- 用户体验
- 内容规范

---

微信小程序开发的工具配置。根据实际项目环境修改。