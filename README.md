# TikTools

**你的 TikTok 工具箱 · Xposed 模块**

地区和城市预设、地图手选位置、本机设备参数、界面规则、关键词评论过滤、本机翻译与可识别视频保存。各组功能独立开关。

[下载](https://github.com/Xposed-Modules-Repo/io.github.sunisup666.tiktools/releases) · [源码与完整说明](https://github.com/sunisup666/TikTools) · [反馈](https://github.com/sunisup666/TikTools/issues) · [隐私说明](https://github.com/sunisup666/TikTools/blob/main/docs/PRIVACY.md)

## 使用

1. 需要 Android 13+、ARM64 和 Vector 或兼容的 LSPosed / Xposed 框架。
2. 安装 APK，在框架中启用 TikTools，仅勾选自己实际使用的 TikTok。
3. 打开 TikTools，启用总开关并按需打开各组功能；修改后强行停止并重新打开 TikTok。

23 个地区和 46 个城市预设会成套填入相关参数。地图采用 WGS84，手选位置在点击保存后生效；IP 更新保留已经手选的坐标。设备字段默认使用本机真实值。

在“界面”中启用应用内工具入口后，可使用 TikTok 中的 **TT** 按钮。翻译首次使用需要下载 ML Kit 语言模型；视频保存需要先打开下载控制并确认下载。

## 验证范围

已测试 Redmi K40、Android 17、Vector 2.2、TikTok `com.ss.android.ugc.trill` 47.4.3 / 470403。另一个 TikTok 包名 `com.zhiliaoapp.musically` 及其他版本尚未完整验证。

界面规则只处理可识别的小视图，部分规则依赖具体版本。保存不支持直播、图片帖、DRM、分段流或无法明确对应当前内容的地址；本轮公开包的保存复测未识别到明确直链，不能保证任意视频均可保存。定位与设备字段只影响目标进程读取的部分值，不改变硬件或服务端状态。

具体结果和边界见 [测试记录](https://github.com/sunisup666/TikTools/blob/main/docs/TESTING.md)。短时间复测不代表长期稳定或未来版本兼容。

本目录仓库保存说明和安装包。构建脚本、应用源码、更新记录、依赖说明及 [Agent 分析指南](https://github.com/sunisup666/TikTools/blob/main/docs/APP_PLUGIN_ANALYSIS_GUIDE.md) 位于 [sunisup666/TikTools](https://github.com/sunisup666/TikTools)。
