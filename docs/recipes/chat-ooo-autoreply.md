---
tags:
  - recipe
  - Out of office
  - Team Messaging
  - Chat
---

# Sending an out-of-office auto-reply for team messaging messages

If you are going out of town, or taking a holiday and need to let your co-workers messaging you know, then it can be helpful to setup an automation that will send an auto-reply via team messaging whenever someone "at-mentions" you in a team, chat or conversation. One challenge however is that when one posts a message to a team, the messages in that team are automatically marked as read. So imagine going out of town, and when you return seeing all of your messages as being read. How would you know what messages you need to reply to?

Enter the automation below, which will post a second message to yourself with a link back to the original conversation, so that when you return to the office you have a reliable catalog of all the messages in which you were mentioned. That way you can reply to each of them, and ease your transition back into the workplace. 

This recipe works like this:

* When you receive a chat message, it will look at the message received date to ensure it is receiving between two dates of your choice.
* It immediately posts an auto-reply message (once per day, per chat)
* It posts a message to your personal chat letting you know you received a message, linking to the team/chat to make it easier to find later. 

[:fontawesome-solid-download: Download automation](chat-ooo-autoreply.json){: download .md-button }

Learn how to [import it into your account](../user-guide.md#importing-automations). 
