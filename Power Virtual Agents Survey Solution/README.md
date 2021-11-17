# Overview
Microsoft's Power Virtual Agent allows you create powerful bots that can answer questions in seconds without the help of data scientists or developers. You can decide to create your bot and integrate as a standalone web application, share on Microsoft Teams, on your website, on cortana, telegram, slack or kik.

Using a Power Automate flow connected to your bot, you can collect responses from your users, collate and upload those responses on SharePoint. Love to see how to make this happen? Let's begin!

# Prerequisites
Before we begin designing our bot, let's take some time to talk about how it is expected to work. 

Since our bot is designed for the survey only, our employees would need to start off the conversation with related phrases. These phrases are take survey, employee survey, start survey, survey, and begin survey. We would be using these as our trigger phrases for now.

The bot thanks the employee for taking the survey and asks for their department. It asks the survey questions and collects the employee's rating per question. At the end of the survey, each employee's response is collated and updated on SharePoint in real-time.

# Building your Power Virtual Agents Bot
- Head over to http://aka.ms/TryPVA and sign in with your Microsoft account. Once signed in, you are directed to a page that looks like the image below.

![](/Images/powervirtualagents-1.PNG)

- First give your bot a name. I would name mine **SurveySolution**. Then select your preferred language. Next you are expected to select an environment. I would use my default environment because I created my Power Apps application in that environment. An environment is a space where your organization can store, manage, and share business data, apps, and flows. After filling in the details, click 'Create'. You would be directed to an interface that looks exactly like the one in the image below.

![](/Images/powervirtualagents-2.PNG)

- On the right navigation bar, click on 'Topics'. The next page you are directed to has 12 existing topics. 

A topic defines a how a bot conversation plays out. In this sample, we would create new topics from scratch. Topics have trigger phrases — these could be phrases, keywords, or questions that a user is likely to type. We also have conversation nodes — these are what you use to define how a bot should respond and what it should do.

![](/Images/powervirtualagents-3.PNG)

- Delete the first 4 topics. To do so, open each topic and click on 'Delete' at the top right of the page. After deleting the topics, you would be left with 8 existing topics.

- Now let's create a new topic for the purpose of our survey. On that same page, click on '+ New topic' at the top. Give your topic a name. I would name mine "TakeASurvey". 

- In the section 'Trigger Phrases', I would input up to 5 phrases our employees would possibly type in when about to start the survey.

![](/Images/powervirtualagents-4.PNG)

- Click on 'Go to authoring canvas'. The authoring canvas is where you define the bot's conversation pattern.

![](/Images/powervirtualagents-5.PNG)

- You would notice that a blank Message node was automatically added. In the empty box, input your welcome message. Mine is below.

``` Text
Thank you for taking out time to respond to this survey. We totally appreciate you!
The goal of this short survey is to ensure that you are enjoying being part of our organization. Please fill only once!
```

- Next, add another node by clicking the '+' icon and the 'Show a message'. We need to add a message telling the employee a little bit about the survey. Notice that a new empty text box is added to the flow. In that box, I would input the details below.

``` Text
This survey consist of 4 questions.
For each question, you are expected to tell us how you feel. 0 stands for lowest and 5 for highest.
Be assured that your anonymous responses would go a long way in making our organization better.
```

- Next, we would need to add each question and the option. To do so, click on the '+' icon again, but this time we would click on 'Ask a question'. Notice that as you do, a different type of block is added to the flow.

![](/Images/powervirtualagents-6.PNG)

- Fill in the details of the block correctly.
    * Ask a question: Our first question is "Do you feel good about your current work/life balance?", so we would input it in that box.
    * Identity: This is a multiple choice question as participants can select from 0 to 5.
    * Options for user: Input the different options. In our case, it would be 0 to 5.
    * Save response as: It is important we rename our bot variable for each question, so it's easy to reuse them. Click on the pencil icon and in the column that pops out by the side, change the bot variable name for this first question to question1. Bot variables are global variables as they are used to store information that do not change from topic to topic.

- Notice too that beneath the question block, multiple condition blocks have been added. A separate condition block was created for each option as shown in the image below.

![](/Images/powervirtualagents-7.PNG)

- Next, 
