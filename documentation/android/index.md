
### Basic integration

Integrate Chartboost in a few easy steps. Checkout our [Github repo](https://github.com/ChartBoost/client-examples) for a full example project.

Use requirements:
- Minimum API level 8 (Android OS 2.2)
- Requires permission: `android.permission.INTERNET`
- Optional (recommended) permissions: `WRITE_EXTERNAL_STORAGE`, `ACCESS_NETWORK_STATE`, `ACCESS_WIFI_STATE`

---

 1. Add the chartboost.jar file to your libs folder
 	- If you don't have a libs folder, create one and add the .jar file to it

 2.  Import the Chartboost SDK into any activity that uses Chartboost
    
    ```java
    	import com.chartboost.sdk.*;
    ```

 3. Add the following code to your `onCreate()` method:
    
    ```java
	// Configure Chartboost
	this.cb = Chartboost.sharedChartboost();
	String appId = "YOUR_APP_ID";
	String appSignature = "YOUR_APP_SIGNATURE";
	this.cb.onCreate(this, appId, appSignature, null);
	
	// Notify the beginning of a user session
	this.cb.startSession();
	
	// Show an interstitial
	this.cb.showInterstitial() 
	```

 4. Add the following code to your activity's `onStart()`, `onStop()`, and `onBackPressed()` methods:

	```java
    @Override
	protected void onStart() {
		super.onStart();
		
		this.cb.onStart(this);
	}
	
	@Override
	protected void onStop() {
		super.onStop();
		
		this.cb.onStop(this);
	}
	
	@Override
	public void onBackPressed() {

		// If an interstitial is on screen, close it. Otherwise continue as normal.
		if (this.cb.onBackPressed())
			return;
		else
			super.onBackPressed();
	}
    ```
    
---
   
### Advanced topics

<a class="article_box" href="/documentation/android/caching">Caching</a>: interstitials &amp; the More-Apps page for fast load times.

<a class="article_box" href="/documentation/android/delegation">Delegate methods</a>: to finely control Chartboost behavior in your app.

<a class="article_box" href="/documentation/android/analytics">Analytics</a>: tracking ARPU via transaction reporting.