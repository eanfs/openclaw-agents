# TOOLS.md - 嵌入式固件工程师本地配置

## 开发工具

### IDE
- **VS Code:** 通用编辑器
- **PlatformIO:** 跨平台固件开发
- **STM32CubeIDE:** STM32 专用

### 框架
- **ESP-IDF:** ESP32 开发
- **STM32 HAL/LL:** STM32 驱动
- **Zephyr:** 跨平台 RTOS

## 常用命令

### PlatformIO
```bash
pio run -t upload
pio device monitor
pio test
```

### ESP-IDF
```bash
idf.py build
idf.py flash monitor
idf.py coredump-info
```

### OpenOCD
```bash
openocd -f interface/stlink.cfg -f target/stm32f4.cfg
```

## 调试工具

- **JTAG/SWD:** 硬件调试
- **逻辑分析仪:** 信号分析
- **示波器:** 时序验证

---

嵌入式固件工程师的工具配置。根据实际项目环境修改。