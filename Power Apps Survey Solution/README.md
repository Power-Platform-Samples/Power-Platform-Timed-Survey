# Overview
Microsoft's Power Apps is a low-code development platform that enables you build enterprise applications (applications created for use within your organization not for consumer consumption) within minutes. But wait! Asides allowing you build applications for your business, Power Apps has other MAD skills.

With Power Apps, you can build applications that run on web, Android, and iOS devices. Power Apps provides an easy to use drag-and-drop interface that allows you add different controls (checkbox, choice field, buttons, drop-down, or text field), forms, and media (video, image, or audio files) into whatever application you are building. It also allows you store and connect to external data sources inside your app.

# Building An App from SharePoint
We would be connecting Power Apps to our SharePoint List which we created earlier. Here's how you can do that.
- On your SharePoint List, click on 'Integrate', then 'Power Apps', then 'Create an app'.

![](/Images/powerapps-1.PNG)

- Give your app a name and click on 'Create'. I would name it **"SurveySolution"**.

![](/Images/powerapps-2.PNG)

- You would be redirected to Power Apps Studio where you can redesign your application to suite your needs. The next screen would be like the image below.

![](/Images/powerapps-3.PNG)

Employees at Microsoft have a busy time at work, so it is important we keep this application as simple and easy to navigate as possible. We would be editing our design so employees can submit their responses in less than 20 seconds while navigating through 3 screens.

LET'S START RE-DESIGNING OUR APP!

# Redesigning our Power Apps Application
First thing we would do is change the theme of our application. This theme is too popular in Power Apps, we need something unique. To change the theme, go to 'Theme' at the top navbar and pick any theme of your choice. I would pick "Rose". Notice that immediately you pick a theme, the color of your application changes as shown below.

![](/Images/powerapps-4.PNG)

Now let's focus on our application! The first screen we want employees to interact with is the welcome screen with a clickable button "Get Started". 

To add a new screen, click on 'New screen' at the top and select 'Blank' as shown in the image below. Immediately you do, a new screen would be added to the application.

![](/Images/powerapps-5.PNG)

Now let's add a button to the new screen. To add a button, click on the '+ sign' in the right sidebar of the page and search for 'Button'. Click on it and it would automatically be added to the page.

I would prefer my button to be close to the bottom of the page, so I would drag it there as shown in the image below.

![](/Images/powerapps-6.PNG)

Next we need to edit the text of the button and add an action which would direct employees to a form on the next screen where they can fill in their response.

To edit the text, double click on the button and type in "Get Started". To add the action, click on the button and 

``` PowerFX
NewForm(EditForm1);Navigate(EditScreen1, ScreenTransition.None)
```

