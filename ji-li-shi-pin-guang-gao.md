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

### 设置回调事件

```text
AdManager.getInstance().setVideoListener(new VideoListener() {
            @Override
            public void onVideoLoad() {
                //加载成功
                Log.e("VideoListener","onVideoLoad");
            }

            @Override
            public void onVideoClose() {
                //视频被关闭
                Log.e("VideoListener","onVideoClose");
            }

            @Override
            public void onVideoCompleted() {
                //发放视频奖励
                Log.e("VideoListener","onVideoCompleted");
            }

            @Override
            public void onVideoFailedToLoad() {
                Log.e("VideoListener","onVideoFailedToLoad");
                text.setText("Video is FailedToLoad");
            }

            @Override
            public void onVideoOpened() {
                Log.e("VideoListener","onVideoOpened");
            }
        });
```

