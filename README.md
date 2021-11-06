# Overview
At Microsoft, we cherish and care about our employees. They are an integral part of Microsoft. They are Microsoft's greatest asset. At all times, we ensure that their voices are heard. To understand what needs to change within the organization, Microsoft surveys and speaks with its employees about the current state of work. They listen to the inputs, reviews, and suggestions of employees. This culture is one of the most surprising reasons why Microsoft's stock will keep rising. Would you love to embed this culture in your organization and get reviews from your employees at frequent intervals?

Microsoft's Power Platform can help make this happen. This sample showcases how you can integrate an automated employee review system in your organization using either Power Apps or Power Virtual Agents. Your automated system would share the survey with employees in your organization at the scheduled time and date, collect all responses, and upload them in real-time on SharePoint. From SharePoint, you can visualize the results to gain confirmed insights for growing your organization using Power BI.

In this sample, I would show you how to integrate this system into your organization's Teams tenant using either Power Apps or Power Virtual Agents and Power Automate.

# Prerequisites
Throughout this sample, we would be using SharePoint for storing our data. SharePoint enables you
-   Build intranet sites and create pages, document libraries, and lists.
-   Discover, follow, and search for sites, files, and people across your company.
-   Manage your daily routine with workflows, forms, and lists.
-   Sync and store your files in the cloud so anyone can securely work with you.

SharePoint stores and displays information in form of a list. It is a collection of data that you can share with your team members and people who you've provided access to.

Throughout this sample, we would be making use of a SharePoint list. First we need to create a SharePoint site. If you have already created one, you just need to create a list to store information.

# Creating a SharePoint Online Site
There are two types of SharePoint sites:
- Team sites enables team members create and edit content and collaborate on projects, events, or ideas. They are restricted to people in your Microsoft 365 Group. Each member of the group has the same permissions.
- Communication sites are relevant when you need to broadcast a message, tell a story or share content for viewing to a large audience. Behind the scene, just a few members are given permissions to create and contribute to content.

In this sample, we would create a Communication Site.

- Head over to sharepoint.com and sign in with your Microsoft account.
- Click on '+ Create site' and select 'Communication site'.
- Give your site a name and add a description if you wish to at this point. 
    Notice that as you type in the name of your site, it automatically creates a site address and confirms if it is available in your organization. You can also decide to pick another language convenient for you aside English.
- When completed, click 'Finish'. The result is as shown in the image below.

# Creating a SharePoint List
- Click on '+ New' and in the dropdown, click on 'List'.
- Click on 'Blank List' and give your SharePoint List a name. If you wish to, you can add a description or decide to leave that for later.
- Once you have completed this, click on 'Create'.
