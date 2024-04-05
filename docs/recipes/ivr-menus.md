# Triggering automations within an IVR menu

For extensions of type `IvrMenu`, only "Call Received" and "Call Ended" triggers are currently supported. IVR menus cannot technically miss a call in our system today. 

For the "Call ended" trigger, there is a variable "Call end reason" that holds one of the following values:

* Voicemail
* CallerDropped
* BlindTransfer
* CallFinished
* NoReason

![Call ended trigger](call-ended-trigger.png)

## Properly detecting if an IVR menu "missed" a call

One can use the "Call end reason" variable to determine if a caller ended the call before pressing a key. For example, let's say you have an IVR menu that prompts people with, "Press 1 to speak to Sales, press 2 to leave a voicemail." When user end the call without pressing any key, "Call end reason" will be "CallerDropped". But when user is redirected by pressing 1, "Call end reason" will be "NoReason". 

## Detecting what key a user pressed in an IVR menu

For now, there is no way to detect specific key a user pressed in an IVR menu, but we can make some reasonable inferrences depending upon what extensions an IVR menu might direct a user to. For example, if an IVR menu directs someone to a extension 203, and if the IVR menu is the only way a user could navigate to that extension, then one could place a "Call received" trigger on extension 203 - thereby detecting that someone previously selected it via an IVR menu. 

