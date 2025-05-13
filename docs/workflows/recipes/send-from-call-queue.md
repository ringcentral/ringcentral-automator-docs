# Send SMS messages from a call queue

Many RingCentral customers ask: "How can I send SMS messages from my call queue number?" or "Why can’t my team text customers using our main business number?" If you use a call queue phone number for customer-facing communications, being able to send text messages (SMS) from that same number is essential for consistent branding, seamless customer experiences, and effective team collaboration.

This article explains what you need to know and where to go to configure SMS for call queues in RingCentral, including how to assign a recipient so messages can be managed properly—especially when using automated workflows in Workflow Builder.

## Why You Might See Issues Sending SMS from a Call Queue

Out of the box, RingCentral call queues are designed for voice routing, not SMS. So when you try to send a text from your call queue number, you may notice:

* SMS messages fail to send
* Responses are missed or not routed to the right team member
* Workflow Builder automations that depend on SMS triggers or actions don't work as expected

The root cause? The call queue number isn’t set up to allow SMS or doesn’t have an assigned SMS recipient. Without this step, RingCentral doesn’t know who should send and receive texts on behalf of that number.

## How to Enable SMS for a Call Queue Number

To enable SMS on a RingCentral call queue number, you’ll need to assign an SMS recipient in the Admin Portal or RingCentral App. Once done, SMS messages sent to the call queue number will go directly to the designated user or group. This also enables workflows in Workflow Builder that use SMS actions to function correctly.

We won’t repeat the full instructions here, but RingCentral’s official guide walks you through every step:

* [Assigning an SMS recipient for call queues](https://support.ringcentral.com/article-v2/assigning-an-sms-recipient-for-call-queues-in-the-ringcentral-app-and-admin-portal.html?brand=RingCentral&product=RingEX&language=en_US)

### Use Cases Supported by This Setup

* A support team wants to send order updates from a single shared business number
* A sales queue needs to follow up with leads via SMS after missed calls
* A workflow automation sends appointment reminders using a call queue’s number

## Tip for Workflow Builder Users

Once your call queue has an assigned SMS recipient, you can use Send SMS actions in Workflow Builder with that number, enabling powerful automation like:

* Sending automated replies when a customer texts in
* Notifying a team member via SMS when a voicemail is left in the call queue
* Triggering an SMS after a specific call queue event

## Summary

To send SMS from a call queue number in RingCentral or use that number in Workflow Builder, you must assign an SMS recipient to the queue. This unlocks messaging features and improves how your team communicates with customers.