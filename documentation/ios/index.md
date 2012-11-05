
The Chartboost iOS SDK is the cornerstone of the Chartboost network. It
provides the functionality for showing ads and  more apps pages, and tracking
analytics and in-app purchase revenue.


### Basic integration

Integrating Chartboost takes two easy steps:

 1. Drop the Chartboost folder into your Xcode project.
    
    Ensure you are linking against the following frameworks: `QuartzCore`,
    `SystemConfiguration`, `StoreKit`, `CoreGraphics`, and `GameKit`.

 2. Instanciate with the Chartboost SDK in your
    `application:didFinishLaunchingWithOptions:` method, like this:
    
    ```objc
    #import "Chartboost.h"
    
    - (BOOL)application:(UIApplication *)application
      didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
        
        Chartboost *cb = [Chartboost sharedChartboost];
        cb.appId = /* your app id goes here */;
        cb.appSignature = /* your app signature goes here */;
        [cb startSession];
        [cb showInterstitial];
        
        return YES;
    }
    ```


### Advanced topics

<a class="article_box" href="/documentation/ios/caching">Caching</a>

<a class="article_box" href="/documentation/ios/delegates">Delegate methods</a>

