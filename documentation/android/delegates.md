Implement the delegate methods below to finely control Chartboost behavior in your app.

First, set the Chartboost delegate in Chartboost's onCreate() method, like so:

```java
this.cb.onCreate(this, appId, appSignature, this.chartBoostDelegate);

```

Then, setup your delegate methods. To see these in action, check out our [example code](https://github.com/ChartBoost/client-examples).

```java

private ChartboostDelegate chartBoostDelegate = new ChartboostDelegate() {

	/* 
	 * shouldDisplayInterstitial(String location)
	 *
	 * This is used to control when an interstitial should or should not be displayed
	 * If you should not display an interstitial, return NO
	 *
	 * For example: during gameplay, return NO.
	 *
	 * Is fired on:
	 * - showInterstitial()
	 * - Interstitial is loaded & ready to display
	 */
	@Override
	public boolean shouldDisplayInterstitial(String location) {
		return true;
	}
	
	/*
	 * shouldRequestInterstitial(String location)
	 * 
	 * This is used to control when an interstitial should or should not be requested
	 * If you should not request an interstitial from the server, return NO
	 *
	 * For example: user should not see interstitials for some reason, return NO.
	 *
	 * Is fired on:
	 * - cacheInterstitial()
	 * - showInterstitial() if no interstitial is cached
	 * 
	 * Notes: 
	 * - We do not recommend excluding purchasers with this delegate method
	 * - Instead, use an exclusion list on your campaign so you can control it on the fly
	 */
	@Override
	public boolean shouldRequestInterstitial(String location) {
		return true;
	}
	
	/*
	 * didCacheInterstitial(String location)
	 * 
	 * Passes in the location name that has successfully been cached
	 * 
	 * Is fired on:
	 * - cacheInterstitial() success
	 * - All assets are loaded
	 * 
	 * Notes:
	 * - Similar to this is: cb.hasCachedInterstitial(String location) 
	 * Which will return true if a cached interstitial exists for that location
	 */
	@Override
	public void didCacheInterstitial(String location) {
	   // Save which location is ready to display immediately
	}

	/*
	 * didFailToLoadInterstitial(String location)
	 * 
	 * This is called when an interstitial has failed to load for any reason
	 * 
	 * Is fired on:
	 * - cacheInterstitial() failure
	 * - showInterstitial() failure if no interstitial was cached
	 * 
	 * Possible reasons:
	 * - No network connection
	 * - No publishing campaign matches for this user (go make a new one in the dashboard)
	 */
	@Override
	public void didFailToLoadInterstitial(String location) {
	    // Show a house ad or do something else when a chartboost interstitial fails to load
	}

	/*
	 * didDismissInterstitial(String location)
	 *
	 * This is called when an interstitial is dismissed
	 *
	 * Is fired on:
	 * - Interstitial click
	 * - Interstitial close
	 *
	 * #Pro Tip: Use the code below to immediately re-cache interstitials
	 */
	@Override
	public void didDismissInterstitial(String location) {
		// Immediately re-caches an interstitial
		cb.cacheInterstitial(location);
	}

	/*
	 * didCloseInterstitial(String location)
	 *
	 * This is called when an interstitial is closed
	 *
	 * Is fired on:
	 * - Interstitial close
	 */
	@Override
	public void didCloseInterstitial(String location) {
		// Know that the user has closed the interstitial
	}

	/*
	 * didClickInterstitial(String location)
	 *
	 * This is called when an interstitial is clicked
	 *
	 * Is fired on:
	 * - Interstitial click
	 */
	@Override
	public void didClickInterstitial(String location) {
		// Know that the user has clicked the interstitial
	}

	/*
	 * didShowInterstitial(String location)
	 *
	 * This is called when an interstitial has been successfully shown
	 *
	 * Is fired on:
	 * - showInterstitial() success
	 */
	@Override
	public void didShowInterstitial(String location) {
		// Know that the user has seen the interstitial
	}

	/*
	 * More Apps delegate methods
	 */
	
	/*
	 * shouldDisplayLoadingViewForMoreApps()
	 *
	 * Return NO to prevent the pretty More-Apps loading screen
	 *
	 * Is fired on:
	 * - showMoreApps()
	 */
	@Override
	public boolean shouldDisplayLoadingViewForMoreApps() {
		return true;
	}

	/*
	 * shouldRequestMoreApps()
	 * 
	 * Return NO to prevent a More-Apps page request
	 *
	 * Is fired on:
	 * - cacheMoreApps()
	 * - showMoreApps() if no More-Apps page is cached
	 */
	@Override
	public boolean shouldRequestMoreApps() {
		return true;
	}

	/*
	 * shouldDisplayMoreApps()
	 * 
	 * Return NO to prevent the More-Apps page from displaying
	 *
	 * Is fired on:
	 * - showMoreApps() 
	 * - More-Apps page is loaded & ready to display
	 */
	@Override
	public boolean shouldDisplayMoreApps() {
		return true;
	}

	/*
	 * didFailToLoadMoreApps()
	 * 
	 * This is called when the More-Apps page has failed to load for any reason
	 * 
	 * Is fired on:
	 * - cacheMoreApps() failure
	 * - showMoreApps() failure if no More-Apps page was cached
	 * 
	 * Possible reasons:
	 * - No network connection
	 * - No publishing campaign matches for this user (go make a new one in the dashboard)
	 */
	@Override
	public void didFailToLoadMoreApps() {
		// Do something else when the More-Apps page fails to load
	}

	/*
	 * didCacheMoreApps()
	 * 
	 * Is fired on:
	 * - cacheMoreApps() success
	 * - All assets are loaded
	 */
	@Override
	public void didCacheMoreApps() {
		// Know that the More-Apps page is cached and ready to display
	}

	/*
	 * didDismissMoreApps()
	 *
	 * This is called when the More-Apps page is dismissed
	 *
	 * Is fired on:
	 * - More-Apps click
	 * - More-Apps close
	 */
	@Override
	public void didDismissMoreApps() {
		// Know that the More-Apps page has been dismissed
	}

	/*
	 * didCloseMoreApps()
	 *
	 * This is called when the More-Apps page is closed
	 *
	 * Is fired on:
	 * - More-Apps close
	 */
	@Override
	public void didCloseMoreApps() {
		// Know that the More-Apps page has been closed
	}

	/*
	 * didClickMoreApps()
	 *
	 * This is called when the More-Apps page is clicked
	 *
	 * Is fired on:
	 * - More-Apps click
	 */
	@Override
	public void didClickMoreApps() {
		// Know that the More-Apps page has been clicked

	}

	/*
	 * didShowMoreApps()
	 *
	 * This is called when the More-Apps page has been successfully shown
	 *
	 * Is fired on:
	 * - showMoreApps() success
	 */
	@Override
	public void didShowMoreApps() {
		// Know that the More-Apps page has been presented on the screen
	}

	/*
	 * shouldRequestInterstitialsInFirstSession()
	 *
	 * Return false if the user should not request interstitials until the 2nd startSession()
	 * 
	 */
	@Override
	public boolean shouldRequestInterstitialsInFirstSession() {
		return true;
	}
};

```