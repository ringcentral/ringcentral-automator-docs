# Trigger: SMS received

This event is fired when the current user receives an SMS message via any of the phone numbers they have access to. 

## Trigger variables

| Trigger variable | Type | Description |
|-|-|-|
| **Sender's phone number** | Phone number | The phone number that sent the SMS message that was received. |
| **Sender's name** | String | If the sender exists in your address book, this variable will contain the name stored in your address book. |
| **Recipient's phone number** | Phone number | The phone number that received the SMS. |
| **Message text** | String | The exact text of the received message. |
| **Is image attached** | boolean | True if the received SMS contained an image. |
| **Message received date** | date | The date the message was received, in the format of YYYY-MM-DD. |
| **Message received time** | time | The time the message was received, in the format of HH:MM:SS (AM|PM) | 
| **Message received day of week** | day of the week | |

