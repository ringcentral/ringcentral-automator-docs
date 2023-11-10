# Trigger: chat message received

This event is fired when the current user receives a chat message via RingCentral's unified messaging app. 

## Trigger variables

| Trigger variable                 | Type            | Description                                                               |
|----------------------------------|-----------------|---------------------------------------------------------------------------|
| **Team ID**                      | String          | A string for the unique ID of the team in which the message was received. |
| **Message text**                 | String          | The text of the message.                                                  |
| **Team name**                    | String          | The name of the team in which the message was received.                   |
| **Chat type**                    | String          | Possible values: Team, Group, Direct, Personal, Everyone. See below.      |
| **Mention me**                   | boolean         | True if the message mentions the current user. False otherwise.           |
| **Message received date**        | date            | The date the voicemail was received, in the format of YYYY-MM-DD.         |
| **Message received time**        | time            | The time the voicemail was received, in the format of HH:MM:SS (AM\|PM)   |
| **Message received day of week** | day of the week |                                                                           |

### Chat types

* Team. A chat defined by a topic. Members of the team may change over time. 
* Group. A chat defined exclusively by its members. Adding a user to a group chat results in a new group chat. 
* Direct. A message between two people.
* Personal. A special private chat a user can have with themselves. Good for receiving private notifications from other apps. 
* Everyone. A special chat in which all users in an account are automatically made members. 
