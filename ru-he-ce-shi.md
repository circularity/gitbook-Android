---
description: 可根据需求选择以下方式来进行测试
---

# 如何测试

**1.测试Admob 通过查看log添加设备到测试列表**

log格式如下

```text
I/Ads: Use AdRequest.Builder.addTestDevice("A903DDFCF6FFDD6FD076C25212D21F91") to get test ads on this device.
```

然后在GoogleAdScript脚本CreateAdRequest 中加入设备到测试列表

**2.使用Admob测试id**

**Android**

```text
横幅广告    ca-app-pub-3940256099942544/6300978111
插页式广告    ca-app-pub-3940256099942544/1033173712
激励视频广告    ca-app-pub-3940256099942544/5224354917
```

**iOS**

```text
横幅广告    ca-app-pub-3940256099942544/2934735716
插页式广告    ca-app-pub-3940256099942544/4411468910
激励视频广告    ca-app-pub-3940256099942544/1712485313
```

**3.测试Facebook广告**

3.1.提供设备id由我们加入到后台

ios为Identifier for Advertising \(IDFA\) for iOS devices

Android为Google Advertising ID \(AAID\) for Android devices Android 可以在谷歌服务中广告页面查看，也可下载infinia.optout查看

[https://play.google.com/store/apps/details?id=com.infinia.optout](https://play.google.com/store/apps/details?id=com.infinia.optout)

**3.2添加设备id到测试列表**

添加facebook测试设备id ,可在log中查看 D/AdInternalSettings: Test mode device hash: 95a42086-7454-4862-b166-191f351e53b9

```text
AdSettings.addTestDevice("95a42086-7454-4862-b166-191f351e53b9";
```

