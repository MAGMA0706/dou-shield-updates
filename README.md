# 豆包安全护盾 · 更新清单

这个仓库只存放公开的更新清单 `latest.json`，不包含源码。

App 通过 jsDelivr（失败回退 GitHub raw）读取清单，比较 `versionCode`，下载 APK 后校验 SHA-256 与签名，再拉起系统安装器。

## 清单格式

```json
{
  "versionCode": 302,
  "versionName": "3.0.2",
  "apkUrl": "https://.../apk",
  "sha256": "64位小写十六进制",
  "size": 19000000,
  "changelog": ["..."],
  "force": false
}
```

`apkUrl` 必须是 HTTPS；`size` 单位为字节；`force=true` 时客户端不允许「稍后」。
