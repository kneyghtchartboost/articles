
The Chartboost iOS SDK is the cornerstone of the Chartboost network. It
provides the functionality for showing ads and  more apps pages, and tracking
analytics and in-app purchase revenue.


### Basic integration

Integrating Chartboost takes a few easy steps:

 1. Drop the Chartboost folder into your Xcode project.
    
    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <activity android:name="com.chartboost.sdk.CBDialogActivity"
        android:configChanges="orientation|keyboard|keyboardHidden"
        android:windowSoftInputMode="adjustResize"
        android:theme="@android:style/Theme.Translucent"
        android:launchMode="singleTop" >
    </activity>
    ```

 2.  Configure Chartboost and use it in your application:
    
    ```java
    // Configure ChartBoost
    ChartBoost _cb = ChartBoost.getSharedChartBoost(this);
    _cb.setAppId("app id");
    _cb.setAppSignature("app signature");

    // Notify an install
    _cb.install();

    // Show an interstitial
    _cb.showInterstitial();
    ```

3. Paste this into any activity that accesses the ChartBoost singleton:

    ```java
    @Override 
    protected void onResume()
    {
        super.onResume();
        ChartBoost.getSharedChartBoost(this);
    }

    ```
