# Trigger: voicemail received

This event is fired after a voicemail is left for an extension. 

## Transcribing voicemails

One can use the [transcribe action](../actions/transcribe.md) to transcribe the voicemail's media file and add the transcription text to the current automation's context. 

## Trigger variables

| Trigger variable | Type | Description |
|-|-|-|
| **Sender's phone number** | Phone number | The phone number that sent the SMS message that was received. |
| **Sender's name** | String | If the sender exists in your address book, this variable will contain the name stored in your address book. |
| **Recipient's phone number** | Phone number | The phone number that received the voicemail. |
| **Message received date** | date | The date the voicemail was received, in the format of YYYY-MM-DD. |
| **Message received time** | time | The time the voicemail was received, in the format of HH:MM:SS (AM|PM) | 
| **Message received day of week** | day of the week | |
| **Voicemail audio** | URL | A URL pointing to the voicemail's media file. |

