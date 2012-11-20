<a class="big_button" href="https://chartboost.com/support/sdk_download/3.1?os=android">Download the latest Android SDK</a>
<a class="big_button" href="https://github.com/ChartBoost/client-examples/archive/master.zip">Download example projects</a>

---

(Integration instructions)[/documentation/android]

---

## Changelog

#### v3.1

- SDK is now an Interface instead of a Class
- New native interstitials: faster, less memory
- New native More-Apps page: faster, less memory, less network activity
- Asset caching: individual assets are cached & only downloaded if they don't exist in cache
- Cache expiration: cached interstitials automatically expire after 24 hours
- Multi orientation support: if your app works in both orientations, simply select both (landscape and portrait) in the dashboard
- No longer uses an activity to display the view (better performance)
- Handles tracking of cached interstitials properly
- Countless performance & stability upgrades
- New API methods:
-- cb.onCreate: Initialize Chartboost with cb.onCreate(Context, appID, appSignature, chartboostDelegate or null)
-- cb.startSession(), removed cb.install()
- New delegate methods:
-- didCacheInterstitial: called when an interstitial is successfully cached from the server, interstitial location identifier passed in
-- didCacheMoreApps: called when the more apps page is successfully cached from the server
-- shouldRequestInterstitialsInFirstSession: default is YES, you may override to NO if you don't want interstitials displayed until after the 2nd startSession (for compliance with Human Interface Guidelines)
