## Caching interstitials

Interstitials may be cached to display at a later time:

```objc
// Instead of using [cb showInterstitial], cache it first:
[cb cacheInterstitial];

// Then when you want to display the interstitial, use:
[cb showInterstitial];

// Each interstitial location has it's own cache, so cache each location like this:
[cb cacheInterstitial:@"After Level One"];
[cb cacheInterstitial:@"Pause Screen"];

// Then display the cached interstitial by location:
[cb showInterstitial:@"After Level One"];
```

Be notified of interstitial cache success with the optional method below. The SDK will pass in the named location of the cached interstitial.

```objc
// Called when an interstitial has been received and cached.
- (void)didCacheInterstitial:(NSString *)location;
```

Check to see if an interstitial is cached using:

```objc
// Implement this to check if an interstitial is stored in cache for the default location
[cb hasCachedInterstitial];

// Implement this to check if an interstitial is stored in cache for a specific location
[cb hasCachedInterstitial:@"After Level One"];
```

## Caching more apps

```objc
// To quickly display the more apps page, you may cache it similar to interstitials above
[cb cacheMoreApps];

// Then show the more apps page in the same way
[cb showMoreApps];
```

## Notes on Caching

- `[cb showInterstitial]` displays a cached interstitial if one exists. Otherwise it will load one from the server.
- Each named location has it's own cache. If you call `[cb cacheInterstitial]` without specifying a location, the "Default" location is used.
- Caching is recommended for the best performance, but be conscious of data usage for your users.
- Cached interstitials automatically expire after 24 hours.
- Interstitial requests are asynchronous. Keep this in mind if you cache many interstitials while loading other data for your app.
- ProTip: Use the `didDismissInterstitial` delegate method to automatically re-cache interstitials like this:

```objc
- (void)didDismissInterstitial:(NSString *)location {
    [[Chartboost sharedChartboost] cacheInterstitial:location];
}
```

- Similarly use `didDismissMoreApps` to automatically re-cache the More-Apps page:

```objc
- (void)didDismissMoreApps {
    [[Chartboost sharedChartboost] cacheMoreApps];
}
```
