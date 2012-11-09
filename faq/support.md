<a href="#compatibility" name="compatibility">Compatible coding languages</a>

**What coding languages are you compatible with?**

A: We are currently compatible with Objective-C, Java, and Unity (through the plug-in located [here](http://www.prime31.com/unity/#ChartBoost)).

<a href="#noads" name="noads">"I can't see any ads in my app."</a>

**I can't see any ads in my app. Is something wrong?**

Please make sure you've followed the ['Getting Started' Guide.](http://help.chartboost.com/getting-started) After doing so, you may want to make your device a Test Device (**ADD REDIRECT URL HERE**). Test devices ignore all campaign logic - For example, if you set a limit of one ad per hour, or set specific countries to show ads in, we ignore all that. Instead, we simply serve your device as many ads as possible. This is meant for testing purposes.

<a href="#callbacks" name="callbacks">Callbacks</a>

**What are callbacks and how can I add them?**

Callbacks are used as a way to be notified when a user clicks an ad and/or installs an app. It's a great way to get real-time data in your server for your own tracking and analytics. You can add a callback URL by navigating to your campaign, choosing 'Advanced Settings,' and then 'Show Callbacks.' Please see the images below for visual aid.

<img src="http://chartboost.s3.amazonaws.com/help_assets/Callbacks%20Step%201.jpg" />

<img src="http://chartboost.s3.amazonaws.com/help_assets/Callbacks%20Step%202.jpg" />


<a href="#priorities" name="priorities">Priorities</a>

**What are priorities and how do they work?**

Priorities work as such - We work our way from the Highest campaign down to Low. Whichever campaign is set to "Highest", we serve as many ads as possible from that campaign until we cannot serve any more. From there, we drop down to the next priority (High) and serve as many ads from there as possible. So forth and so on. 

For example, if you have a Publish in Network campaign set to "Highest" and a Cross Promo campaign set to "High", we will show as many ads as possible from our network and then, when there are no more ads to show, we will drop down to the next priority (in this case, "High") and then show the Cross Promo ad.

____________________ DUPLICATED ________________________

<a href="#end" name="end">Something important End</a>

<a href="/legal/terms#end" name="end">Legal End</a>
