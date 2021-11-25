# Overview
CONGRATULATIONS on getting this far!

In this section, I would show you how to send scheduled reminders to everyone in your organization when it's time for them to take the survey. We want our survey to be sent regularly so we can capture our employee's feelings, so we would schedule our reminders to go out every Tuesday by 09:00am. Microsoft's Power Automate can help make this happen.

We would be sending out these reminders as adaptive cards. An Adaptive Card is a modern technology built by Microsoft to help content creators create engaging messages that are rendered into a native UI. These messages adapt to the hosted app experience.

You can learn more about Adaptive Cards using any of the links below:
- [Creating Adaptive Cards](https://docs.microsoft.com/en-us/learn/modules/writing-adaptive-cards/)
- [Create engaging messages with Adaptive Card](https://docs.microsoft.com/en-us/learn/modules/adaptive-cards-create-engaging-messages/)

Let's begin building our adaptive card.

# Building our Automated Adaptive Card
If you would love to design your adaptive card yourself, visit [Adaptive Cards Designer](https://adaptivecards.io/designer/) page and design your own adaptive card to suit your needs.

You could decide to use the adaptive card I designed. Here's the JSON code for the adaptve card I designed
``` JSON
{
    "type": "AdaptiveCard",
    "body": [
        {
            "type": "TextBlock",
            "size": "ExtraLarge",
            "weight": "Bolder",
            "text": "Anonymous Survey Solution",
            "spacing": "Medium",
            "horizontalAlignment": "Center",
            "fontType": "Default",
            "color": "Good",
            "isSubtle": true
        },
        {
            "type": "TextBlock",
            "text": "Hello Everyone,\n\nHow's your week going? Hope you all are having fun at work?\n\nWe would love to know how things are going in your various departments and would appreciate if you could please fill a short survey. \n\nYou can decide to take the survey \n- by visiting the SurveySolution tab in the General channel of MPowerSeries team, or\n\n- by searching for SurveySolution in the apps section and adding it to your Microsoft Teams.\n\nThanks again for your time and be sure to have an amazing week ahead.\n\nBest regards!",
            "size": "Large",
            "weight": "Bolder",
            "isSubtle": false,
            "horizontalAlignment": "Left",
            "wrap": true,
            "maxLines": 36,
            "fontType": "Default"
        }
    ],
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "version": "1.3",
    "verticalContentAlignment": "Center",
    "backgroundImage": {
        "fillMode": "RepeatHorizontally"
    }
}
```

The result should be like the one in the image below.

![](/Images/adaptivecard-1.PNG)

# Creating our Scheduled Reminder
Now it's time to automate sending of the reminders. As mentioned above, we want our reminders to go out every Tuesday by 09:00am. Let's head over to [Power Automate](https://flow.microsoft.com) and start creating this.

In Power Automate, click on 'Create' in the left navbar. Select 'Scheduled cloud flow'. In the dialog that pops up, fill in the correct details about your flow.
* Flow name: Give your flow a name
* Run this flow: Select a start date for your flow and pick the specific time you want it to run on the scheduled day or days.
* Repeat every: We want our flow to run weekly, so we set the repeat time to be 1 week.
* On these days: Here select the day or days each week you want your flow to run. You might need to select more than one day as your employee's might need more than on reminder before they fill the survey.

![](/Images/powerautomate-7.PNG)

Click 'Create' when you are done filling in the details. You would be directed to a new page. The first step in our Power Automate flow is the schedule we created earlier. 

Click on '+ New step' to add a new step to your flow. The new step would send out the adaptive card as a message on our preferred Microsoft Teams channel. Search for "Adaptive Card" and select 'Post adaptive card in a chat or channel'.

When you do, your flow would check if you are signed in to Microsoft Teams and then create a connection if confirmed. Thereafer, fill in the required details correctly.
* Post as: Flow bot
* Post in: We want our adaptive card to be posted in a Microsoft Teams channel, so we would select 'Channel'
* Team: Select the Microsoft Teams team you want the message to be posted in
* Channel: Select the specific channel in that team
* Adaptive card: Here you would need to paste in your adaptive card code. If you designed your adaptive card in the adaptive card designer, go to "Card Payload Editor" below the card design, copy the code and paste here. If you are using my adaptive card code, just copy and paste here.

![](/Images/powerautomate-8.PNG)

Click 'Save' and then 'Test'. In the dialog that pops out, select 'Manually', 'Test', and finally select 'Run flow'. Your flow should run successfully if you filled in all details correctly.

CONGRATULATIONS for successfully coming this far.