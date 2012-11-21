
The Chartboost iOS SDK is the cornerstone of the Chartboost network. It
provides the functionality for showing ads and  more apps pages, and tracking
analytics and in-app purchase revenue.

Use requirements:
- Apps must be compiled with iOS base SDK v6.0 or higher (may still target 4.3+)
- Runs only on devices with iOS version 4.3 or higher (for 4.0 compatibility, get v3.0.7)
- Must weak-link AdSupport.framework in your app for iOS 6 compatibility (select "Optional")


### Basic integration

Integrating Chartboost takes two easy steps:

 1. Drop the Chartboost folder into your Xcode project.
    
    Ensure you are linking against the following frameworks: `QuartzCore`,
    `SystemConfiguration`, `CoreGraphics`.

    Additionally, ensure you are weak-linking to the `AdSupport` and `StoreKit` frameworks.

 2. Initialize Chartboost in your
    `applicationDidBecomeActive` method, like this:
    
    ```objc
    #import "Chartboost.h"
    
    - (void)applicationDidBecomeActive:(UIApplication *)application        
        Chartboost *cb = [Chartboost sharedChartboost];
        
        cb.appId = "YOUR_CHARTBOOST_APP_ID";
        cb.appSignature = "YOUR_CHARTBOOST_APP_SIGNATURE";
        
        // Begin a user session
        [cb startSession];
        
        // Show an interstitial
        [cb showInterstitial];
        
    }
    ```

### Advanced topics

<a class="article_box" href="/documentation/ios/caching">Caching</a>

<a class="article_box" href="/documentation/ios/analytics">Analytics</a>

<a class="article_box" href="/documentation/ios/delegation">Delegate methods</a>

