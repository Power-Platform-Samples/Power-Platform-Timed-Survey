# Overview
Microsoft's Power Apps is a low-code development platform that enables you to build enterprise applications (applications created for use within your organization not for consumer consumption) within minutes. But wait! Asides from building applications for your business, Power Apps has other MAD skills.

With Power Apps, you can build applications that run on the web, Android, and iOS devices. Power Apps provides an easy-to-use drag-and-drop interface that allows you to add different controls (checkbox, choice field, buttons, drop-down, or text field), forms, and media (video, image, or audio files) into whatever application you are building. It also allows you to store and connect to external data sources inside your app.

# Building our app from SharePoint
We would be connecting Power Apps to our SharePoint List which we created earlier. Here's how you can do that.
- On your SharePoint List, click on 'Integrate', then 'Power Apps', then 'Create an app'.

![](/Images/powerapps-1.PNG)
- Give your app a name and click on 'Create'. I would name it **"SurveySolution"**.

![](/Images/powerapps-2.PNG)

- You would be redirected to Power Apps Studio where you can redesign your application to suit your needs. The next screen would be like the image below.

![](/Images/powerapps-3.PNG)

Employees at Microsoft have a busy time at work, so we must keep this application as simple and easy to navigate as possible. We would be editing our design so employees can submit their responses in less than 20 seconds while navigating through 3 screens.

LET'S START RE-DESIGNING OUR APP!

# Redesigning our Power Apps application
The first thing we would do is change the theme of our application. This theme is too popular in Power Apps, we need something unique. To change the theme, go to 'Theme' at the top navbar and pick any theme of your choice. I would pick "Rose". Notice that immediately you pick a theme, the color of your application changes as shown below.

![](/Images/powerapps-4.PNG)

Now let's focus on our application! The first screen we want employees to interact with is the welcome screen with a clickable button "Get Started". 

To add a new screen, click on 'New screen' at the top and select 'Blank' as shown in the image below. Immediately you do, a new screen would be added to the application.

![](/Images/powerapps-5.PNG)

Now let's add a button to the new screen. To add a button, click the '+ sign' in the left sidebar of the page and search for 'Button'. Click on it and it would automatically be added to the page. I would prefer my button to be close to the bottom of the page, so I would drag it there as shown in the image below.

![](/Images/powerapps-6.PNG)

Next, we need to add an image to the screen, edit the text of the button and add an action that would direct employees to the screen where the form is located so they can fill in their response.

To add an image click the '+ sign' in the left sidebar of the page, search for 'Image', and select. Immediately you do, you would notice a new item added to the screen. Click on the item. Go to Properties in the right sidebar, then Image. Click the dropdown and select '+ Add an image file', then select the image you want to add, preferably your company's logo. The result should look like the image below.

![](/Images/powerapps-7.PNG)

To edit the text in the button, double click the button and type in "Get Started". 

To add an action, click on the button then copy and paste the code below into the fx section showing false above the screen.
``` Power FX
NewForm(EditForm1);Navigate(EditScreen1, ScreenTransition.None)
```
The code above tells the button to take you to the screen (EditScreen1) with the form (EditForm1) when clicked.

Next, we would need to move this screen to the top so it appears first. To do so, click on the ellipsis by the side of the screen (Screen1) and click on 'Move up' till the screen is at the top of the list.

We would need to create a success screen which our employees would see after filling the form. To add that, click on 'New screen' at the top and select 'Success'. A new screen is immediately added to the application.

As mentioned at the beginning, we want our employees to only interact with 3 screens. We have successfully designed the first and last screen, let's design the second screen which would display the form (EditScreen1) and collect responses. Click on the screen to start editing.

Notice from EditScreen1 that the name of the first column is now Title instead of Department. To change that, click on the 'Title' row, hover to the sidebar on the right, click on 'Advanced' then ‘Unlock to change properties’. Now change the DisplayName from "Title" to "***Department***". Also notice that an 'Attachments' column was added to the screen. To get rid of it, just click on the column and delete it.

To get our employee response after filling the form, we need to add a submit button. Follow the same steps you followed when creating the "Get Started" button. This time though, change the text from "Get Started" to "Submit".

To add an action, click on the button then copy and paste the code below into the fx section showing false above the screen.
``` Power FX
SubmitForm(EditForm1) And Navigate(Screen2, ScreenTransition.Cover)
```
The code above submits the form immediately after the button is clicked and directs us to the success screen we created earlier. Our screen should look like the one in the image below.

![](/Images/powerapps-8.PNG)

Now we have created and designed all 3 screens, we would need to delete all other screens which are not part of our application. To delete a screen, click on the ellipsis by the side of the screen name and click 'Delete'.

When you delete the other screens, you would notice an error is flagged in "EditScreen1". Click on the icon then ‘Edit in the formula bar’ and delete the code. Thereafter you can delete every other item. Your screen should look like the one in the image below.

![](/Images/powerapps-9.PNG)

To test your application from the beginning, go to the first screen and click on F5. Fill in the details of the form and click submit. When you click submit you are directed to the success screen and immediately, the response is uploaded on SharePoint. 

I tested my application twice and the responses were stored on SharePoint immediately as you can see from the image below.

![](/Images/sharepoint-5.PNG)

# Sharing your application on Microsoft Teams with your employees
CONGRATULATIONS ON SUCCESSFULLY CREATING YOUR APPLICATION! ✨✨🎉

Now it's time to share our application with our employees. Do not forget to publish your application before sharing though. 

To publish your app, click on 'File' to open up the file menu. Click on 'Save' and then 'Publish'. In the prompt that pop out, click on 'Publish this version' and you are good to go. Immediately your app is published, the 'Publish' button changes to 'Share'. Click on 'Share'.

![](/Images/powerapps-10.PNG)

Click on 'Cancel' as we would like to share with all employees on our Microsoft Teams tenant and not just in a specific channel.

![](/Images/powerapps-11.PNG)

Click on 'Add to Teams'. In the dialog that pops out at the right, click on 'Add to Teams'. 

Before clicking 'Add to Teams', don't forget to edit the description of your application so employees understand what it is about and what it does. You can do so by clicking 'Edit details'. In the page that opens up, click 'File' in the top navbar, then 'Settings' in the left navbar, and edit whatever detail you need to.

When you have completed editing the details, head to the former page and click on 'Add to Teams'. You would be directed to Microsoft Teams where you can decide to add your app to a team or a chat.

![](/Images/microsoftteams-1.PNG)

Click on the dropdown icon beside 'Add' and select 'Add to a team'. 

Next, select the specific team and channel you want the app to be added to. It is required that you select a general channel which can be accessed by everyone in your organization. For me, I would select the team *MPowerSeries* and channel *General*. When completed, click 'Set up a tab'.

The next dialog shows you the description of the application you are adding. Click on 'Save' to set up the tab for your application. CONGRATULATIONS!

Check out [Scheduled Reminder with Adaptive Card](/Scheduled%20Reminder%20with%20Adaptive%20Card/README.md) to learn more about sending out scheduled reminders to your employees when it's time to take the survey.

How do you visualize all the data stored on SharePoint? Check out [Visualizing your Data with Power BI](/Visualizing%20your%20Data%20with%20Power%20BI/README.md) to learn about this.