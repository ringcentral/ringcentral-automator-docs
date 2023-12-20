# Troubleshooting

## Why isn't my automation getting triggered?

One of the most common questions from users of Automator happens when they setup an automation for the first time, and then try to trigger the automation by placing a phone call. They observe that their automation is not getting triggered, and they want to understand why. This is especially true for automations that are triggered in some way by a phone call. 

In most cases, the trick to solving this problem rests in understanding how phone calls are routed through an account based on the account's call handling rules. That is because automations must be associated with where a call ultimately terminates in order for those automations to be triggered. Let's look at a common example in which one wants to send an SMS when a call is missed from a call queue. 

First, let's look at what the customer experiences and how this is typically configured in RingCentral. 

1. A customer calls your main company number, typically extension 101. 
2. The customer hears an IVR prompt, "press one if you are an existing client, or press two for sales."
3. The customer presses "2" and the call is transfered to a new extension of type "Call Queue," say extension 105.
4. The customer waits at extension 105 for someone to become available.
5. The customer waits a while, grows impatient, and hangs up. The call has now been missed.

When looking at this flow, many will create an automation associated with the main company number, because that is what the customer dialed to contact them. This is a very logical conclusion to make. However, if you want to send an SMS when a call is missed while waiting for a member of the sales team to answer the phone, then in actuality, one needs to associate the automation with extension 105, the call queue extension that ultimately received the call, and where that call was ultimately terminated. 

## Sending SMS

<details id="noSMS" markdown>
  <summary>Why is the "Send SMS from" field empty? Why am I unable to send SMS?</summary>

  There are a couple reasons why a user in Automator might not have SMS fully enabled for their account or extension. Check to see which of these two issues may be affecting you and take the appropriate action.

  **You do not have a phone/device or phone number assigned to you**

  All SMS messages must be sent from a phone number you have rights to. For most, this is a phone number that has been assigned to them. You can verify that you have a number via our Admin Console. Follow these steps.

  1. Log into the [Admin Console](https://service.ringcentral.com/)
  2. Click the "Settings" tab.
  3. Expand the "Phones & Numbers" section.
  4. Check for one of the following:
      - There is a "Primary Number" assigned to you.
      - Under the "Numbers" tab, make sure a number is assigned to you.

  If you do not have a number assigned to you, contact your account administrator to have one assigned to you.

  ![phone numbers](./img/phone-numbers.png)

  **SMS feature is not enabled for your number/extension**

  If you have a phone number, that phone number needs to be enabled for SMS. This check is best done via a RingCentral API, but in almost all circumstances a number is not enabled for SMS because your organization has not successfully completed a TCR registration. This is a step required by all carriers to help combat fraud and comply with industry regulations.

  To resolve this problem, please register your company and how you are using SMS via the [Admin Console](https://service.ringcentral.com/).
</details>

<details id="mainNumber" markdown>
  <summary>How do I send SMS from my company's main number?</summary>

  In order to send an SMS from your company's main number, the person logged into Automator must be designated the Operator for their account. This is done in the RingCentral Admin Console. Follow these steps.

  1. Log into the [Admin Console](https://service.ringcentral.com/).
  2. Click the "Phone System" tab.
  3. Click "General Settings" under "Auto-Receptionist."
  4. Expand the "Call handling", then click "Settings" tab
  5. Scroll down to "Call / Fax / SMS Recipients" and select your extension as the "Operator Extension." It is extension 101 by default.

  ![operator extension](./img/operator-extension.png)

  Once you know the extension associated with your main company number or Operator, an administrator can load that extension into Automator. They can then build and design workflows on behalf of the Operator. To enable these workflows, the Operator will need to login or accept their Automator invite.
</details>

<details markdown>
  <summary>How can I prevent Automator from sending messages too frequently?</summary>

  Automator allows you to set limitations on the frequency of automation running. To prevent excessive messaging, please refer to the user guide for instructions on how to configure these limitations.
</details>

## Automation templates

<details markdown>
  <summary>Why is my missed call auto-reply automation not working?</summary>

  There are a few reasons why your missed call auto-reply automation may not be working. 

  First, if a call goes to voicemail, it will not trigger the missed call event in Automator. To enable auto-reply for calls that go to voicemail, you need to add voicemail auto-reply automation separately.

  Second, for calls from a call queue, the missed event is triggered at the call queue extension, not the call queue member. To set up missed call automation for call queue extensions, please refer to the admin guide for detailed instructions.

  It's important to note that Automator's events are currently based on the extension/user level. This means that if a call is redirected to an IVR menu and disconnected before reaching an extension, the event will not be fired for the extension's automations. Unfortunately, missed called event at IVR menus is not supported at this time. For now, user can create a advanced automation for IvrMenu with call ended trigger and call end reason is "CallerDropped" to run automation when user end call before pressing any key to be redirected.
</details>

## Call queues, voicemail extensions, and IVR menus

<details markdown>
  <summary>Why is my automation not being triggered with IVR menus?</summary>

  Currently, Automator only support call received and call ended trigger for IVR menu extension. Please refer to IVR section in admin guide for details.
</details>

<details markdown>
  <summary>Why is the "call received" event not being triggered for my voicemail-only extension?</summary>

  We have new release to support call received event for voicemail-only extension. But it requires user to disable and enable the automation onc to get event.
</details>

<details markdown>
  <summary>How do I send an SMS from a call queue's phone number?</summary>

  Sending an SMS on behalf of a call queue is not currently supported. If you need to send SMS messages from a call queue's direct number (or "DL"), you must create the call queue without having a call queue manager. The call queue must be set with unique email address and password and to send SMS from that call queue number, the app must be authenticated using the call queue's login credentials.
</details>

<details markdown>
  <summary>How can I set up an automatic SMS reply when a user presses a key on the IVR menu?</summary>

  To achieve this, begin by crafting an empty IVR menu within the RingCentral admin portal. Following this, modify your current IVR menu to redirect users to the newly established IVR menu when they press the designated key. Proceed by generating an advanced automation in Automator, utilizing the trigger "Call received," and configuring the action "send SMS" for the extension connected to the empty IVR menu. This seamless integration will enable the desired automatic SMS response when a key is pressed on the IVR menu.
</details>

## Presence

<details markdown>
  <summary>My automations based on my presence do not seem to work.</summary>

  Some may observe that Automator assumes one is "Available" even after one changes their presence in the RingCentral mobile or desktop app. This is especially true when you set your status to "Invisible." 

  The reason for this discrepency lies in the fact that their are two types of presence within RingCentral's ecosystem: one presence is tied to telephony and the other is tied to team messaging. Automator only is able to respond to one's telephony presence, which is determined by one being on the phone or not. Other presence may be related to your team messaging presence which Automator does not currently have access to and is unable to build rules around. 
</details>

## Team chat and messaging

<details markdown>
  <summary>How to get RingCentral Team Messaging team ID</summary>

  You can use "Copy team URL" feature in RingCentral Team Messaging, then you can get conversation id in the URL.
  
  ![Copy Team URL](./img/copy-team-url.png){ style="max-width: 50%" }
</details>

## Using Automator

<details markdown>
  <summary>Why can't I edit an automation?</summary>

  You can't edit an automation if it is enabled. Please disable the automation first, and then proceed to edit it.
</details>

<details markdown>
  <summary>Why can't I edit a node in my advanced automation?</summary>

  You can't edit any node of automation if the node has any children. You can delete sub nodes then edit the node.
</details>

<details markdown>
  <summary>Why can't I enable the automation?</summary>

  You can't enable the automation if there are blank or incomplete nodes in the automation, or if the automation lacks an action node. 
</details>

<details markdown>
  <summary>Why doesn't my automation work?</summary>

  Please check the automation status firstly. If the automation is NOT enabled, it won't work. If the automation is enabled, please check logs of the automation. And check if trigger filters and conditions are set correctly. Most issues are caused by wrong conditions. And please check history details in History page.
</details>

<details markdown>
  <summary>Why doesn't time related condition work?</summary>

  The app uses timezone that user set in RingCentral service portal. Be sure you have set right timezone in [RingCentral service portal](https://service.ringcentral.com/application/settings/settings/extensionInfo/settingsAndPermissions).

  After timezone updated, please re-enable the automation to make timezone synced to this app.
</details>

<details markdown>
  <summary>Why don't I see a newly registered phone number in my automation templates?</summary>

  Automator caches input options in the browser's local storage. You can logout and log back in to refresh the cache.
</details>

<details markdown>
  <summary>When will automation history be cleared?</summary>

  Automation history is automatically cleared after 7 days.
</details>

<details markdown>
  <summary>Why I can't get automation history?</summary>

  The app only creates automation history when there are any actions run in the automation. Please check if there are any issue at trigger filters or condition node to prevent action running.
</details>
