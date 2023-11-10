# Automation recipes

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
