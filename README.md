# Overview
At Microsoft, we cherish and care about our employees. They are an integral part of Microsoft. They are Microsoft's greatest asset. At all times, we ensure that their voices are heard. To understand what needs to change within the organization, Microsoft surveys and speaks with its employees about the current state of work. They listen to the inputs, reviews, and suggestions of employees. This culture is one of the most surprising reasons why Microsoft's stock will keep rising. Would you love to embed this culture in your organization and get reviews from your employees at frequent intervals?

Microsoft's Power Platform can help make this happen. This sample showcases how you can integrate an automated employee review system in your organization using either Power Apps or Power Virtual Agents. Your automated system would share the survey with employees in your organization at the scheduled time and date, collect all responses, and upload them in real-time on SharePoint. From SharePoint, you can visualize the results to gain confirmed insights for growing your organization using Power BI.

In this sample, I would show you how to integrate this system into your organization's Teams tenant using either Power Apps or Power Virtual Agents and Power Automate.

# Prerequisites
Throughout this sample, we would be using SharePoint for storing our data. SharePoint enables you
-	Build intranet sites and create pages, document libraries, and lists.
-	Discover, follow, and search for sites, files, and people across your company.
-	Manage your daily routine with workflows, forms, and lists.
-	Sync and store your files in the cloud so anyone can securely work with you.

SharePoint stores and displays information in the form of a list. A SharePoint List is a collection of data that you can share with your team members and people who you've provided access to.

Throuhgout this sample, we would be using the sharepoint list we would create now.

# Creating a SharePoint List
- Head over to sharepoint.com and sign in with your Microsoft account,

![sharepoint-1](https://user-images.githubusercontent.com/59547637/140572085-64bef340-3b3d-4ff0-980c-c040e1160842.PNG)

- Next click '+ New' and 'List' in the dropdown,
- Click on 'Blank List', fill in the details
    * Name: Give your list a name. I'll name mine - SurveySolutions,
    * Description: You could decide to add a description, but I'll keep mine blank,
    * Site Navigation: Ensure that
- Once you have completed this, click on 'Create'
