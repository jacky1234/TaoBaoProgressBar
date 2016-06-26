#一个模仿淘宝秒杀商品页面的进度条

##Feature
有进度条加载动画

###Snapshot
![snapshot](https://github.com/jacky1234/TaoBaoProgressBar/blob/master/.raw/demo.gif)

##Usage

```XML
<com.liuhb.taobaoprogressbar.com.liuhb.taobaoprogressbar.view.CustomProgressBar
        android:layout_width="match_parent"
        android:layout_height="30dp"
        android:layout_marginTop="30dp"
        app:progress="2"
        app:max="100"
        app:progressRadius="10dp"
        app:progressDesc="已售"/>
```

###Advanced

```Java
        mProgressBar = (CustomProgressBar) findViewById(R.id.cpb_progresbar);
        mProgressBar.setOnFinishedListener(new CustomProgressBar.OnFinishedListener() {
            @Override
            public void onFinish() {
                Toast.makeText(MainActivity.this,"done!",Toast.LENGTH_SHORT).show();
            }
        });
        mProgressBar.setProgressDesc("剩余");
        mProgressBar.setMaxProgress(50);
        mProgressBar.setProgressColor(Color.parseColor("#F6CB82"));
        mProgressBar.setCurProgress(50);


        mProgressBar2 = (CustomProgressBar) findViewById(R.id.cpb_progresbar2);
        mProgressBar2.setOnAnimationEndListener(new CustomProgressBar.OnAnimationEndListener() {
            @Override
            public void onAnimationEnd() {
                Toast.makeText(MainActivity.this,"animation end!",Toast.LENGTH_SHORT).show();
            }
        });
        mProgressBar2.setProgressDesc("剩余");
        mProgressBar2.setMaxProgress(100);
        mProgressBar2.setProgressColor(Color.parseColor("#79aa6b"));
        mProgressBar2.setCurProgress(80,4000);
```
