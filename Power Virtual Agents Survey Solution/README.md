# Overview
Microsoft's Power Virtual Agent allows you create powerful bots that can answer questions in seconds without the help of data scientists or developers. You can decide to create your bot and integrate as a standalone web application, share on Microsoft Teams, on your website, on cortana, telegram, slack or kik.

Using a Power Automate flow connected to your bot, you can collect responses from your users, collate and upload those responses on SharePoint. Love to see how to make this happen? Let's begin!

# Prerequisites
Before we begin designing our bot, let's take some time to talk about how it is expected to work. 

Since our bot is designed for the survey only, our employees would need to start off the conversation with specific phrases related to taking a survey. For example, take survey, employee survey, start survey, survey, and begin survey. We would be using these as our trigger phrases for now.

The bot thanks the employee for taking the survey and asks for their Department. It then asks the survey questions and at each point, it collects the employee's rating per question. At the end of the survey, the entire response is collated and updated on SharePoint in real-time.

# Building your Power Virtual Agents Bot
- Head over to http://aka.ms/TryPVA and sign in with your Microsoft account. Once signed in, you are directed to a page that looks like the image below.

![](/Images/powervirtualagents-1.PNG)

- First give your bot a name. I would name mine **SurveySolution**. Then select your preferred language. You are also expected to select an environment. I would use my default environment because I also created my Power Apps application in that environment. An environment is a space where your organization can store, manage, and share business data, apps, and flows. Pick the environment you would like to use. When you have filled in all details correctly, click 'Create'. You would be directed to an interface that looks exactly like the one in the image below.

![](/Images/powervirtualagents-2.PNG)

- On the right navigation bar, click on 'Topics'. The next page you are directed to has 12 existing topics. 

A topic defines a how a bot conversation plays out. In this sample, we would create new topics from scratch. Topics have trigger phrases — these could be phrases, keywords, or questions that a user is likely to type. We also have conversation nodes — these are what you use to define how a bot should respond and what it should do.

![](/Images/powervirtualagents-3.PNG)

- Delete the first 4 topics. To do so, open each topic and click on 'Delete' at the top right of the page. After deleting the topics, you would be left with 8 existing topics.

- Now let's create a new topic for the purpose of our survey. On that same page, click on '+ New topic' at the top. Give your topic a name. I would name mine "TakeASurvey". 

- In the section 'Trigger Phrases', I would input up to 5 phrases our employees would possibly type in when about to start the survey.

![](/Images/powervirtualagents-4.PNG)

- Click on 'Go to authoring canvas'. The authoring canvas is where you define the bot's conversation pattern.

