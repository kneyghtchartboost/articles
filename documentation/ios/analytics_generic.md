## Track Generic Events

TODO: Some blurb explaining what generic events are and why one would use them.
Also add this back to analytics.md when ready.

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
          andMetadata:@{@"level": @1, @"boosts": @[@"jetpack", @"snowmobile"]}];
```
