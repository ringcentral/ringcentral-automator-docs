# Trigger: missed call

This event is fired when a call comes into an extension, but is never answered or picked up. 

* Voicemail-only extensions do not fire the missed call event, because no call that comes into a voicemail extension is ever missed - they are instantly picked up and a voicemail message is played. 
* Call queues fire the missed call event when a user hangs up while waiting for someone to answer. 
* Some call queues are configured to transfer unanswered calls to another extension, like a voicemail box. If this is the case for you, then the missed call event will not be fired for these calls. 

## Trigger variables

| Trigger variable              | Type         | Description                                                                   |
|-------------------------------|--------------|-------------------------------------------------------------------------------|
| **Call session ID**           | String       |                                                                               |
| **Call telephony session ID** | String       |                                                                               |
| **Call direction**            | String       | Possible values: "Inbound" and "Outbound."                                    |
| **Caller phone number**.      | Phone number | The phone number that initiated the phone call.                               |
| **Caller name**               | String       | The name of the caller as stored in your company directory or personal address book (if available) |
| **Recipient's phone number**  | Phone number | The phone number that received the phone call.                                |
| **Recipient name**            | String       | The name of the call recipient as stored in your company directory or personal address book (if available) |
| **Call ended date**           | date         | The date the call ended, in the format of YYYY-MM-DD.             |
| **Call ended time**           | time         | The time the call ended, in the format of HH:MM:SS (AM\|PM)                   |
| **Call ended day of week**    | day of week  |                                                                               |
