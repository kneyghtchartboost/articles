
The Chartboost SDK is the cornerstone of the Chartboost network. It
provides the functionality for showing interstitials and  More-Apps pages, as well as tracking
analytics and in-app purchase revenue.


### Basic integration

Integrating Chartboost takes a few easy steps. Checkout our (Github repo)[https://github.com/ChartBoost/client-examples] for a full example project.

Use requirements:
- Minimum API level 8 (Android OS 2.2)
- Requires permission: android.permission.INTERNET
- Optional (recommended) permissions: WRITE_EXTERNAL_STORAGE, ACCESS_NETWORK_STATE, ACCESS_WIFI_STATE

---

 1. Add the chartboost.jar file as an external jar to your project 
 - Right click project > Properties > Java Build Path > Libraries > Add External JARs...
 - Select "Order and Export" and select checkbox next to chartboost.jar

 2.  Import the Chartboost SDK into any activity that uses Chartboost
    
    ```java
    import com.chartboost.sdk.*;
    ```

 3. Add the following code to your onCreate() method:
    
    ```java
		// Configure Chartboost
		this.cb = Chartboost.sharedChartboost();
		String appId = "YOUR_APP_ID";
		String appSignature = "YOUR_APP_SIGNATURE";
		this.cb.onCreate(this, appId, appSignature, this.chartBoostDelegate);
		
		// Notify the beginning of a user session
		this.cb.startSession();
		
		// Show an interstitial
		this.cb.showInterstitial() 
	```

 4. Add the following code to your activity's onStart(), onStop(), and onBackPressed() methods :

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
			if (this.cb.onBackPressed())
				return;
			else
				super.onBackPressed();
		}
    ```