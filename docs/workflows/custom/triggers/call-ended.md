# Trigger: call ended

This event is fired when the current user disconnects from a phone call, thus ending the current telephony session, for any of the phone numbers or extensions for which they are assigned or associated. 

!!! warning "Call end reason for outbound calls"
    You may notice a trigger variable called "Call end reason." However, the value of this property is always "No Reason." The reason a call end reason for outbound calls is difficult or impossible to determine. For example, RingCentral knows when an inbound call ends because a voicemail was received, but we don't know if the caller left a voicemail in someone else's system. We hope to improve upon this in the future. In the mean time, do not rely upon or use the "Call end reason" attribute for outbound calls. 

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
| **Call missed**               | boolean      | True if the call was missed. See also: [call missed trigger](call-missed.md) |
| **Call ended date**           | date         | The date the call ended, in the format of YYYY-MM-DD.             |
| **Call ended time**           | time         | The time the call ended, in the format of HH:MM:SS (AM\|PM)                   |
| **Call ended day of week**    | day of week  |                                                                               |

