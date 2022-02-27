# G6
_User Testing_

## Part 1: Description of your medium-fidelity prototype

The two functionalities we implemented are the onboard user feature and the schedule study session feature. For the **onboard user feature**, we implemented an event handler so that users who join the server are DM’d instructions on how to use our tool. The **schedule study session** feature is implemented such that when a user runs a command to set up a study session with a specified time and duration, the bot messages the channel to ask who will attend. Users will accept the study session by reacting with a check or X mark. Any user can run the study session command, where the bot will then create a new text channel and send a message that mentions all the users who accepted the study session.

You can find all the functionalities in our ```bot.py``` file. We didn’t create issues for these functionalities. For our other functionalities during our user test, we chose to omit them for now.

## Part 2: Screenshot/photo of the prototype:

![G6BotDM](/LALA/images/G6/G6BotDM.JPG)

**Image I.** Onboarding DM from Bot to new user upon joining the server.

![G6BotSchedule](/LALA/images/G6/G6BotSchedule.PNG)

**Image II.** User schedules a study session and the bot sends a poll to the channel.

![G6BotStudyChanel](/LALA/images/G6BotStudyChanel.PNG)

**Image III.** When the study session time begins, users are added to a new channel for the session and notified it has started.

## Part 3: Findings from the user testing sessions

### What did you learn in the user testing sessions?

We gathered a lot of useful feedback from our six user testing sessions. We got a lot of feedback on our existing functionalities (onboarding user and starting study session), as well as feedback on functionalities we have yet to implement.

For our existing functionalities, we got feedback mainly on organization and formatting of our bot interactions. People liked that they were sent a DM with instructions on how to use the bot. Some things to change included how much content we were sending and formatting to make important information more clear. Folks also gave us feedback on scheduling the study session and some small fixes for us were to take a look at date format for scheduling, how users are going about reacting with emojis, organization and creation of study session channels, and more. We got great suggestions such as giving users the choice to create a text and/or voice channel, creating private study session channels, and more.

We also got a lot of great feedback on how to further develop our future functionalities, such as for starting up a session, generating break messages, and more. 

### Are the findings promising enough that you would like to go ahead with the current functionality of the prototype? (If yes, describe why, if no, describe what changes you are proposing to make.)

Based on feedback from our users about the two functionalities we tested we are going to keep the Onboarding DM and reformat it with less text so the commands are clearer. We are also going to implement a ```/help``` command to reiterate the instructions to the user if they need. This will increase the visibility for the instructions for multiple different user scenarios. We will also provide more descriptions for the different channels that users will interact with.

We will change the implementation of study sessions in order to have a more modular design that includes the study session id, users who have accepted, and the times required for reminders/check-ins. This will prevent issues that we encountered regarding concurrent study sessions, and allow us to continue developing our planned features with check-ins, break times, and closing the study session channel.

### What are the next functionalities that you will implement in your prototype?

In addition to the edits and revisions to our current features, we will also be adding these new features that pertain to the bulk of our study session group work.

* Study session reminders
* Automatic Studybot check-ins
* Automatic recommendations for break times
* Ending a study session

### User Testing Quotes
- Onboard User DM:
  - “Too many instructions”
  - “Date format is a little strange, won’t be scheduling study sessions years in advance”
  - “Should add instructions for starting the study session”
  - “Send different directions as different messages”
  - “Add some formatting like bolding, emojis, etc.”
  - “Make it more clear how the bot prompts during the study sessions”
  - “Would be nice to have a legend or breakdown of all the commands”
  - “Not sure which channel to post in, have instructions describe all of the channels”
- Scheduling Study Session
  - “Would be nice to have the emojis preloaded on the bot study session request message”
  - “The one who sends the schedule request should have an automatic green check reaction”
  - “When scheduling a session, having to navigate back to the DM to make sure they’re typing it correctly”
  - “Could we just start a study session without scheduling it in advance?” (used words such as “now”, “today”, “tomorrow”)
  - “Unsure if the user that sends the schedule request should also react to the message”
  - [For when we implement automated study session start] “Have a study session identifier (name, number, etc.) for channel names”
  - “What is the difference between ignoring a study session request vs. reacting with an X”
  - “When scheduling a session, give the option to create a voice channel or text channel or both”
- Beginning study session
  - “Likes that the users who reacted are being mentioned, draws attention to the channel”
  - “New spun up channel should only be viewable by members of study session”
- During study session
  - “Would be nice to get ‘15 minutes left’ reminders”
- End study session
  - “Would be nice if we could ask users in study session if they want to extend the time”
- General
  - “Unsure if this is meant for collaborative work time with others or just to do individual work with others”
  - “Instead of sending scheduling in any channel, have a dedicated channel just for scheduling purposes”
  - “Consider maybe adding an option for recurring study sessions”
  - Implement ```/help``` feature to get reminder of how to use bot
  - “For bot messages, would be nice to add some spice with some fun message formatting”
  - “Add a functionality so that users can leave the study session early so they don’t continue getting notifications”
  - ```/leave``` - announces to everyone else that you’re leaving and removes you from study session
  - “Can people who didn’t respond to the bot’s invite still join the study session?”
  - Build functionality for private channels, but have public as default

