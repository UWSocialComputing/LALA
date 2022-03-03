
# The Project

Our team is interested in understanding how we can best help students _streamline their productivity and to help limit burnout._

# The Team
![Team_Pictures](/LALA/images/LALAProfilePics.png)

# The Solution
<div style="text-align:center"><img src="https://github.com/UWSocialComputing/LALA/blob/main/images/Logo.png?raw=true" /></div>

Check out our <a href="https://github.com/UWSocialComputing/LALA-Project/blob/main/README.md">GitHub Respository</a> to learn more!

## 🔍  About Our Tool

Welcome to _**StudyCafeBot** ☕️_ – a Discord bot that will help users schedule collaborative online study sessions where they can motivate each other to stay on topic and reflect on their goals. 

_How did this tool come about?_ With everyone in our group being college-aged students going into new grad life, we’ve experienced the troubles and consequences of education and technology intertwining more and more. The utilization of platforms such as Discord, Slack, Google Calendar, Notion, and more have helped students like us to organize their tasks, keep track of deadlines, and more. But at the same time, this usage has kept our attention locked on screens, hour after hour, causing screen fatigue and burnout. We know that there are an overwhelming number of tasks to accomplish in such little time.

We hoped to create a solution that will allow us to remain productive and efficient online, while reducing screentime, which can contribute to screen fatigue and burnout.
<br><br>

## 💻  How to Download

Feel free to locally clone the repo and try it out on your own! We are hoping to figure out how to host our bot over a server to make it more accessible.
<br><br>

## 🧑‍💻 How to Use

### ⏰ Scheduling a Study Session
To schedule a study session, you can send a request in any text channel with the format **/schedule [year-month-date] the time in PT followed by am/pm and the duration [1,2,3 hr]**. <br>

`🆕 Example: /schedule 2022-02-23 5pm 1')`
<br><br>
After sending the schedule command, StudyCafeBot will send out a study request with the time, date, and length you requested along with a study session id at the bottom of the message.<br><br>
Once your session is scheduled other members of the server can “RSVP” to the session by using the reactions ✅ or ❌!
<br><br>

### 💡 Starting a Study Session
To start your study session, you can send a message in any channel with the format **/startsession with the session id assigned to your request**. <br><br>
`🆕 Example: /startsession 0`<br><br>
Upon sending the message, you and your study session partners will be sent to a new private text channel created just for the study session. You will be prompted by the bot to share what your goals are for the study session. Once everyone has shared, the bot will send out everyone's goals to the new study session text channel.<br><br>

#### ⏱  _Check-ins and Break Reminders_

Throughout the duration of the study session, StudyCafeBot wil check in with you every 30 minutes to see how you're progressing through your goals by having you rate your progress on a scale from 1 to 5. After you share your rating, the bot will recommend you to take a five minute break before you continue working!<br><br>

### 🎉  Ending a Study Session
Once you have finished your study session, one of your group members can type **/endsession** in the private study session text channel. The bot will send you a report of how you did during the study session and then the private text channel will close!
