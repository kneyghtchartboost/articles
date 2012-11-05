<a class="big_button" href="https://chartboost.com/support/sdk_download/3.1.1?os=ios">Downloads the latest iOS SDK</a>

---

## Changelog

#### v3.1.1

- Stability improvements for apps with over 300mb of bundled assets
- Fixed rare visual glitch where interstitial positions itself incorrectly
  relative to status bar after app rotation

#### v3.1

- Added support for the iOS 6 App Sheet so your users can download apps without
  ever leaving your app! You must include StoreKit.framework for access to the
  App Sheet. We are rolling out this feature in phases, apply for access via
  [bizdev@chartboost.com](mailto:bizdev@chartboost.com).
- More apps status bar fixed, now auto-adjusts position when status bar is
  visible
- Fixed rare crasher in CBCrypto
- Note: This version and all versions in the future are compatible with iOS
  version 4.3 and higher ONLY (armv7 & armv7s). For armv6 compatibility,
  download SDK v3.0.7 above.

#### v3.0.7 - [Download this version][3.0.7]

REQUIRED: You must include AdSupport.framework for access to the
identifierForAdvertising

- Added compatibility with Xcode 4.5 & armv7s. This SDK includes armv6, armv7,
  and armv7s
- Fixed shouldRequestInterstitialsInFirstSession delegate method; now requests
  interstitials only after 2nd startSession call
- Internal API upgrades

[3.0.7]: https://s3.amazonaws.com/chartboost/sdk/3.0.7/ChartBoostConnect.tar.bz2
 
#### v3.0.6

- Automatic interstitial caching now uses a version fallback if your app does
  not include CFBundleShortVersionString in the info.plist. For best
  interstitial caching, add CFBundleShortVersionString key & value to your
  info.plist.

#### v3.0.5

- Fixed rare crash in web image caching library

#### v3.0.4

- Added SDK support for targeting Wi-fi devices

#### v3.0.3

- Removed automatic removal of interstitials & more apps view when
  backgrounding app

#### v3.0.2

- Improves click tracking in race conditions
- Fixes issue where cached ads appear during backgrounding
- Fixed JSON crasher in CB Analytics

#### v3.0.1

- Improved compatibility with iOS version 4.0 - 4.2

#### v3.0

- Mandatory updates:
    - Delegate methods now return location strings (no longer pass in a view)
      -- i.e. didFailToLoadInterstitial will pass in the specific location
      identifier that failed
    - Removed methods: loadInterstitial, install -- now use showInterstitial,
      startSession
    - Requirement: rename ChartBoost class to Chartboost (lowercase b, no
      camelCase) Feeling hardcore? Run this bash command in your project
      directory to update camelcase ChartBoost in all your files:
      
      ```bash
      for ext in '*.m' '*.h' '*.c' '*.mm'; do find . -name "$ext" -exec sed -i '' 's/ChartBoost/Chartboost/g' '{}' \; ; done
      ```

- New native interstitials: faster, less memory
- New native More Apps page: faster, less memory, less network activity
- Asset caching: individual assets are cached & only downloaded if they don't
  exist in cache -- all assets stored in caches folder so the OS handles memory
  appropriately
- Cache expiration: cached interstitials automatically expire after 24 hours
- Multi orientation support: if your app works in both orientations, simply
  select both (landscape and portrait) in the dashboard
- Orientation override: SDK detects orientation using the statusbar location,
  you may override this detection
- UDID replacement: iOS 6 compatible
- New delegate methods:
    - didCacheInterstitial: called when an interstitial is successfully cached
      from the server, interstitial location identifier passed in
    - didCacheMoreApps: called when the more apps page is successfully cached
      from the server
    - shouldRequestInterstitialsInFirstSession: default is YES, you may
      override to NO if you don't want interstitials displayed until after the
      2nd startSession (for compliance with Human Interface Guidelines)
- Version notifications: if a new version of the SDK is released, you'll get
  a version notification in the Xcode console if current device is iPhone
  Simulator
- Bundle assets: you may include frame & cross promotion assets into your
  binary
- Bug fixes:
    - Displaying interstitial no longer fails when there is no appDelegate
      window property
    - Fixed memory leaks
- SDK supported - coming soon to the dashboard:
    - Interstitial animations: four, configurable from the dashboard
    - Retina support for interstitials & more apps
    - New cell types: regular, featured, webview

#### v2.9.2 - [Download this version][2.9.2]

Improvements to purchase and event tracking, fixed meta dictionary leak

[2.9.2]: https://s3.amazonaws.com/chartboost/sdk/2.9.2/ChartBoostConnect.tar.bz2


