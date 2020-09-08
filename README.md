# PointBerry Event Tracker

### 1. pointberry-event-tracker-v1.0.0.aar을 다운로드 하여 프로젝트에 추가하세요.

### 2. `PointBerryImpressionTracker` 객체를 다음과 같이 선언하세요.
~~~java
PointBerryImpressionTracker = pbImpTracker = new PointBerryImpressionTracker(getApplicationContext());
~~~

### 3. 광고 리스너의 impression 콜백에서 `logImpression()`을 호출하세요. 다음은 MoPub의 예시입니다.
#### `MoPubView.BannerAdListener`
~~~java
@Override
public void onBannerLoaded(MoPubView banner) {
    // The banner has successfully retrieved an ad.
    pbImpTracker.logImpression(YOUR_BANNER_AD_UNIT_ID_HERE);
}
~~~
#### `MoPubInterstitial.InterstitialAdListener`
~~~java
@Override
public void onInterstitialShown(MoPubInterstitial interstitial) {
   // The interstitial has been shown.
   pbImpTracker.logImpression(YOUR_INTERSTITIAL_AD_UNIT_ID_HERE);
}
~~~
