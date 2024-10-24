# Trigger: call received

This event is fired when the current user receives a phone call at any of the phone numbers or extensions for which they are assigned or associated. 

## Trigger variables

| Trigger variable              | Type         | Description                                                                   |
|-------------------------------|--------------|-------------------------------------------------------------------------------|
| **Call session ID**           | String       |                                                                               |
| **Call telephony session ID** | String       |                                                                               |
| **Caller phone number**.      | Phone number | The phone number that initiated the phone call.                               |
| **Caller name**               | String       | The name of the caller as stored in your company directory or personal address book (if available) |
| **Recipient's phone number**  | Phone number | The phone number that received the phone call.                                |
| **Recipient name**            | String       | The name of the call recipient as stored in your company directory or personal address book (if available) |
| **Call received date**           | date         | The date the call was received, in the format of YYYY-MM-DD.             |
| **Call received time**           | time         | The time the call was received, in the format of HH:MM:SS (AM\|PM)                   |
| **Call received day of week**    | day of week  |                                                                               |

