# Code and Design Specification
_Assignment G4_

## Part 1: Requirements

**Primary Functional Requirements:** 
  * Users can schedule study sessions with others 
  * Users can participate in study sessions with others
  * Users can track their progress in their own self-reported study goals
  * Users can view others’ progress in their study goals

**Secondary Functional Requirements:** 
* Tool automatically mutes other channels + notifications
* Users can have a more automated group scheduling functionality (e.g. connecting to a calendar API)
* Users can customize what study strategies they can employ
* Analytics of ratings at the end of a study session

**Primary Technical Requirements:**
* Bot creates a persistent channel in the server, this will be used to request study session times, send notifications of individual study sessions, and share information about each of the group members’ study goals
* Bot creates new voice/text channels for each study session, which is deleted at end of session
  * One channel is a private channel between the bot and the user, in this channel, the user can self-report goals/progress when prompted and can react to break-time notifications
  * The other channel is a text/voice channel pair just for the people in the current study session, they have control over these and use them as they want

**Secondary Technical Requirements:**
* Automatic muting of other servers using the Discord API
* Automatic study session scheduling by looking at users’ google calendars using the Google Calendar API
* Database storage of user’s study session ratings

**Primary Usability Requirements:**
* Bot clearly notes what emojis should be used for progress check-ins
* Bot is installable in any Discord server using the OAuth2 protocol
* Bot will send directions for use for main functionalities as its first communication
* Bot will make it clear on how to schedule and respond to group study sessions 

**Secondary Usability Requirements:**
* Bot would be able to integrate with Calendar/Canvas APIs to communicate availability and notifications
* Bot would have walkthrough tutorial or help section for users to consult


## Part 2: Storyboard

**Scenario 1:** Person wants to find a study group in a class discord server, schedules one through study bot.
![G4-storyboard1](/LALA/images/G4-storyboard1.PNG)

**Scenario 2:** People track each other's goals and hold each other accountable during a group study session run by bot. 
![G4-storyboard2](/LALA/images/G4-storyboard2.PNG)

## Part 3: Architectural Design
![G4-ArchitecturalDesign](/LALA/images/G4-ArchitecturalDesign.jpg)

## Part 4: How System Description Enables Storyboard and Requirements
All of the main functional requirements we described in Part 1 have corresponding event handlers in our architectural design. As shown in the architectural design for our project, we plan to have a python file to connect to a user’s guild (server), authenticate access, and then execute above event handlers corresponding to the functional requirements. The file/functions will be written in a way that can handle flow of use as illustrated in our two storyboards.
