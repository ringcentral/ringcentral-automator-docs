---
title: RingCentral Automator Cookbook
---

# Automation Cookbook

!!! tip "Share your favorite workflow recipe with the community"
    We would love to learn more about your favorite workflow, and how it has positively impacted you. Please consider exporting your most useful recipe and sharing it with us, so that we can publish it and so that others might benefit from it as well. 
	[Share your recipe via Github &raquo;](https://github.com/ringcentral/ringcentral-automator-docs/issues/new)

A number of our most common automations that work right out-of-the-box are available via a [workflow template](../workflow-templates/index.md). Other automations may be less common, but no less important. 

What follows are a set of simple automations that you can think of as building blocks. Each recipe can stand on its own, but can also be combined with other recipes to make highly customized automations that more precisely meet your needs. Use recipes to learn how to solve common problems workflow designers may have. 

### Recipes

<div class="grid cards" markdown>

- [__Team Messaging Out-of-office autoreply__](chat-ooo-autoreply.md)
  
    Let coworkers know in RingCentral app that you are out of the office.
  
    [:fontawesome-solid-download: Download](chat-ooo-autoreply.json)

- [__Send an SMS to users only once__](autoreply-only-once.md)
  
    Send an SMS auto-reply the first time someone contacts you. 
  
    [:fontawesome-solid-download: Download](autoreply-only-once.json)

- [__Voicemail autoresponse__](voicemail-autoresponse.md)
  
    Automatically respond via SMS to customers who leave a voicemail.
  
    [:fontawesome-solid-download: Download](voicemail-autoresponse.json)

- [__Missed call autoresponse__](missed-call.md)
  
    Send an SMS auto-reply the first time someone contacts you. 
  
    [:fontawesome-solid-download: Download](missed-call.json)

- [__Unavailable autoresponse__](unavailable.md)
  
    Send an SMS in response to someone if your presence status is anything but "available."
  
    [:fontawesome-solid-download: Download](unavailabe.json)

- [__Triggering automations from IVR menus__](ivr-menus.md)
  
    Learn how you can trigger an automation when a user navigates an IVR menu.

- [__Creating automations for call queues and more__](extensions.md)
  
    Learn how to setup an automation for non-user-based extensions, e.g. voicemail boxes, IVR menus, call queues and more.

</div>

## Known issues

### Call queues and the "Call Ended" event/trigger

When building an automation for a call queue that is triggered by the “Call Ended” event, please be aware that the event may not signal an actual end to the call. For example, when a call from a call queue is redirected to a member of the call queue, that will also trigger the Call Ended event. 

### Operators, new voicemail event and voicemail extensions

Operators are not able to subscribe to the “New Voicemail” event for a voicemail extension type. We are investigating a fix for this. 

### User presence variable is unavailable when default runner changed

When admin change runner to make it different with trigger owner, the presence variable is unavailable in automation.
