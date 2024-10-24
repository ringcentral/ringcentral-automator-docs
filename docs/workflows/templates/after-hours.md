---
tags:
  - template
  - SMS
  - time-based
  - after-hours
---

# After-hours SMS auto-reply

This workflow will help respond to SMS messages received outside of regular office hours. In the template you specify your company's office hours, or the time during which they will reply to messages. If any message is received outside of these specified hours, the specified message will be sent. 

## Tips and troubleshooting

* Pay close attention to the timezone your workflow is associated with. This setting can be modified in RingCentral's admin console. See "timezone" below.
* Pay close attention to the setting of AM/PM for the times selected for your office hours. 

## Configuration parameters

| Parameter | Description |
|-|-|
| **Timezone** | The timezone in which time calculations will be made. This is a read-only field within Workflow Builder. The value of this field is set within the RingCentral admin console. Click the gear icon to modify this value, then refresh the value when you return to Workflow Builder. |
| **When if your office open?** | Specify the hours your office is open. If texts are received outside of these hours, the auto-response will be sent. | 
| **Enable this workflow for what phone numbers?** | The list of phone numbers for which to enable this workflow. |
| **Auto-reply text** | The message to respond with. |
