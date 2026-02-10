# Triggers

The creation of all [custom workflows](./index.md) begin by selecting the event that will trigger the workflow to be executed. When customizing a workflow trigger, users can specify filtering conditions for the workflow, which dictate the circumstances under which a workflow will be executed. Users can specify whether all conditions must be met, or whether any (one or more) conditions must be met. 

## Index of all triggers

<div class="grid cards triggers" markdown>

- ![Missed call icon](../../../img/icon-call-missed.png){ .icon-trigger } __[Call missed](call-missed.md)__
- ![Missed call icon](../../../img/icon-call-ended.png){ .icon-trigger } __[Call ended](call-ended.md)__
- ![Missed call icon](../../../img/icon-call-received.png){ .icon-trigger } __[Call received](call-received.md)__
- ![Missed call icon](../../../img/icon-chat-message-received.png){ .icon-trigger } __[Chat message received](chat-message-received.md)__
- ![Missed call icon](../../../img/icon-fax-received.png){ .icon-trigger } __[Fax received](fax-received.md)__
- ![Missed call icon](../../../img/icon-fax-sent.png){ .icon-trigger } __[Fax sent](fax-sent.md)__
- ![Missed call icon](../../../img/icon-on-demand.png){ .icon-trigger } __[On-demand](on-demand.md)__
- ![Missed call icon](../../../img/icon-scheduled.png){ .icon-trigger } __[Scheduled](scheduled.md)__
- ![Missed call icon](../../../img/icon-sms-received.png){ .icon-trigger } __[SMS received](sms-received.md)__
- ![Missed call icon](../../../img/icon-voicemail-received.png){ .icon-trigger } __[Voicemail received](voicemail-received.md)__

</div>


## Limiting the frequency of a workflow

Users can also limit how often a workflow will be run for any given triggering event. For example, suppose you are creating an SMS auto-reply, to notify someone that you are out-of-the-office. In such circumstances, you wish to only send an auto-reply once per day regardless of how many times a given individual may send you an SMS in a 24-hour period. 

Each workflow has a way to limit the frequency of its execution based upon the person triggering the event. Look and read carefully when editing a trigger to see how its execution can be throttled. 

## Variables added to a workflow's context by a triggering event

Each triggering event has metadata associated with it that will help govern how the workflow will function. This metadata is accessed within the context of a workflow via "trigger variables." For example, you may want to build a workflow that performs different functions depending upon the content of an SMS message that was received. The event associated with this is [SMS received](sms-received.md) and the trigger variable would be "message text."

Consult the documentation for each trigger to see what variables it adds to the workflows context. 

See: [Variables](../variables.md)

## Administrator options

### Running a workflow on behalf of another user

Administrators have the exclusive ability to modify which user a workflow is executed on behalf of. This ability is especially useful when a user wants to send SMS from a phone number that belongs to another user. Given that users can only send SMS from the phone numbers assigned to them, this allows a user to send SMS from a phone number they may otherwise not be allowed to. 

![admin options](../../../img/admin-options.png)

The same concept applies across the board. When you run a workflow on behalf of another user, you can perform any action that the user is permitted to do, even if the owner of the workflow doesn't have that ability themselves. 

One can modify this setting by editing the trigger node associated with a workflow. 

