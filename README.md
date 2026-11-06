# DonkeyYs （lys破解版）

## 使用方法
- 打开软件 用node生成卡密（签名设备id+时间戳+有效期）
- 找到喜欢的视频 点击悬浮窗即观看
- 点击悬浮按钮直接读取加密的m3u8
- 自动下载 AES-128 加密的 ts 分片、解密、合并为 MP4
- 带进度条显示
- 转换完成后询问是否保存到相册

---


### 安装到手机

**安卓直接用mt管理器或者自带浏览器（需要授权）
**方式 A：TrollStore（免越狱，推荐）**
- 适用 iOS 14.0 - 16.6.1（部分设备到 17.0）
- 下载 `DonkeyYY.app`，通过 TrollStore 安装即可，无需签名

**方式 B：侧载（需 Apple ID）**
- 用 `AltStore`、`Sideloadly` 或 `爱思助手` 等工具
- 导入 `DonkeyYY.ipa`，用你的 Apple ID 签名后安装
- 免费签名有效期 7 天，到期需重签

**方式 C：越狱设备**
- 直接用 Filza 安装 `DonkeyYY.app` 或 `DonkeyYY.ipa`

---


## 项目结构

```
DonkeyYY-iOS/
├── .github/workflows/build.yml   # GitHub Actions 自动编译配置
├── project.yml                    # XcodeGen 项目配置
├── DonkeyYY/
│   ├── AppDelegate.swift          # 应用入口
│   ├── ViewController.swift       # 主界面：WebView + 悬浮按钮 + m3u8查找
│   ├── M3U8Manager.swift          # 下载、解密、合并、转MP4
│   ├── Info.plist                 # 权限配置
│   └── Assets.xcassets/           # 图标资源
├── logo.png                       # 应用图标
└── README.md
```

## 注意事项

- 下载大视频时保持 App 在前台，iOS 后台限制较多
- 保存到相册需授权，首次会弹窗
- 悬浮按钮可拖动位置，轻点触发查找
- 进入视频页面后，等视频开始加载（出现画面/播放按钮）再点悬浮按钮
