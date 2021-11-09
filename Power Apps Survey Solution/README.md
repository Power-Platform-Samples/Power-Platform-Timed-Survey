# Overview
Microsoft's Power Apps is a low-code development platform that enables you build enterprise applications (applications created for use within your organization not for consumer consumption) within minutes. But wait! Asides allowing you build applications for your business, Power Apps has other MAD skills.

With Power Apps, you can build applications that run on web, Android and iOS devices. Power Apps provides an easy to use drag-and-drop interface that allows you add different controls (check-box, choice field, buttons, drop-down, or text field), forms, and media (video, image, or audio files) into whatever application you are building. It also allows you store and connect to external data sources inside your app.

# Building our App from SharePoint
We would be connecting Power Apps to our SharePoint List which we created earlier. Here's how you can do that.
- On your SharePoint List, click on 'Integrate', then 'Power Apps', then 'Create an app'.

![](Images/powerapps-1.PNG)

- Give your app a name and click on 'Create'. I would  name mine "SurveySolution". After naming the app and clicking create, you would be redirected to Power Apps Studio where you can redesign your application to suite your neeeds.

![](Images/powerapps-2.PNG)

Employees at Microsoft have a busy time at work, so it is important we keep this application simple and easy to navigate. We would be editing our design so employees can submit their responses in less than 
SharePoint stores and displays information in the form of a list. A SharePoint List is a collection of data that you can share with your team members and people who you've provided access to.

Throuhgout this sample, we would be using the sharepoint list we would create now.

# Creating a SharePoint List
- Head over to sharepoint.com and sign in with your Microsoft account,
- Next click '+ New' and 'List' in the dropdown,
- Click on 'Blank List', fill in the details
    * Name: Give your list a name. I'll name mine - SurveySolutions,
    * Description: You could decide to add a description, but I'll keep mine blank,
    * Site Navigation: Ensure that
- Once you have completed this, click on 'Create'