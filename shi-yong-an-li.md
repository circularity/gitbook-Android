# 使用案例

### 初始化 AdManager <a id="initialize_mobileads"></a>

加载广告之前，请先调用 AdManager.getInstance\(\).init\(this\);，以便让应用初始化移动广告 SDK。此操作仅需执行一次，最好是在应用启动时执行。

 以下示例说明了如何在 Activity 中调用 `init()` 方法：

#### 示例 MainActivity（节选） <a id="example_mainactivity_excerpt"></a>

```text
package ...
import ...

public class MainActivity extends AppCompatActivity {
    ...
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        AdManager.getInstance().init(this);
    }
    ...
}

```

### 激励视频广告

```text
...
 loadVideo.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                AdManager.getInstance().loadVideoAd();
            }
        });
 AdManager.getInstance().setVideoListener(new VideoListener() {
            @Override
            public void onVideoLoad() {
                //加载成功
                Log.e("VideoListener","onVideoLoad");
                AdManager.getInstance().showCacheVideo();
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

...

```

### 插屏广告 

```text
...
 loadInterstitial.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        AdManager.getInstance().loadInterstitial();
    }
});
 AdManager.getInstance().setInterstitialListener(new InterstitialListener() {
            @Override
            public void onLoad() {
                Log.e("InterstitialListener","onLoad");
                text.setText("Interstitial is Load");
                if (AdManager.getInstance().isInterstitiaLoad()) {
                      AdManager.getInstance().showInterstitial();
                        }
            }

            @Override
            public void onClose() {
                Log.e("InterstitialListener","onClose");
            }

            @Override
            public void onFailedToLoad() {
                Log.e("InterstitialListener","onFailedToLoad");
                text.setText("Interstitial is onFailedToLoad");

            }

            @Override
            public void onOpened() {
                Log.e("InterstitialListener","onOpened");
            }
        });
...

```



```text
...
loadBanner.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        AdManager.getInstance().loadBanner();
    }
});

showBanner.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        if (AdManager.getInstance().bannerIsLoad()) {
            AdManager.getInstance().showBanner();
        }
    }
});
hideBanner.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                AdManager.getInstance().hideBanner();
            }
        });
 //添加广告回调
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
...

```



