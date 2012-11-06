
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

## Track Generic Events

TODO: Some blurb explaining what generic events are and why one would use them:

```objc
// Initialize the CBAnalytics object
CBAnalytics *analytics = [CBAnalytics sharedAnalytics];

// Track a simple event
[analytics trackEvent:@"crash"];

// Track an event with a value
[analytics trackEvent:@"score" withValue:@4567890];

// Track an event with metadata
[analytics trackEvent:@"level"
         withMetadata:@{@"level": @1, @"boosts": @[@"jetpack", @"snowmobile"]}];

// Track an event with a value & metadata
[analytics trackEvent:@"score"
            withValue:@4567890
         withMetadata:@{@"level": @1, @"boosts": @[@"jetpack", @"snowmobile"]}];
```
