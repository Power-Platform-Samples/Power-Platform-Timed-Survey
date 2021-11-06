# Overview
At Microsoft, we cherish and care about our employees. They are an integral part of Microsoft. They are Microsoft's greatest asset. At all times, we ensure that their voices are heard. To understand what needs to change within the organization, Microsoft surveys and speaks with its employees about the current state of work. They listen to the inputs, reviews, and suggestions of employees. This culture is one of the most surprising reasons why Microsoft's stock will keep rising. Would you love to embed this culture in your organization and get reviews from your employees at frequent intervals?

Microsoft's Power Platform can help make this happen. This sample showcases how you can integrate an automated employee review system in your organization using either Power Apps or Power Virtual Agents. Your automated system would share the survey with employees in your organization at the scheduled time and date, collect all responses, and upload them in real-time on SharePoint. From SharePoint, you can visualize the results to gain confirmed insights for growing your organization using Power BI.

In this sample, I would show you how to integrate this system into your organization's Teams tenant using either Power Apps or Power Virtual Agents and Power Automate. For this sample, we would be using the name "SurveySolution" to identify our solution.

# Prerequisites
In this sample, we would be using SharePoint for storing our data. SharePoint allows us
- Build intranet sites and create pages, document libraries, and lists.
- Manage daily routine with workflows, forms, and lists.
- Sync and store your files in the cloud so anyone can securely work with you.

SharePoint stores and displays information in form of a list. It is a collection of data that you can share with your team members and people who you've provided access to.

Throughout this sample, we would be making use of a SharePoint List. But first we need to create a SharePoint site. If you have already created one, you just need to create a list to store information.

# Creating a SharePoint Site
There are two types of SharePoint sites:
- Team site enables team members create and edit content and collaborate on projects, events, or ideas. They are restricted to people in your Microsoft 365 Group. Each member of the group has the same permissions.
- Communication site is relevant when you need to broadcast a message, tell a story or share content for viewing to a larger audience in our organization. Behind the scene, just a few members are given permissions to create and contribute to content. In this sample, we would create a Communication Site.

- Head over to sharepoint.com and sign in with your Microsoft account.

![sharepoint-1](https://user-images.githubusercontent.com/59547637/140617473-ef8833d9-e5e0-4f58-bbbf-b6ac08cef1f4.PNG)

- Click on '+ Create site' and select 'Communication site'.
- Give your site a name and add a description if you wish to at this point. Notice that as you type in the name of your site, it automatically creates a site address and confirms if it is available in your organization. You can also decide to pick another language convenient for you aside English.
- When completed, click 'Finish'. The result is as shown in the image below.

![sharepoint-2](https://user-images.githubusercontent.com/59547637/140617484-6d6d4964-c382-442a-b6fd-daf3abe04ef4.PNG)

# Creating a SharePoint List
- Click on '+ New' and in the dropdown, click on 'List'.
- Click on 'Blank List' and give your SharePoint List a name. If you wish to, you can add a description or decide to leave that for later.
- Once you have completed this, click on 'Create'. You would be redirected to a new page which looks like the one in the image below.

![sharepoint-3](https://user-images.githubusercontent.com/59547637/140617532-7d1d4257-cc37-4997-8e5f-a15e30960189.PNG)

# Populating our SharePoint List
Now it's time to populate our sharepoint list with the required columns for the solution we are building. But first, let's take a look at what our solution would look like.

In our survey, we want employees from different departments in our organization to anonymously tell us the state of things within their department. Their ratings on a scale of 0 to 5, 0 for lowest and 5 for highest is based on the following questions:
* Do you feel good about your current work/life balance?
* Do you feel like a true part of your team?
* Do you feel like you are heading the right direction as a team?
* Do you feel energized about your job?

Our database needs to have a column for their department and each column for each question.

- To add the department column, click on the first column 'Title'. Go to 'Column Settings', then 'Rename' and change the name of the column from Title to Department.
- To add a column for the each question, click on '+ Add Column', then 'Choice'. 
- In the sidebar that pops out fill in the following details:
* Name: Use each question as the name of each column.
* Choices: Add 0 to 5 as the options. 
* Under 'More Options', change 'Display choices using' from Drop-Down Menu to Radio Buttons. Also make sure the section 'Require that this column contains information' is toggled to Yes so employees do not skip any of the questions.
- Click on 'Save' to save the column.
- Replicate this process for the other questions. At the end, your SharePoint list should look like the one in the image below.

Now it's time to start developing an interface for our solution! THe frst 2 folders shows how you can bring this to life as a Power Apps application for employees to interact with or as a virtual agent using Power Virtual Agents and Power Automate.

In either case, the response of each employee is automatically updated on our SharePoint List. The last folder shows us how we can visualize the response using either Power BI Online Service or Power BI Desktop.

TIME TO BRING THIS TO LIFE! 💃🏾 🕺🏾 - 👩🏾‍💻 👨🏾‍💻