## Caching interstitials

Interstitials may be cached to display at a later time:

```objc
// Instead of using [cb showInterstitial] as above, cache it first:
[cb cacheInterstitial];

// Then when you want to display the interstitial, use:
[cb showInterstitial];

// Each interstitial location has it's own cache, so cache each location like this:
[cb cacheInterstitial:@"After Level One"];
[cb cacheInterstitial:@"Pause Screen"];

// Then display the cached interstitial by location:
[cb showInterstitial:@"After Level One"];
```

Be notified of interstitial cache success with the following optional method:

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
