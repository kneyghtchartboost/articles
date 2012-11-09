<h3 id="ios">iOS SDK</h3>

Developers need to integrate our iOS SDK in their app code. This is the way we can track their impressions and installs. The instructions to integrate the SDK can be found http://www.chartboost.com/support/sdk

Developers need to create an app from the dashboard to generate an app ID. This is the way we can track the performance of the campaigns associated to each app.

<h3 id="min">What's the minimum OS version you support?</h3>

We are only supporting 4.3 and above for iOS now due to the very small amount of users who still have 3.X and Apple's plans to only let you target 3.X.  However, if you are still targeting 3.0, you can simply not reference our SDK for users who have 3.X

<h3 id="proper"How do I know if I've integrated properly?</h3>

*You can test on device or simulator, though we suggest using a simulator at first.*

In the Apps ➔ Overview page, if an app has a green "SDK" button next to the title, it indicates the game has been successfully integrated.  You should also create a test campaign to ensure the ads are serving and tracking correctly.

To create a test campaign:
1. Go to Campaigns ➔ Add Campaign ➔ Publish in the Network (even if you don't intend to publish in the marketplace, this is the best and easiest way to make sure that you're 100% integrated)
2. Insert a name for the campaign (indicating it's a test)
3. Select the game you've integrated to run the campaign in
4. Click save

What you're testing for:
- Do the ads serve in the game you've integrated the SDK into?
- Are the impressions recording in your campaign analytics?
- If you click on the ad, does the click record in your campaign analytics?
- If you download, then open the game that was being promoted, does the install record in your campaign analytics?

**If your app is already live on the store with integration, you can go to App ➔ Analytics, select the app and verify that the all installs and boot-ups are accurate.  If so, the integration is successful.**

<h3 id="appid"Where do I find App ID and App Signature?</h3>

Integrating the SDK requires an APP_ID and APP_SIGNATURE.  To get the ID and SIGNATURE, add the app to your Chartboost.com account by going to Apps > Add App.  Fill in the required fields and click 'Save.'  The Apps Overview page will appear.  On this page, click the 'App IDs' link under the name of the app you added, and a pop-up will appear with the App ID and App Signature needed for integration.

<img src="http://chartboost.s3.amazonaws.com/help_assets/App%20ID.jpg"/>
