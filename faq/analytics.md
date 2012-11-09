<h3 id="creativetesting">Advertisers - A/B Testing Creatives</h3>

You should download the sample .csv file [here](http://dl.dropbox.com/u/41402639/tender%20analytics%20draft.xlsx)

The first sheet of the CSV is what the raw data will look like if you have exported all of the campaign data with every group option deselected. The next sheets are comprised of pivot tables using the original data.

We can tell how well a creative is performing by the Click Through Rate (CTR). CTR is the clicks divided by the number of impressions. 

In the AB Creatives tab, "War Creative 2" in the War Horse Campaign on iOS performs slightly better than the "War Horse 1" creative. For that campaign, the advertiser should use the creative with the highest CTR to improve overall performance.

<h3 id="advertising">Advertisers - How to Decide Who to do Direct Deals With</h3>

You should download the sample .csv file [here](http://dl.dropbox.com/u/41402639/tender%20analytics%20draft.xlsx)

The first sheet of the CSV is what the raw data will look like if you have exported all of the data when you have deselected all of the grouping options. The next sheets are comprised of pivot tables using the original data.

When you're looking to acquire users, you want to market to the users with the best CTR, Install Rate, and a high eCPM (it means their users like you). In the Direct Deal sheet, you can see how the eCPM varies by app within each campaign. 

Pretty Pony should look into making a Direct Deal with Jump! Higher! because they have a great CTR, I-Rate, and eCPM. It's advantageous for both sides to have the guaranteed traffic.

In the War Horse Android Campaign, our advertiser might consider doing a Direct Deal with Fish in a Tank because of their great install rate. 

For War Horse's iOS campaign, no app is performing amazingly, so it probably isn't worth their time to seek a Direct Deal Partner for that app.

<h3 id="appfiltering">Publishers - How to Decide What Apps to Filter</h3>

Chartboost allows you to export your campaign data by app, so you can see which ads are making you money. Using this data, you can determine whether there are any games that don't resonate well with your audience, and that perhaps you don't want to run ads for.

Your users must click the ads and in some cases download the apps for you to make money, so if users aren't clicking and downloading from an ad then you might consider filtering it out. It's nothing personal; some game audiences just don't overlap.

To run this analysis, you'll need a copy of Microsoft Excel.

1. Go to Campaigns > Analytics. Select the campaign you want to analyze and the timeframe you'd like to look at. The past week is a good amount of time since it will give a reasonable amount of data but it's recent enough to be highly relevant.

2. Change "Group by Campaign" to "Group by App." This will give you all data broken out by app promoted.

   ![Chartboost.jpg](/help/assets/ea7f51f34f325b19807d20701709cd48846b1c2a/Chartboost_normal.jpg)

3. Click "Refresh" and wait for analytics to load, then click "Export Table to CSV." A .csv file will be downloaded to your computer. Open this file in Excel.

4. Open the data in a pivot table (select all of the data in the sheet, then open Data > Pivot Table). Add "To App Name" as the rows, and sum of impressions, sum of clicks, sum of impressions, and sum of earned to the values.

   ![Screen_Shot_2012-03-08_at_3.23.39_PM.jpg](/help/assets/5dc1abbc635bd10ef7dbe91fe1f4ad640f0667c5/Screen_Shot_2012-03-08_at_3.23.39_PM_normal.jpg)

5. Calculate the eCPM in column F. The formula is earned/impressions * 1000, so in this case you can use =E5/B5 * 1000 in cell F5 and then extend that into the rest of the column. You can format this whole column as currency to help with readability. 

6. eCPM is the most important, but you may also want to consider the click-through rate (clicks/impressions) and the install rate (installs/clicks). Not all apps track installs, so don't be alarmed if some show 0 installs.

7. Your average overall eCPM will be at the bottom right of your new table. Consider filtering out apps with a considerably lower eCPM in order to optimize your campaign. (One handy way to find these is to copy this pivot table into another worksheet and sort by eCPM.)

8. For apps you are thinking about filtering, think about the share of impressions they serve you. If someone is a tiny bit below your average eCPM but is serving a large percentage of your impressions, you may want to keep them. If you filter too many impressions, you might have problems filling your ad inventory. On the other hand, it's probably not worth it to filter a whole bunch of apps with only a handful of impressions.

Now go forth and filter wisely!

<h3 id="performance">Publishers - How can I improve my performance?</h3>

As a publisher, it's wise to keep an eye on your analytics to make sure you are filtering out apps that don't perform well in your app. You can find out about filtering apps [here](https://chartboost.tenderapp.com/kb/exported-data/publishers-how-to-decide-what-apps-to-filter).

Our network averages a click through rate of 12%. If you are finding that you are consistently delivering below this, it might be for one of the following reasons:

1. Where are you showing the ad? If you are using locations other than bootup, we generally do see lower CTRs than on bootup. You might consider showing an ad on bootup as well as at a post game screen.

2. Are you using a custom frame? Try adding a frame that makes the ad unit feel like a recommendation rather than an ad. There are some hints on Chartboost's (assets page)[http://www.chartboost.com/support/assets]

3. Are you cacheing ads? If so, both your eCPM and CTR will be depressed. Currently, we count an impression on the GET call, not the SHOW call. If you are both caching and using multiple locations, you are probably calling GET one more time than you are actually calling SHOW - so your reported impressions is always higher than your actual.
