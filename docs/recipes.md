# Automation recipes

## Sending an out-of-office auto-reply for team messaging messages

If you are going out of town, or taking a holiday and need to let your co-workers messaging you know, then it can be helpful to setup an automation that will send an auto-reply via team messaging whenever someone "at-mentions" you in a team, chat or conversation. One challenge however is that when one posts a message to a team, the messages in that team are automatically marked as read. So imagine going out of town, and when you return seeing all of your messages as being read. How would you know what messages you need to reply to?

Enter the automation below, which will post a second message to yourself with a link back to the original conversation, so that when you return to the office you have a reliable catalog of all the messages in which you were mentioned. That way you can reply to each of them, and ease your transition back into the workplace. 

This recipe works like this:

* When you receive a chat message, it will look at the message received date to ensure it is receiving between two dates of your choice.
* It immediately posts an auto-reply message (once per day, per chat)
* It posts a message to your personal chat letting you know you received a message, linking to the team/chat to make it easier to find later. 

You can [download this automation](./recipes/glip-ooo-autoreply.json){download} and [import it into your account](user-guide.md#importing-automations). 

## Triggering automations within an IVR menu

For IvrMenu extensions, only call received and call ended trigger are supported. Missed call event is not supported for IvrMenu. 

For "Call ended", there is a variable "Call end reason" that can know if user end the call before pressing a key. For example, let's say you have an IVR menu that prompts people with, "Press 1 to speak to Sales, press 2 to leave a voicemail." When user end the call without pressing any key, "Call end reason" will be "CallerDropped". But when user is redirected by pressing 1, "Call end reason" will be "NoReason". For now, we can't know which key user press.

## Creating automations for call queues, IVR menus and voicemail-only extensions

To key to becoming an Automator expert lies in understanding how your account has been configured to route and handle calls. Lets suppose one wants to implement the following automation: when a customer calls the main company number, if the call is missed, then I want to send the customer an SMS." 

It is entirely logical to think that to enable the above automation, one needs to bind an automation to the main company number. However, if your call handling rules route incoming calls to a call queue for example, or an IVR menu, then the correct course of action is to bind your automations to those extensions -- and *not* directly to the main company number. 

!!! tip "A simple and effective trick is to create a simple diagram of your company's phone tree and call routing rules. Once you are able to visualize where calls are ultimately routed, then it becomes much easier to know which extensions to bind and setup automations for."

## Known issues

### Call queues and the "Call Ended" event/trigger

When building an automation for a call queue that is triggered by the “Call Ended” event, please be aware that the event may not signal an actual end to the call. For example, when a call from a call queue is redirected to a member of the call queue, that will also trigger the Call Ended event. 

### Operators, new voicemail event and voicemail extensions

Operators are not able to subscribe to the “New Voicemail” event for a voicemail extension type. We are investigating a fix for this. 

### User presence variable is unavailable when default runner changed

When admin change runner to make it different with trigger owner, the presence variable is unavailable in automation.
