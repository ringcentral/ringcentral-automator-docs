---
title: RingCentral Automator Cookbook
---

# Automation Cookbook

A number of our most common automations that work right out-of-the-box are available via a [workflow template](../workflow-templates/index.md). Other automations may be less common, but no less important. 

What follows are a set of simple automations that you can think of as building blocks. Each recipe can stand on its own, but can also be combined with other recipes to make highly customized automations that more precisely meet your needs. Use recipes to learn how to solve common problems workflow designers may have. 

### Recipes

<div class="grid cards" markdown>

- __Team Messaging Out-of-office autoreply__
  
    Let coworkers know in RingCentral app that you are out of the office.
  
    [Download](chat-ooo-autoreply.json) | [Learn more](chat-ooo-autoreply.md)

- __Send an SMS to users only once__
  
    Send an SMS auto-reply the first time someone contacts you. 
  
    [Download](autoreply-only-once.json) | [Learn more](autoreply-only-once.md)

- __Voicemail autoresponse__
  
    Automatically respond via SMS to customers who leave a voicemail.
  
    [Download](voicemail-autoresponse.json) | [Learn more](voicemail-autoresponse.md)

- __Missed call autoresponse__
  
    Send an SMS auto-reply the first time someone contacts you. 
  
    [Download](missed-call.json) | [Learn more](missed-call.md)

- __Triggering automations from IVR menus__
  
    Learn how you can trigger an automation when a user navigates an IVR menu.
  
    [Learn more](ivr-menus.md)

- __Creating automations for call queues and more__
  
    Learn how to setup an automation for non-user-based extensions, e.g. voicemail boxes, IVR menus, call queues and more.
  
    [Learn more](extensions.md)

</div>

## Known issues

### Call queues and the "Call Ended" event/trigger

When building an automation for a call queue that is triggered by the “Call Ended” event, please be aware that the event may not signal an actual end to the call. For example, when a call from a call queue is redirected to a member of the call queue, that will also trigger the Call Ended event. 

### Operators, new voicemail event and voicemail extensions

Operators are not able to subscribe to the “New Voicemail” event for a voicemail extension type. We are investigating a fix for this. 

### User presence variable is unavailable when default runner changed

When admin change runner to make it different with trigger owner, the presence variable is unavailable in automation.
