# 速度传感器参数计算器 - iOS 版

基于 Capacitor 构建的 iOS 应用，与 Android 版共用同一套 Web 源码。

## 项目结构

```
WheelPulseCalc-iOS/
├── www/                    # Web 源码（与 Android 共用）
│   ├── index.html         # 主页面
│   ├── ratio.html         # 轮径比计算页面
│   └── css/style.css      # 样式文件
├── package.json           # Node.js 依赖
├── capacitor.config.json  # Capacitor 配置
└── .github/workflows/     # GitHub Actions 自动构建
    └── build-ios.yml
```

## 自动构建

每次推送代码到 `main` 分支，GitHub Actions 会自动：
1. 在 macOS 环境中构建 iOS 应用
2. 打包成 IPA 文件
3. 上传到 GitHub Release

## 下载安装

1. 进入 GitHub Release 页面
2. 下载 `WheelPulseCalc-iOS.ipa`
3. 使用 AltStore 等工具安装到 iPhone

## 本地开发（需要 Mac）

```bash
# 安装依赖
npm install

# 添加 iOS 平台
npx cap add ios

# 同步文件
npx cap sync ios

# 打开 Xcode
npx cap open ios
```

## 与 Android 版同步

当 `www/` 目录有更新时，需要同时更新两个仓库：
- [WheelPulseCalc-Android](https://github.com/你的用户名/WheelPulseCalc-Android)
- [WheelPulseCalc-iOS](https://github.com/你的用户名/WheelPulseCalc-iOS)
