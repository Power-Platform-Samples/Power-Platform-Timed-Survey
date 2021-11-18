# Overview
Microsoft's Power Virtual Agent allows you create powerful bots that can answer questions in seconds without the help of data scientists or developers. You can decide to create your bot and integrate as a standalone web application, share on Microsoft Teams, on your website, on cortana, telegram, slack or kik.

Using a Power Automate flow connected to your bot, you can collect responses from your users, collate and upload those responses on SharePoint. Love to see how to make this happen? Let's begin!

# Prerequisites
Before we begin designing our bot, let's take some time to talk about how it is expected to work. 

Since our bot is designed for the survey only, our employees would need to start off the conversation with related phrases. These phrases are take survey, employee survey, start survey, survey, and begin survey. We would be using these as our trigger phrases for now.

The bot thanks the employee for taking the survey and asks for their department. It asks the survey questions and collects the employee's rating per question. At the end of the survey, each employee's response is collated and updated on SharePoint in real-time.

# Building your Power Virtual Agents Bot
Head over to http://aka.ms/TryPVA and sign in with your Microsoft account. Once signed in, you are directed to a page that looks like the image below.

![](/Images/powervirtualagents-1.PNG)

First give your bot a name. I would name mine **SurveySolution**. Then select your preferred language. Next you are expected to select an environment. I would use my default environment because I created my Power Apps application in that environment. An environment is a space where your organization can store, manage, and share business data, apps, and flows. After filling in the details, click 'Create'. You would be directed to an interface that looks exactly like the one in the image below.

![](/Images/powervirtualagents-2.PNG)

On the right navigation bar, click on 'Topics'. The next page you are directed to has 12 existing topics. 

A topic defines a how a bot conversation plays out. In this sample, we would create new topics from scratch. Topics have trigger phrases — these could be phrases, keywords, or questions that a user is likely to type. We also have conversation nodes — these are what you use to define how a bot should respond and what it should do.

![](/Images/powervirtualagents-3.PNG)

Delete the first 4 topics. To do so, open each topic and click on 'Delete' at the top right of the page. After deleting the topics, you would be left with 8 existing topics.

Now let's create a new topic for the purpose of our survey. On that same page, click on '+ New topic' at the top. Give your topic a name. I would name mine "TakeASurvey". 

In the section 'Trigger Phrases', I would input up to 5 phrases our employees would possibly type in when about to start the survey.

![](/Images/powervirtualagents-4.PNG)

Click on 'Go to authoring canvas'. The authoring canvas is where you define the bot's conversation pattern. You would notice that a blank Message node was automatically added. In the empty box, input your welcome message. Mine is below.
``` Text
Thank you for taking out time to respond to this survey. We totally appreciate you!
The goal of this short survey is to ensure that you are enjoying being part of our organization. Please fill only once!
```

Next, add another node by clicking the '+' icon and the 'Show a message'. We need to add a message telling the employee a little bit about the survey. Notice that a new empty text box is added to the flow. In that box, I would input the details below.
``` Text
This survey consist of 4 questions.
For each question, you are expected to tell us how you feel. 0 stands for lowest and 5 for highest.
Be assured that your anonymous responses would go a long way in making our organization better.
```

Before asking our questions, we need to identify which department the employee works at. This detail would go along way in helping us position our organization properly. To add this question, click on the '+' icon again, and this time click on 'Ask a question'. Notice that as you do, a different type of block is added to the flow.

Fill in the details correctly.
* *Ask a question:* The question we need an answer to is "Which department do you work with?", so we would input it in that box.
* *Identity:* This is a direct question, so we would pick the employee's entire response.
* *Save response as:* It is important we rename our bot variable for each question, so it's easy to reuse. Click on the pencil icon and in the column that pops out by the side, change the bot variable name for this question to ***department***. Bot variables are global variables as they are used to store information that do not change from topic to topic.

![](/Images/powervirtualagents-5.PNG)

Next, we would need to add each question and the options. We repeat the steps above. Click on the '+' icon again, and click on 'Ask a question'.

Fill in the details of the block correctly.
* *Ask a question:* Our first question is "Do you feel good about your current work/life balance?", so we would input it in that box.
* *Identity:* Unlike the question about department, this is a multiple choice question as participants have to select from 0 to 5.
* *Options for user:* Input the different options. In our case, it would be 0 to 5.
* *Save response as:* Change the bot variable name for the first question to ***question1***.

Notice that beneath the question block, multiple condition blocks have been added. A separate condition block was created for each option as shown in the image below.

![](/Images/powervirtualagents-6.PNG)

After collecting the response to that question, the bot is expected to ask the second question. To make this happen, we need to add a new node to one of the conditions. Click on the '+' sign and then 'Ask a question'. Fill in the block correctly. For 'Ask a question', input the next question. 'Identity' and 'Options for user' is the same throughout as above. For 'Save response as', give each question a new variable name - ***question2*** for the second question, ***question3*** for the third question and ***question4*** for the fourth question.

Now we need to connect all condition blocks earlier to the second question. We do this so that whatever the response to the first question is, the second question would still be asked. To do this, click on the '+' sign and instead of adding a node, click on the small circle and connect to the second question block. Repeat this process for all conditions. Your flow should look like the image below.

![](/Images/powervirtualagents-7.PNG)

Repeat this process for questions 2 and 3 - question 2 connecting to question 3 and question 3 connecting to question 4. After the 4th question, our bot should thank the employee for taking out time to fill the survey. To make this happen, add a 'Show a message' node to the flow, type in a short thank you message, and connect all conditions to the message as shown in the image below.

![](/Images/powervirtualagents-8.PNG)

You can test your bot to make sure it's working well by clicking 'Test your bot' on the left side of the page.

# Collecting Employee's Responses and Updating on SharePoint with Power Automate
CONGRATULATIONS ON SUCCESSFULLY BUILDING YOUR BOT! Now let's connect our bot to our SharePoint using Power Automate.

We start off by adding a new node to our bot after the thank you message. Remember how to add a node? Just click on the '+' sign. This time we would pick 'Call an action' then 'Create a flow'. Clicking 'Create a flow' would open up Power Automate in a new window as shown below.

![](/Images/powerautomate-1.PNG)

Notice that two actions have been automatically added to our Power Automate flow. 

In the first action, Power Automate is establishing a connection with our Power Virtual Agent bot. We need to add each question the bot would ask or we would need response to as an input. 

To add the questions as inputs, click on '+ Add an input', then 'Text'. Notice that when you do, a new input box is added. Repeat this step for all the questions and fill in the details correctly.
* *Input:* Use the same variable name you assigned to each question in the bot as the name of the input. For example, Department for the question to identify which department in your organization the employee works with, Question1 for the first question, Question2 for the second question, Question3 for the third question, and Question4 for the fourth question.
* *Please enter your input:* Enter each question as input. Ensure you input the questions as arranged on SharePoint and in your Power Virtual Agent bot.

![](/Images/powerautomate-2.PNG)

The second action automatically added to our flow returns the values of the first action to Power Virtual Agents. We would need to create an output for each input entered in the first action. Repeat this step for all the inputs and fill in the details correctly.
* *Enter title:* Enter each question as input. Ensure you input the questions as arranged on SharePoint and in your Power Virtual Agent bot.
* *Enter a value to respond:* Click on 'Add dynamic content' and the pop up, select the input for each question.

![](/Images/powerautomate-3.PNG)