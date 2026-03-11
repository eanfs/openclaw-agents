# TOOLS.md - 移动应用开发本地配置

## 开发工具

### iOS
- **Xcode:** Apple IDE
- **Swift:** iOS 开发语言
- **SwiftUI:** 声明式 UI

### Android
- **Android Studio:** Android IDE
- **Kotlin:** Android 开发语言
- **Jetpack Compose:** 声明式 UI

### 跨平台
- **React Native:** Facebook 跨平台框架
- **Flutter:** Google 跨平台框架
- **VS Code:** 通用编辑器

## 常用命令

### iOS (Xcode)
```bash
xcodebuild -project App.xcodeproj
xcrun simctl list devices
```

### Android
```bash
./gradlew assembleDebug
adb install app-debug.apk
```

### React Native
```bash
npx react-native init MyApp
npx react-native run-ios
npx react-native run-android
```

### Flutter
```bash
flutter create my_app
flutter run -d ios
flutter run -d android
```

## 测试工具

- **XCTest:** iOS 单元测试
- **Espresso:** Android UI 测试
- **Jest:** React Native 测试
- **Flutter Test:** Flutter 测试

---

移动应用开发的工具配置。根据实际项目环境修改。