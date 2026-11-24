# Lenovo ThinkCentre E96 hackintosh

联想 ThinkCentre E96 台式电脑

CPU：i5-8400 6核心

主板：联想313A（B360芯片组）只有HDMI和VGA接口

显卡：UHD630

声卡：ALC662

网卡：RTL8111

无线网卡：BCM94360CS2，蓝牙免驱，无线网卡通过 SimpleBCM.kext 驱动

OC版本：1.0.8

Mac系统版本：Sequoia 15.8.2

显示器：Lenovo LEN60EC T2224s (21.5英寸) 只有DVI和VGA接口


备注：核显HDMI输出，使用缓冲帧 从Big Sur开始已解决黑屏问题，使用HDMI转DVI线连接显示器！

## 更新日志

### 2.2.0（2026-11-24）体检修复版
- Drivers 补齐 OpenCore 1.0.8 必需字段（Arguments / HideVerbose / LoadEarly），OpenRuntime 置首
- 关闭 XhciPortLimit（USB 端口已由 SSDT-UIAC 定制映射）
- 移除与 SSDT-EC-USBX 重复的 SSDT-EC
- boot-args 精简为 alcid=12
- 关闭 AppleDebug / ApplePanic，Target=0，ExposeSensitiveData=6
- 键盘语言改为 zh-Hans:252
- RealtekRTL8111 升级至 3.0.0 官方包（build 3.0.4），重启实测千兆全双工正常
- ocvalidate（OC 1.0.8 官方）校验 0 错误
- 三码（序列号 / MLB / UUID / ROM）已清空，使用前请自行生成
