Please apply to the Chartboost ARPU beta program before adding in-app purchase tracking to your app. Apply via <a href="mailto:bizdev@chartboost.com">bizdev@chartboost.com</a>.

## Record In-App Purchases

```java
// Make sure you've already integrated chartboost and 
// called `startSession` by this point.

// Create some meta data to pass with the purchase transaction
HashMap<String, Object> meta = new HashMap<String, Object>();
meta.put("item_id", 5);
meta.put("item_title", "Coins");

// Report transaction
CBAnalytics.sharedAnalytics().recordPaymentTransaction(
		"OBJECT_001", "Purchase Object", 0.99, "$", 1, meta);
```