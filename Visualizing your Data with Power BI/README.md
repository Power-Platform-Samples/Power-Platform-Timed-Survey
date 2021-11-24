# Overview
CONGRATULATIONS ON GETTING THIS FAR! By now you must have successfully built and connected your Power Apps application or Power Virtual Agent bot to SharePoint. All data collected from the responses of our employees is stored on SharePoint. Data is knowledge. Good data  allows organizations to more effectively determine the cause of problems. To be able to communicate business insights in a constructive manner, we need to make use of visualizations.

Power BI is a Data Visualization and Business Intelligence tool that converts data from different data sources including SharePoint to interactive dashboards and BI reports. It is a collection of software services, apps, and connectors that work together to turn your unrelated sources of data into coherent, visually immersive, and interactive insights. Power BI let's you easily connect to your data sources, visualize and discover what's important, and share that with anyone or everyone you want.

Power BI consists of several elements that all work together. In this sample, we would be focusing on 2 of them:
* Power BI service: Power BI service or Power BI online is a cloud-based service, or software as a service (SaaS) online. You can build dashboards that help you keep a finger on the pulse of your business. It’s designed for light report editing and collaboration.
* Power BI Desktop: Power BI Desktop is a desktop application that allows you connect, transform, and visualize data. You can conect to more than one different data source and combine them into a data model. You can build visuals, and collections of visuals which can be shared as reports with other people inside your organization.

In this section, I would show you how to visualize your data stored on SharePoint using Power BI Online or Power BI Desktop.

# Visualizing data with Power BI Online
Did you know that you can easily visualize your SharePoint data with Power BI in seconds? Yes I meant that. Let's learn how to do that. We start off by going back to our SharePoint List. By now, our list should have some more data in it after testing our Power Apps application and Power Virtual Agent bot.

Click on 'Integrate' in the top navbar of the screen, then 'Power BI' and 'Visualize the list' as shown in the image below.

![](/Images/sharepoint-7.PNG)

Immediately you do, Power BI Online opens up in a new window. If you haven't already, you would be prompetd to sign in. If you have signed in, your screen should be similar to the one in the image below.

![](/Images/powerbi-1.PNG)

Data visualizations like the ones in the image above should give us clear idea of what the information we are trying to pass across to our audience is and what it means. This makes the data more natural for the human mind to comprehend and therefore makes it easier to identify trends and patterns which would improve your organization. The visualization above though doesn't totally meet this criteria.

In this documentation, I would not show you how to work with Power BI. 😢😢 But I've got something for you. I would be sharing 3 links that would help you. Check out

- [Use visuals in Power BI](https://docs.microsoft.com/en-us/learn/modules/visuals-in-power-bi/)
- [Visualize data in Power BI](https://docs.microsoft.com/en-us/learn/paths/visualize-data-power-bi/)
- [Data analysis in Power BI](https://docs.microsoft.com/en-us/learn/paths/perform-analytics-power-bi/)

Take some time to explore the content of these links. Now let's see how you can visualize your data with Power BI Desktop, just in case you are more convenient with the desktop version.

# Visualizing data with Power BI Desktop
Have you tried visualizing data with Power BI Desktop? You should definitely try it out. If you haven't already, please [download](https://powerbi.microsoft.com/en-us/desktop/) Power BI Desktop. In this section, I would show you how to connect and visualize data in your SharePoint List using Power BI Desktop. If you have installed Power BI Desktop already, open it.

![](/Images/powerbi-2.PNG)

Click on 'Get data'. In the Get Data dialog, search for "SharePoint" and select 'SharePoint Online List'. Click 'Connect' and input your SharePoint Online site that contains your list in the "Site URL". Next click 'Ok'.

You might see a SharePoint access screen like the one in the image below. If you see it, select 'Microsoft Account' and click 'sign in' to connect to your Microsoft 365 account. Once signed in, click 'Connect'.

![](/Images/powerbi-3.PNG)

Not to worry if your screen didn't look like the one above. It should look like the one below.

![](/Images/powerbi-4.PNG)

Select the specific SharePoint List you want to connect to and click 'Transform Data'. The goal of transforming this data first is to discard unnecessary columns.

![](/Images/powerbi-5.PNG)

Select all colunms that are not relevant and delete. You should be left with 5 columns (Title and the columns for the 4 questions). Next click 'Close and Apply'. When you do, your data would be loaded into Power BI Desktop.

![](/Images/powerbi-6.PNG)

But wait! What if you already connected your SharePoint list and new responses are submitted, does that mean you have to go through this process again? Well I've got some good news for you....😁🙌🎉

You don't have to go through this process again. Here's what you need to do.

Just click on 'Home' in the top navbar and then 'Refresh' under Queries. Immediately you do, your visualization would check if there are new results and update accordingly.

To learn about building presentable visuals, reports, and dashboards, check out the recommended learning resources above and the ones below too:
- [Get started building with Power BI](https://docs.microsoft.com/en-us/learn/modules/get-started-with-power-bi/)
- [How to build a simple dashboard](https://docs.microsoft.com/en-us/learn/modules/build-simple-dashboard/)