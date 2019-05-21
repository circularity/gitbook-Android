# 插屏广告

### 加载插屏广告

```text
AdManager.getInstance().loadInterstitial();
```

### 判断是否加载广告

```text
if (AdManager.getInstance().isInterstitiaLoad()) {
    AdManager.getInstance().showInterstitial();
}
```

### 显示插屏广告

```text
 AdManager.getInstance().showInterstitial();
```

### 设置回调事件

```text
AdManager.getInstance().setInterstitialListener(new InterstitialListener() {
            @Override
            public void onLoad() {
                Log.e("InterstitialListener","onLoad");
            }

            @Override
            public void onClose() {
                Log.e("InterstitialListener","onClose");
            }

            @Override
            public void onFailedToLoad() {
                Log.e("InterstitialListener","onFailedToLoad");
            }

            @Override
            public void onOpened() {
                Log.e("InterstitialListener","onOpened");
            }
        });
```

