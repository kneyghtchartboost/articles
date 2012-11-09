<a name="glossary"></a>

**Getting Started: Chartboost Glossary** 

If you're new to mobile advertising and distribution, this is a good place to start learning the basic terminology!

**Campaign Basics**

Advertiser: A developer who pays (or barters) for promotion of his ads.

Publisher: A developer who runs ads in his games in order to make money (or trades).

Cross-promotion: A campaign where you show ads in one game that promote another one of your games. In this case, you are both the advertiser and the publisher.

Direct Deal: A campaign where you have made a deal directly with another developer to buy, sell, or trade traffic. You can be an advertiser or a publisher.

Network: A campaign that runs through Chartboost’s game-only ad network, which pulls ads from a pool of advertisers and distributes them to many publishers. You can be an advertiser or a publisher.

Cost per Install Campaign (CPI): A campaign where you pay for each install your app receives from Chartboost ads.

Cost per Click Campaign (CPC): A campaign where you pay for each click your ad receives.

**Anatomy of an Ad**

Interstitial: A full-screen ad that pops up either when the app is booted up or at some point between bouts of gameplay. This is the only size of ad unit that Chartboost serves.

Creative/Asset/Ad Unit: The image that you upload as an advertiser to be shown when ads for your game pop up. Find instructions for making creatives [here](http://www.chartboost.com/support/assets#advertisers).

Call to Action (CTA): A button, graphic, or text on an ad creative that prompts a user to download the advertised app (ie “Download now on the App Store”). If you are advertising an iOS app, be sure to follow Apple’s CTA Guidelines [here](http://www.chartboost.com/support/assets#guidelines). 

A/B Testing: The process of uploading and running multiple creatives to see whether one performs better than the other (you can compare colors, CTAs, images, etc).

Frame: The image that surrounds ads that are served in your game as a publisher. Adding a frame allows you to customize the look/feel of ads in your app, but is optional. Find instructions [here](http://www.chartboost.com/support/assets#publishers).

Close Button: An integral part of the frame, this button allows users to close an interstitial and is typically displayed as an “X” in the upper corner of a frame.

**Campaign Performance**

Impression: An impression is counted each time an ad is shown to a user.

Click: A click is counted each time a user taps an ad that is shown to them.

Install: An install is counted every time a user launches an app for the first time that they downloaded after clicking an ad.

Impressions/Clicks/Installs Delivered: Metrics for a publishing campaign (ie, the campaign shown to users in your app delivered 1200 installs to advertisers in the network).

Impressions/Clicks/Installs Received: Metrics for an advertising campaign (ie, your network advertising campaign received 1200 new installs of your app).

All Installs: We track all your new users, not just the ones coming from Chartboost. This number includes all users that the Chartboost server is seeing for the first time, regardless of where they came from.

Click-Through Rate (CTR): The percentage of the time that a user clicked an ad after an impression was served to them. CTR = Clicks/Impressions

Install Rate (i-rate): The percentage of the time that a user downloaded an app after they clicked on an ad for it. i-rate = Installs/Clicks

eCPM: The effective cost (if you’re an advertiser) or revenue (if you’re a publisher) per thousand impressions served. Also the value that the Chartboost network uses to rank campaigns. eCPM = Money/Impressions*1000 

**Tech Stuff**

SDK: Software Development Kit. Code that we have created that is integrated into your application so that we can serve ads and run analytics for your campaign.

Unity Plugin: If you used Unity to develop your game, you can use this [plugin] (http://prime31.com/unity/#ChartBoost) to integrate with Chartboost.

**Direct Deals**

Direct Deals Marketplace: A “social network” for game developers to meet and make direct deals. You need to meet a few requirements to have access to the direct deals marketplace; apply under the Marketplace tab above. Being in the direct deals marketplace is NOT a requirement to do direct deals - you can still do direct deals with partners you’ve met or talked to outside of Chartboost, just email us and let us know to connect you.

Direct Deal Profile: This is your public facing persona for your company on the Direct Deals Marketplace. This is a helpful place to list your apps, demographics, and what kind of campaigns you are interested in running (Advertising/Publishing).

Direct Invoicing: When creating a direct deal, choose Direct Invoicing if you and your partner will be handling all money transactions yourselves. Chartboost will track your impressions, clicks, and installs, but tracking money is up to you. The publisher keeps 100% of the money paid by the advertisers. Also choose this option if there is no money changing hands.

Chartboost Invoicing: Choose this option if you want Chartboost to track and handle payment and invoicing. In this case, the publisher keeps 90% of the money paid by the advertiser.

**Money Stuff**

Balance: How much you have left to spend as an advertiser. If this number is negative, you won’t be able to run any campaigns until you deposit more money in your account.

Earnings: How much you have earned as a publisher with Chartboost.

<a name="overview"></a>

1. Create an account at Chartboost.com

2. Add the app you want to use with Chartboost by going to Apps -> Add App

3. Once you've added the app and clicked save, the App ID and App Signature will be available in the dashboard which the development team will need to integrate the SDK. The SDK can be found at https://chartboost.com/support/sdk

4. Test the integration. You can do this by installing our Test Example Project located [here](https://github.com/ChartBoost/client-examples). It's a ready to go project you can use to ensure that you have integrated correctly. Please remember to replace the existing App ID and App Signature in the project with your own.


5. If you're interested in publishing interstitials, add a custom frame to your app under Apps -> Your App Name -> Promote other apps (note: a custom frame is not required, but we do recommend it).

6. If you're interested in advertising your app, add ad units under Apps -> Your App Name -> Promote this app.  Also, add funds to your account using PayPal or wire transfer under 'Add Funds' in the left sidebar.

7. Once your update to the app has gone live in the App Store/Marketplace, it's time to start a campaign!  Just go to Campaigns -> Add a Campaign and choose the type of campaign you want to start. Types of campaigns you can run are:
  + Cross-Promotion: promoting among your own apps for free
  + Advertising in the Network: advertise your app across our network of games on a CPI or CPC basis
  + Publish in the Network: show ads in your app for those advertising and earn revenue

8. Now that your campaigns are running, get reports on their performance under Campaign -> Analytics.  You can also see impressions, clicks and installs broken down by app under Apps -> Analytics.

<a name="campaigns"></a>

**What do the different campaigns do?**

**Publish in the Network** - Promote other developers' apps. You should upload a custom frame to make the ad feel like a recommendation from you.

**Advertise in the Network** - Advertise in other developers' apps. For this, you will want to upload a custom ad unit.

**Cross Promotion** - This is a way to promote your own apps within other apps you have created. Your users are your best audience for your new apps.

**Direct Deals** - Partner directly with other developers to make deals as either an advertiser or a publisher. When you have volume, you have the power to make deals.

**More Apps Page** - These pages are usually linked from the homescreen of an app and can display any of the above campaigns, or a specific app.

<a name="cost"></a>


**What does it cost to use Chartboost?**

Cross-promotion of your own games and any deals you make directly with other developers are free to do on the Chartboost platform.  Advertising in our network of games works on a bidding basis with either CPI or CPC type campaigns.  When you publish the advertising for our network, we share 70% of the revenue with developers.

<a name="compatibility"></a>

**What coding languages are you compatible with?**

A: We are currently compatible with Objective-C, Java, and Unity (through the plug-in located [here](http://www.prime31.com/unity/#ChartBoost)).

<a name="cross promo"></a>

**How do I start a cross-promotional campaign?**

To start cross-promoting internally- say, to advertise to users of your Super-Popular App that they should try your Awesome New App- follow these steps to get started.

1. Add your Super-Popular App under the "App" tab at the top of your dashboard. If you want, you can upload a custom frame under "Promote Other Apps"- design them according to our [publishing creative guidelines](http://www.chartboost.com/support/assets#publishers).
2. Add Awesome New App as an app, and add creative for it under "Promote this App" according to our [advertising creative guidelines](http://www.chartboost.com/support/assets#advertisers).
3. [Integrate the Chartboost SDK](http://www.chartboost.com/support/sdk) into Super-Popular App. If you want to track installs or publish in Awesome New App in the future, you should also integrate the SDK into it as well. [Test the integration](https://chartboost.tenderapp.com/kb/ios-integration/how-do-i-know-if-ive-integrated-properly) and submit your update to the app store.
4. Create a cross-promotional campaign under the Campaign tab at the top of the dashboard, with whatever logic/frequency settings you want. Save the campaign and it will start running (once your update is live in the app store, that is).

<a name="don't have games"></a>

**I don't have any games. Can I still use Chartboost?**

Yes! If you are a developer who makes awesome apps but they are not games, you can still use Chartboost. 

You can use Chartboost for internal cross promotion for your portfolio of apps, or setting up Direct Deals with partners you already know. You can also publish ads for the network to monetize your app.

However, as a non-game, you cannot advertise in our network or view the Direct Deals Marketplace.

<a name="SDK lights"></a>

**What are those 2 icons next to the SDK Integration icon?**

After you've integrated our SDK and set up the Chartboost dashboard, you'll notice there are two icons next to the green SDK light. Listed below is the representation of each light and what it means:

From left to right:

1. SDK Light - If lit, our SDK has successfully integrated with your App.
2. Frame Light - If lit, it means you have successfully uploaded a custom frame.
3. Creative Light - If lit, it means you have successfully uploaded a custom creative.

Please utilize the following image for visual aid:

![3_Lights.jpg](/help/assets/1a10f78a5868cd3dc51b6c9a489902fe0290e2c1/3_Lights_normal.jpg)

<a name="no ads"></a>

**I can't see any ads in my app. Is something wrong?**

Please make sure you've followed the ['Getting Started' Guide.](http://help.chartboost.com/getting-started) After doing so, you may want to make your device a Test Device (**ADD REDIRECT URL HERE**). Test devices ignore all campaign logic - For example, if you set a limit of one ad per hour, or set specific countries to show ads in, we ignore all that. Instead, we simply serve your device as many ads as possible. This is meant for testing purposes.

<a name="callbacks"></a>

**What are callbacks and how can I add them?**

Callbacks are used as a way to be notified when a user clicks an ad and/or installs an app. It's a great way to get real-time data in your server for your own tracking and analytics. You can add a callback URL by navigating to your campaign, choosing 'Advanced Settings,' and then 'Show Callbacks.' Please see the images below for visual aid.

<img src="http://chartboost.s3.amazonaws.com/help_assets/Callbacks%20Step%201.jpg" />

<img src="http://chartboost.s3.amazonaws.com/help_assets/Callbacks%20Step%202.jpg" />


<a name="priorities"></a>

**What are priorities and how do they work?**

Priorities work as such - We work our way from the Highest campaign down to Low. Whichever campaign is set to "Highest", we serve as many ads as possible from that campaign until we cannot serve any more. From there, we drop down to the next priority (High) and serve as many ads from there as possible. So forth and so on. 

For example, if you have a Publish in Network campaign set to "Highest" and a Cross Promo campaign set to "High", we will show as many ads as possible from our network and then, when there are no more ads to show, we will drop down to the next priority (in this case, "High") and then show the Cross Promo ad.
