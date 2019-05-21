# 激励视频广告

### 加载视频广告

```text
AdManager.getInstance().loadVideoAd();
```

### 单独加载admob广告

```text
AdManager.getInstance().loadMobVideoAd();
```

### 判断是否加载广告

```text
if (AdManager.getInstance().isLoadVideo()) {
    AdManager.getInstance().showCacheVideo();
}
```

### 显示已经加载的广告

```text
AdManager.getInstance().showCacheVideo();
```

