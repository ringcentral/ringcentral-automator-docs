# Out-of-office SMS replies

This automation template is intended to use temporarily while one is away from the office and unable to respond to incoming SMS messages. It is great solution when you are on holiday or ill. 

When any text is received at the phone numbers identified in the "enable this automation for what phone number" field, the specified text will be sent to the sender of the text you received.

## Configuration parameters

| Parameter | Description |
|-|-|
| **Start day** | The day to begin sending the response. The day begins at 12:00am. |
| **End day** | The day to stop sending the response. The day ends at 11:59pm. The automation will be disabled at the same time. |
| **Enable this automation for what phone numbers?** | The list of phone numbers for which to enable this automation. |
| **Auto-reply text** | The message to respond with. |

When the end date arrives, this automation will be disabled automatically.
 
