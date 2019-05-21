# Banner广告

### 加载Banner广告

```text
AdManager.getInstance().loadBanner();
```

### 判断广告是否加载

```text
if (AdManager.getInstance().bannerIsLoad()) {
    AdManager.getInstance().showBanner();
}
```

### 显示Banner广告

```text
AdManager.getInstance().showBanner();
```

### 隐藏banner广告

```text
AdManager.getInstance().hideBanner();
```

### 设置回调事件

```text
AdManager.getInstance().setBannerListener(new BannerListener() {
            @Override
            public void onBannerLoad() {
                //加载成功
                Log.e("BannerListener","onBannerLoad");
                text.setText("Banner is load");
            }

            @Override
            public void onBannerHide() {
                //隐藏banner
                Log.e("BannerListener","onBannerHide");
            }

            @Override
            public void onBannerShow() {
                //显示banner
                Log.e("BannerListener","onBannerShow");
            }

            @Override
            public void onBannerFailedToLoad() {
                //加载失败
                Log.e("BannerListener","onBannerFailedToLoad");
                text.setText("Banner is FailedToLoad");
            }

            @Override
            public void onBannerOpened() {
                //点击banner
                Log.e("BannerListener","onBannerOpened");
            }
        });
```

