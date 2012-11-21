Please apply to the Chartboost ARPU beta program before adding in-app purchase tracking to your app. Apply via <a href="mailto:bizdev@chartboost.com">bizdev@chartboost.com</a>.

## Record In-App Purchases

```objc
// Make sure you've already integrated chartboost and 
// called `startSessions` by this point.

// Initialize the CBAnalytics object
CBAnalytics *analytics = [CBAnalytics sharedAnalytics];

// Report transaction
[analytics recordPaymentTransaction:transaction                 // The SKPaymentTransaction
                         forProduct:product                     // The SKProduct
                               meta:@{@"coins-bought": @200}];  // Any custom meta-data
```